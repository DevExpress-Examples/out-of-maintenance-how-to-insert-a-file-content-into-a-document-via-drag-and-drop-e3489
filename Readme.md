<!-- default file list -->
*Files to look at*:

* [Form1.cs](./CS/Form1.cs) (VB: [Form1.vb](./VB/Form1.vb))
<!-- default file list end -->
# How to insert a file content into a document via drag-and-drop


<p>When the file of one of the supported formats is dropped on the RichEditControl, its content is completely replaced with this file content. But what if you wish to <strong>insert</strong> this file content into a drop position in the document? To achieve this goal, set the <strong>RichEditControl.Options.Behavior.Drop</strong> property (see <a href="https://docs.devexpress.com/OfficeFileAPI/DevExpress.XtraRichEdit.RichEditBehaviorOptions.Drop"><u>RichEditBehaviorOptions.Drop</u></a>) to DocumentCapability.Disabled, and handle drag-and-drop operations in a custom manner (see the <a href="https://supportcenter.devexpress.com/ticket/details/e2943/how-to-perform-drag-and-drop-operation-in-a-custom-manner">How to perform drag-and-drop operation in a custom manner</a> example). 
  In this example, the <a href="https://docs.devexpress.com/OfficeFileAPI/DevExpress.XtraRichEdit.RichEditDocumentServer"><u>RichEditDocumentServer</u></a> class is used to load a dropped file in memory (see the <strong>richEditControl1_DragDrop</strong> event handler). Then, the loaded document is inserted into a target RichEditControl via the <a href="https://docs.devexpress.com/OfficeFileAPI/devexpress.xtrarichedit.api.native.subdocument.insertdocumentcontent.overloads"><u>SubDocument.InsertDocumentContent Method</u></a>.</p>

<br/>


