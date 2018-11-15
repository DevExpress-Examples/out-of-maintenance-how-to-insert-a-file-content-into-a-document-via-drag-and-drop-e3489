<!-- default file list -->
*Files to look at*:

* [Form1.cs](./CS/Form1.cs) (VB: [Form1.vb](./VB/Form1.vb))
* [Program.cs](./CS/Program.cs) (VB: [Program.vb](./VB/Program.vb))
<!-- default file list end -->
# How to insert a file content into a document via drag-and-drop


<p>When the file of one of the supported formats is dropped on the RichEditControl, its content is completely replaced with this file content. But what if you wish to <strong>insert</strong> this file content into a drop position in the document? To achieve this goal, set the <strong>RichEditControl.Options.Behavior.Drop</strong> property (see <a href="http://documentation.devexpress.com/#CoreLibraries/DevExpressXtraRichEditRichEditBehaviorOptions_Droptopic"><u>RichEditBehaviorOptions.Drop</u></a>) to DocumentCapability.Disabled, and handle drag-and-drop operations in a custom manner (see the <a href="https://www.devexpress.com/Support/Center/p/E2943">How to perform drag-and-drop operation in a custom manner</a> example). The most interesting place in this example is the <strong>richEditControl1_DragDrop</strong> event handler (method). Note the manner in which the non-visual <a href="http://search.devexpress.com/?q=RichEditDocumentServer&p=T0|P0|0&d=2928"><u>RichEditDocumentServer</u></a> component is utilized to load dropped file in memory. Then, the loaded document is inserted into a target RichEditControl via the <a href="http://documentation.devexpress.com/#CoreLibraries/DevExpressXtraRichEditAPINativeSubDocument_InsertDocumentContenttopic"><u>SubDocument.InsertDocumentContent Method</u></a>.</p>

<br/>


