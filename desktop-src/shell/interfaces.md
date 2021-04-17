---
description: En esta sección se describen las interfaces del shell de Windows.
title: 'Interfaces de Shell '
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 05223970-14f5-44c2-937b-07826b8aecf9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 23bd87e86ba9e30ce443616920326bf37aba6d2c
ms.sourcegitcommit: 9a614d8ce23dcca88873148683d9ec7d38be57b9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2020
ms.locfileid: "104421680"
---
# <a name="shell-interfaces"></a>Interfaces de Shell 

En esta sección se describen las interfaces del shell de Windows.

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iaccessibleobject"><strong>IAccessibleObject</strong></a><br/></td>
<td>Expone un método que una aplicación de accesibilidad puede usar.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh448546(v=vs.85)"><strong>IAccessibilityDockingService</strong></a><br/></td>
<td>Acopla una sola ventana de la aplicación de accesibilidad en la parte inferior de una pantalla.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh448547(v=vs.85)"><strong>IAccessibilityDockingServiceCallback</strong></a><br/></td>
<td>Informa a una aplicación de accesibilidad de que su ventana se ha desacoplado.<br/></td>
</tr>
<tr class="even">
<td><a href="iaclcustommru.md"><strong>IACLCustomMRU</strong></a><br/></td>
<td>Expone métodos que se usan para inicializar una lista de elementos usados recientemente (MRU) para un objeto de finalización automática.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist"><strong>IACList</strong></a><br/></td>
<td>Expone un método que mejora la eficacia de la <a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>finalización automática</strong></a> cuando las cadenas candidatas están organizadas en una jerarquía.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist2"><strong>IACList2</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist"><strong>IACList</strong></a> para permitir a los clientes de un objeto Autocompletar recuperar y establecer marcas de opciones.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>IActionProgress</strong></a><br/></td>
<td>Representa la clase base abstracta de la que pueden heredar las operaciones basadas en progreso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogressdialog"><strong>IActionProgressDialog</strong></a><br/></td>
<td>Expone métodos que inicializan y detienen un cuadro de diálogo de progreso.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationactivationmanager"><strong>IApplicationActivationManager</strong></a><br/></td>
<td>Proporciona métodos que activan las aplicaciones de la tienda Windows para el inicio, el archivo y <a href="/previous-versions/windows/apps/hh464906(v=win.10)">las extensiones</a>de protocolo. Normalmente, utilizará esta interfaz en depuradores y herramientas de diseño.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a><br/></td>
<td>Expone métodos que consultan y establecen aplicaciones predeterminadas para un <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype"><strong>tipo de asociación</strong></a>de archivo específico y protocolos en un nivel de <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel"><strong>Asociación</strong></a>específico. <br/>
<blockquote>
[!Note]<br />
A partir de Windows 8, la única funcionalidad de esta interfaz admitida es <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault"><strong>QueryCurrentDefault</strong></a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui"><strong>IApplicationAssociationRegistrationUI</strong></a><br/></td>
<td>Expone un método que inicia un cuadro de diálogo de asociación avanzada a través del cual el usuario puede personalizar sus asociaciones.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings"><strong>IApplicationDesignModeSettings</strong></a><br/></td>
<td>Permite que las aplicaciones de herramientas de desarrollo suplanten dinámicamente los Estados de usuario y del sistema, como la resolución de pantalla nativa, el factor de escala de dispositivo y el estado de vista de la aplicación, con el fin de probar las aplicaciones de la tienda Windows que se ejecutan en modo de diseño para una amplia gama de factores de forma sin necesidad de hardware real. También permite probar los cambios normalmente en el estado controlado por el usuario para probar aplicaciones de la tienda Windows en una gran variedad de escenarios.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings2"><strong>IApplicationDesignModeSettings2</strong></a><br/></td>
<td>Permite que las aplicaciones de herramientas de desarrollo controlen dinámicamente los Estados de usuario y del sistema, como la resolución de pantalla nativa, el factor de escala de dispositivo y el diseño de la vista de aplicación, notificados a las aplicaciones de la tienda Windows con el fin de probar las aplicaciones de la tienda Windows que se ejecutan en modo de diseño para una amplia gama de factores de forma sin necesidad También permite probar los cambios normalmente en el estado controlado por el usuario para probar aplicaciones de la tienda Windows en una gran variedad de escenarios.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations"><strong>IApplicationDestinations</strong></a><br/></td>
<td>Expone métodos que permiten a una aplicación quitar uno o todos los destinos de las categorías <strong>recientes</strong> o <strong>frecuentes</strong> en una Jump List.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists"><strong>IApplicationDocumentLists</strong></a><br/></td>
<td>Expone métodos que permiten a una aplicación recuperar el contenido de las categorías <strong>recientes</strong> o <strong>frecuentes</strong> en una Jump List.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher"><strong>IAppPublisher</strong></a><br/></td>
<td>Expone métodos para publicar aplicaciones a través de <strong>Agregar o quitar programas</strong> en el panel de control. Esta es la interfaz principal implementada para este fin.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility"><strong>IAppVisibility</strong></a><br/></td>
<td>Proporciona funcionalidad para determinar si la pantalla muestra las aplicaciones de la tienda Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibilityevents"><strong>IAppVisibilityEvents</strong></a><br/></td>
<td>Permite que las aplicaciones reciban notificaciones de cambios de estado en una pantalla y de cambios en la visibilidad de la pantalla Inicio.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler"><strong>IAssocHandler</strong></a><br/></td>
<td>Expone métodos para operaciones con un cuadro de diálogo o un menú de Asociación de archivos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandlerinvoker"><strong>IAssocHandlerInvoker</strong></a><br/></td>
<td>Expone métodos que invocan un controlador de aplicación asociado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute"><strong>IAttachmentExecute</strong></a><br/></td>
<td>Expone métodos que funcionan con las aplicaciones cliente para presentar un entorno de usuario que proporciona descarga e intercambio seguro de archivos a través de mensajes de correo electrónico y datos adjuntos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>IAutoComplete</strong></a><br/></td>
<td>Expuesto por el objeto AutoComplete (CLSID_AutoComplete). Esta interfaz permite a las aplicaciones inicializar, habilitar y deshabilitar el objeto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete2"><strong>IAutoComplete2</strong></a><br/></td>
<td>Extiende <a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>IAutoComplete</strong></a>. Esta interfaz permite a los clientes del objeto Autocompletar recuperar y establecer una serie de opciones que controlan el funcionamiento de la finalización automática.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iautocompletedropdown"><strong>IAutoCompleteDropDown</strong></a><br/></td>
<td>Expone métodos que permiten a los clientes restablecer o consultar el estado de presentación de la lista desplegable de autocompletar, que contiene posibles finalizaciones en una cadena especificada por el usuario en un control de edición.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ibandhost"><strong>IBandHost</strong></a><br/></td>
<td>Expone métodos que crean y destruyen bandas y especifican su disponibilidad.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ibandsite"><strong>IBandSite</strong></a><br/></td>
<td>Expone métodos que controlan objetos de banda.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ibrowserframeoptions"><strong>IBrowserFrameOptions</strong></a><br/></td>
<td>Permite a un explorador o un host preguntar a <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> qué tipo de comportamiento de la vista se admite.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icategorizer"><strong>ICategorizer</strong></a><br/></td>
<td>Expone métodos que se usan para obtener información sobre las listas de identificadores de elementos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icategoryprovider"><strong>ICategoryProvider</strong></a><br/></td>
<td>Expone una lista de categorizadores registrada en un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icdburn"><strong>ICDBurn</strong></a><br/></td>
<td>Expone métodos que determinan si un sistema tiene hardware para escribir en el CD, la letra de unidad de un dispositivo de grabadora de CD y inicia mediante programación una sesión de grabación de CD. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a><br/></td>
<td>Expone métodos que permiten la inspección y manipulación de columnas en la vista de detalles del explorador de Windows. Una estructura <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> hace referencia a cada columna, que asigna un nombre a una propiedad.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a><br/></td>
<td>Expuesto por los cuadros de diálogo de archivos comunes que se usarán cuando hospeden un explorador de Shell. Si se admite, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a> expone métodos que permiten que una vista de Shell controle varios casos que requieren un comportamiento diferente en un cuadro de diálogo que en una vista de Shell normal. Puede obtener un puntero de interfaz <strong>ICommDlgBrowser</strong> llamando a <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> en el objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a><br/></td>
<td>Extiende las capacidades de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a>. Esta interfaz se expone mediante los cuadros de diálogo de archivos comunes cuando hospedan un explorador de Shell. Un puntero a <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a> se puede obtener llamando a <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> en el objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icommdlgbrowser3"><strong>ICommDlgBrowser3</strong></a><br/></td>
<td>Extiende las capacidades de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a>y se usan en los cuadros de diálogo de archivos comunes cuando hospedan un explorador de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl/nn-shobjidl-icomputerinfochangenotify"><strong>IComputerInfoChangeNotify</strong></a><br/></td>
<td>Es posible que esta interfaz no esté presente en versiones posteriores de Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential"><strong>IConnectableCredentialProviderCredential</strong></a><br/></td>
<td>Expone métodos para conectar y desconectar objetos <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential"><strong>IConnectableCredentialProviderCredential</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-icontactmanagerinterop"><strong>IContactManagerInterop</strong></a><br/></td>
<td>Habilita el acceso a los métodos de <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-icontactmanagerinterop"><strong>ContactManager</strong></a> en una aplicación que administra varias ventanas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a><br/></td>
<td>Expone métodos que crean o combinan un menú contextual asociado a un objeto de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2"><strong>IContextMenu2</strong></a><br/></td>
<td>Expone métodos que crean o combinan un menú contextual asociado a un objeto de Shell. Extiende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a> agregando un método que permite a los objetos de cliente controlar los mensajes asociados a los elementos de menú dibujados por el propietario.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3"><strong>IContextMenu3</strong></a><br/></td>
<td>Expone métodos que crean o combinan un menú contextual asociado a un objeto de Shell. Permite a los objetos de cliente controlar los mensajes asociados a los elementos de menú dibujados por el propietario y extiende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2"><strong>IContextMenu2</strong></a> aceptando un valor devuelto de ese control de mensajes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb"><strong>IContextMenuCB</strong></a><br/></td>
<td>Expone un método que habilita la devolución de llamada de un menú contextual. Por ejemplo, para agregar un icono de escudo a un <strong>MenuItem</strong> que requiere elevación.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/bb776063(v=vs.85)"><strong>IControlMarkup</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)"><strong>ICopyHook</strong></a><br/></td>
<td>Expone un método que crea un <em>controlador de enlace de copia</em>. Un controlador de enlace de copia es una extensión de Shell que determina si un objeto de impresora o carpeta de Shell puede moverse, copiarse, cambiar de nombre o eliminarse. El shell llama al método <a href="/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)"><strong>ICopyHook:: CopyCallback</strong></a> antes de realizar una de estas operaciones.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>ICreateObject</strong></a><br/></td>
<td>Expone un método que crea un objeto de una clase especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess"><strong>ICreatingProcess</strong></a><br/></td>
<td>Lo usan <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a> para permitir que el autor de la llamada modifique algunos parámetros del proceso que se está creando.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs"><strong>ICreateProcessInputs</strong></a><br/></td>
<td>Lo usa la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess"><strong>ICreatingProcess</strong></a> para modificar algunos parámetros del proceso que se está creando.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovider"><strong>ICredentialProvider</strong></a><br/></td>
<td>Expone los métodos utilizados en la instalación y manipulación de un proveedor de credenciales. Todos los proveedores de credenciales deben implementar esta interfaz.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredential"><strong>ICredentialProviderCredential</strong></a><br/></td>
<td>Expone métodos que habilitan el control de una credencial.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredential2"><strong>ICredentialProviderCredential2</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredential"><strong>ICredentialProviderCredential</strong></a> agregando un método que recupera el identificador de seguridad (SID) de un usuario. La credencial está asociada a ese usuario y se puede agrupar en el icono del usuario.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents"><strong>ICredentialProviderCredentialEvents</strong></a><br/></td>
<td>Proporciona un mecanismo de devolución de llamada asincrónica que usa una credencial para notificarle los eventos de cambio de estado o de texto en la interfaz de usuario de credenciales o de inicio de sesión.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredentialevents2"><strong>ICredentialProviderCredentialEvents2</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents"><strong>ICredentialProviderCredentialEvents</strong></a> agregando métodos que habilitan la actualización por lotes de campos en la interfaz de usuario de credenciales o la interfaz de usuario de logo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredentialwithfieldoptions"><strong>ICredentialProviderCredentialWithFieldOptions</strong></a><br/></td>
<td>Proporciona un método que permite que el marco de trabajo del proveedor de credenciales determine si ha realizado una personalización en la opción de un campo en una interfaz de usuario de credenciales o de inicio de sesión.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialproviderevents"><strong>ICredentialProviderEvents</strong></a><br/></td>
<td>Proporciona un mecanismo de devolución de llamada asincrónica que usa un proveedor de credenciales para notificar los cambios en la lista de credenciales o sus campos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialproviderfilter"><strong>ICredentialProviderFilter</strong></a><br/></td>
<td>Se usa para filtrar dinámicamente los proveedores de credenciales en función de la información disponible en tiempo de ejecución.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidersetuserarray"><strong>ICredentialProviderSetUserArray</strong></a><br/></td>
<td>Proporciona un método que permite a un proveedor de credenciales recibir el conjunto de usuarios que se mostrarán en la interfaz de usuario de credenciales o de inicio de sesión.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovideruser"><strong>ICredentialProviderUser</strong></a><br/></td>
<td>Proporciona métodos que se usan para recuperar ciertas propiedades de un usuario individual incluido en una interfaz de usuario de credenciales o de inicio de sesión.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovideruserarray"><strong>ICredentialProviderUserArray</strong></a><br/></td>
<td>Representa el conjunto de usuarios que aparecerán en la interfaz de usuario de credenciales o de inicio de sesión. Esta información permite al proveedor de credenciales enumerar el conjunto para recuperar información de propiedades sobre cada usuario para rellenar los campos o filtrar el conjunto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icurrentitem"><strong>ICurrentItem</strong></a><br/></td>
<td>Se obtiene mediante una llamada a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> para un elemento. Si el elemento representa una instantánea de un elemento en un momento anterior, esta interfaz obtendrá la versión actual del elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-icurrentworkingdirectory"><strong>ICurrentWorkingDirectory</strong></a><br/></td>
<td>Expone métodos que permiten a un cliente recuperar o establecer el directorio de trabajo actual de un objeto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist"><strong>ICustomDestinationList</strong></a><br/></td>
<td>Expone métodos que permiten a una aplicación proporcionar una Jump List personalizada, incluidos los destinos y las tareas, para su presentación en la barra de tareas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability"><strong>IDataObjectAsyncCapability</strong></a><br/></td>
<td>Habilita las interfaces que normalmente son sincrónicas para funcionar de forma asincrónica. <br/>
<blockquote>
[!Note]<br />
Esta interfaz es la versión actual, con el nombre cambiado, de <a href="/previous-versions//bb776309(v=vs.85)"><strong>IAsyncOperation</strong></a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idataobjectprovider"><strong>IDataObjectProvider</strong></a><br/></td>
<td>Proporciona métodos que permiten establecer o recuperar la <a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>interfaz IDataObject</strong></a>de un objeto de <a href="/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage?view=winrt-19041">paquete</a> de objetos, que el paquete de paquetes de componentes utiliza para admitir la interoperabilidad. Una aplicación usa el objeto de paquete de datos para proporcionar datos a otra aplicación.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idatatransfermanagerinterop"><strong>IDataTransferManagerInterop</strong></a><br/></td>
<td>Habilita el acceso a los métodos de <a href="/uwp/api/Windows.ApplicationModel.DataTransfer.DataTransferManager"><strong>DataTransferManager</strong></a> en una aplicación de la tienda Windows que administra varias ventanas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit"><strong>IDefaultExtractIconInit</strong></a><br/></td>
<td>Expone métodos para establecer los iconos predeterminados asociados a un objeto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultfoldermenuinitialize"><strong>IDefaultFolderMenuInitialize</strong></a><br/></td>
<td>Proporciona métodos que se usan para obtener y establecer información de menú contextual. Esta información es la misma que la que se proporciona para <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultContextMenu</strong></a> a través de la estructura <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-idelayedpropertystorefactory"><strong>IDelayedPropertyStoreFactory</strong></a><br/></td>
<td>Expone un método para crear un objeto <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> especificado en circunstancias en las que el acceso a la propiedad es potencialmente lento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegatefolder"><strong>IDelegateFolder</strong></a><br/></td>
<td>Expone un método a través del cual se proporciona a una carpeta de delegado la interfaz <a href="/windows/desktop/api/objidl/nn-objidl-imalloc"><strong>IMalloc</strong></a> necesaria para asignar y liberar identificadores de elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegateitem"><strong>IDelegateItem</strong></a><br/></td>
<td>Se utiliza para obtener la representación subyacente inmediatamente de la ruta de acceso de un elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idesktopgadget"><strong>IDesktopGadget</strong></a><br/></td>
<td>Expone un método que permite la adición mediante programación de un gadget instalado al escritorio del usuario.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper"><strong>IDesktopWallpaper</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory"><strong>IDestinationStreamFactory</strong></a><br/></td>
<td>Expone un método para copiar manualmente una secuencia o un archivo antes de aplicar los cambios a las propiedades.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idisplayitem"><strong>IDisplayItem</strong></a><br/></td>
<td>Expone métodos que buscan una versión del elemento actual que se va a usar para obtener las propiedades de presentación, como el nombre del elemento, que se mostrarán en la interfaz de usuario. Lo usan los cuadros de diálogo del motor de copia para proporcionar la interfaz de usuario con el elemento adecuado que se va a mostrar. Si no se encuentra ninguna otra versión, se usa el elemento actual.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a><br/></td>
<td>Expone métodos que notifican a los cambios el objeto de ventana de acoplamiento, lo que incluye la eliminación, ocultación y desinstalación inminente. Esta interfaz se implementa mediante objetos de ventana que se pueden acoplar dentro del espacio del borde de una ventana del explorador de Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe"><strong>IDockingWindowFrame</strong></a><br/></td>
<td>Expone métodos que admiten la adición de objetos <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a> a un marco. Implementado por el explorador.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite"><strong>IDockingWindowSite</strong></a><br/></td>
<td>Expone métodos que administran el espacio del borde de uno o más objetos <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a> . El explorador implementa esta interfaz y es similar a la interfaz <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow"><strong>IOleInPlaceUIWindow</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper"><strong>IDragSourceHelper</strong></a><br/></td>
<td>Expuesto por el shell para permitir que una aplicación especifique la imagen que se mostrará durante una operación de arrastrar y colocar del shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idragsourcehelper2"><strong>IDragSourceHelper2</strong></a><br/></td>
<td>Expone un método que agrega funcionalidad a <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper"><strong>IDragSourceHelper</strong></a>. Este método establece las características de una operación de arrastrar y colocar sobre un objeto <strong>IDragSourceHelper</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper"><strong>IDropTargetHelper</strong></a><br/></td>
<td>Expone métodos que permiten a los destinos de colocación mostrar una imagen de arrastre mientras la imagen está sobre la ventana de destino.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idynamichwhandler"><strong>IDynamicHWHandler</strong></a><br/></td>
<td>Llamado por reproducción automática. Expone métodos que obtienen información dinámica sobre un controlador registrado antes de mostrarlo al usuario.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumassochandlers"><strong>IEnumAssocHandlers</strong></a><br/></td>
<td>Expone un método que permite la enumeración de una colección de controladores asociados a extensiones de nombre de archivo determinadas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ienumerableview"><strong>IEnumerableView</strong></a><br/></td>
<td>Expone métodos que enumeran el contenido de una vista y reciben una notificación de devolución de llamada en la finalización de la enumeración. Esta interfaz permite a los clientes de una vista intentar compartir la lista de contenido de la carpeta de la vista.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumexplorercommand"><strong>IEnumExplorerCommand</strong></a><br/></td>
<td>Proporcionado por un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a>. Esta interfaz contiene la enumeración de los comandos que se van a colocar en la barra de comandos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>IEnumExtraSearch</strong></a><br/></td>
<td>Enumerador OLE estándar utilizado por un cliente para determinar los objetos de búsqueda disponibles para una carpeta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumfullidlist"><strong>IEnumFullIDList</strong></a><br/></td>
<td>Expone un conjunto estándar de métodos que enumeran los punteros a listas de identificadores de elemento (PIDL) de los elementos de una carpeta de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist"><strong>IEnumIDList</strong></a><br/></td>
<td>Expone un conjunto estándar de métodos que se usan para enumerar el PIDL de los elementos de una carpeta de Shell. Cuando se llama al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder:: EnumObjects</strong></a> de una carpeta, se crea un objeto de enumeración y pasa un puntero a la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist"><strong>IEnumIDList</strong></a> del objeto a la aplicación que realiza la llamada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumobjects"><strong>IEnumObjects</strong></a><br/></td>
<td>Expone métodos para enumerar objetos desconocidos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps"><strong>IEnumPublishedApps</strong></a><br/></td>
<td>Expone métodos que enumeran las aplicaciones publicadas para agregar o quitar programas en el panel de control. El objeto que expone esta interfaz se solicita a través de <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-iapppublisher-enumapps"><strong>IAppPublisher:: EnumApps</strong></a>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ienumreadycallback"><strong>IEnumReadyCallback</strong></a><br/></td>
<td>Expone métodos que permiten a la vista notificar al implementador cuando se ha completado la enumeración. La vista llama a este método para indicar al implementador que la enumeración se puede recuperar a través de <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-ienumerableview-createenumidlistfromcontents"><strong>IEnumerableView:: CreateEnumIDListFromContents</strong></a>. La devolución de llamada permite al implementador compartir la enumeración de vistas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumresources"><strong>IEnumResources</strong></a><br/></td>
<td>Expone los métodos de enumeración de recursos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems"><strong>IEnumShellItems</strong></a><br/></td>
<td>Expone la enumeración de las interfaces <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> . Normalmente, esta interfaz se obtiene llamando al método <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems"><strong>IEnumShellItems</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrconflict"><strong>IEnumSyncMgrConflict</strong></a><br/></td>
<td>Expone métodos de enumeración de conflictos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrevents"><strong>IEnumSyncMgrEvents</strong></a><br/></td>
<td>Expone métodos de enumeración de eventos de sincronización.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems"><strong>IEnumSyncMgrSyncItems</strong></a><br/></td>
<td>Expone métodos que enumeran los objetos de elemento de sincronización administrados por el controlador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a><br/></td>
<td>Expone métodos que establecen un estado o un parámetro determinado relacionados con el verbo de comando, así como un método para invocar ese verbo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandapplicationhostenvironment"><strong>IExecuteCommandApplicationHostEnvironment</strong></a><br/></td>
<td>Proporciona un método único que permite que una aplicación determine si su host está en modo de escritorio o envolvente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandhost"><strong>IExecuteCommandHost</strong></a><br/></td>
<td>Proporciona un método que permite a un controlador de verbos de Shell basado en <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a>consultar el modo de interfaz de usuario del componente host desde el que se invocó la aplicación.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a> es un objeto de explorador al que se puede navegar o que puede hospedar una vista de un objeto de datos. Como objeto de explorador con todas las características, también admite un registro de viajes automático.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowserevents"><strong>IExplorerBrowserEvents</strong></a><br/></td>
<td>Expone métodos para la notificación de navegación del explorador del explorador y eventos de creación de vistas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a><br/></td>
<td>Expone métodos que obtienen la apariencia del comando, enumeran subcomandos o invocan el comando.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a><br/></td>
<td>Expone métodos para crear los comandos del explorador y los enumeradores de comandos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate"><strong>IExplorerCommandState</strong></a><br/></td>
<td>Expone un método único que permite la recuperación del estado del comando.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a><br/></td>
<td>Se usa en el explorador de Windows mediante una implementación de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> para proporcionar sugerencias a la vista sobre los paneles visibles. Además, un host de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a> puede utilizar esta interfaz para proporcionar información sobre la visibilidad del panel. El host debe implementar <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a> con <strong>SID_ExplorerPaneVisibility</strong> como identificador de servicio. El host debe estar en la cadena de sitios. <br/> La implementación de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a> se recupera de la carpeta de Shell. La carpeta Shell, a su vez, se recupera de la vista. Una extensión de espacio de nombres puede optar por proporcionar una vista personalizada (<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>) en lugar de usar el objeto de vista de carpeta del sistema (DefView). En ese caso, la implementación de <strong>IShellView</strong> debe incluir una implementación de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder"><strong>IFolderView:: GetFolder</strong></a> para devolver el objeto <strong>IExplorerPaneVisibility</strong> .<br/> Una extensión de espacio de nombres puede proporcionar una vista personalizada implementando <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> en lugar de usar el objeto de vista de carpeta del sistema (DefView). En ese caso, la implementación de <strong>IShellView</strong> debe incluir una implementación de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder"><strong>IFolderView:: GetFolder</strong></a> para usar <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona"><strong>IExtractIcon</strong></a><br/></td>
<td>Expone métodos que permiten a un cliente recuperar el icono que está asociado a uno de los objetos de una carpeta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage"><strong>IExtractImage</strong></a><br/></td>
<td>Expone métodos que solicitan una imagen en miniatura de una carpeta de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2"><strong>IExtractImage2</strong></a><br/></td>
<td>Extiende las capacidades de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage"><strong>IExtractImage</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a><br/></td>
<td>Expone métodos que inicializan, muestran y obtienen resultados del cuadro de diálogo de archivo común.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialog2"><strong>IFileDialog2</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> proporcionando métodos que permiten al llamador asignar un nombre a una ubicación específica y restringida que se puede examinar en el cuadro de diálogo de archivo común, así como especificar texto alternativo que se va a mostrar como etiqueta en el botón <strong>Cancelar</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents"><strong>IFileDialogControlEvents</strong></a><br/></td>
<td>Expone métodos que permiten a una aplicación recibir notificaciones de eventos relacionados con los controles que la aplicación ha agregado a un cuadro de diálogo de archivo común.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize"><strong>IFileDialogCustomize</strong></a><br/></td>
<td>Expone métodos que permiten a una aplicación agregar controles a un cuadro de diálogo de archivo común.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents"><strong>IFileDialogEvents</strong></a><br/></td>
<td>Expone métodos que permiten la notificación de eventos dentro de un cuadro de diálogo de archivo común.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileisinuse"><strong>IFileIsInUse</strong></a><br/></td>
<td>Expone métodos a los que se puede llamar para obtener o cerrar un archivo que está usando otra aplicación. Cuando una aplicación intenta tener acceso a un archivo y encuentra ese archivo ya en uso, puede usar los métodos de esta interfaz para recopilar información que se presenta al usuario en un cuadro de diálogo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog"><strong>IFileOpenDialog</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> agregando métodos específicos para el cuadro de diálogo Abrir.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a><br/></td>
<td>Expone métodos para copiar, trasladar, cambiar el nombre, crear y eliminar elementos de Shell, así como métodos para proporcionar cuadros de diálogo de progreso y error. Esta interfaz reemplaza la función <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink"><strong>IFileOperationProgressSink</strong></a><br/></td>
<td>Expone métodos que proporcionan un sistema de notificaciones completo utilizado por los llamadores de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> para supervisar los detalles de las operaciones que se realizan a través de esa interfaz.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog"><strong>IFileSaveDialog</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> agregando métodos específicos para el cuadro de diálogo Guardar, que incluyen aquellos que proporcionan compatibilidad para que la colección de metadatos se conserve con el archivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesyncmergehandler"><strong>IFileSyncMergeHandler</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a><br/></td>
<td>Expone métodos que almacenan información del sistema de archivos para optimizar las llamadas a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2</strong></a><br/></td>
<td>Extiende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a>, que almacena información del sistema de archivos para optimizar las llamadas a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a>. Esta interfaz agrega el conjunto de capacidad o el identificador de la clase de unión (CLSID).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/shell/schema-library-iconreference"><strong>IFileViewer</strong></a><br/></td>
<td>Expone métodos que designan una interfaz que permite a un visor de archivos registrado recibir una notificación cuando debe mostrar o imprimir un archivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-ifileviewersite"><strong>IFileViewerSite</strong></a><br/></td>
<td>Expone métodos que designan una interfaz que permite que un visor de archivos recupere el identificador de la ventana anclada actual o establece una nueva ventana anclada. La ventana anclada es la ventana en la que el visor de archivos actual muestra un archivo. Cuando el usuario selecciona un archivo nuevo para verlo, el shell dirige el visor de archivos para que muestre el nuevo archivo en la ventana anclada en lugar de crear una nueva ventana.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfilter"><strong>IFolderFilter</strong></a><br/></td>
<td>Expuesto por un cliente para especificar cómo filtrar la enumeración de una carpeta de Shell por una aplicación de servidor.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfiltersite"><strong>IFolderFilterSite</strong></a><br/></td>
<td>Exportado por un host para permitir que los clientes especifiquen cómo filtrar una enumeración de carpetas de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a><br/></td>
<td>Expone métodos que recuperan información sobre las opciones de presentación de una carpeta, seleccionan los elementos especificados en esa carpeta y establecen el modo de vista de la carpeta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2"><strong>IFolderView2</strong></a><br/></td>
<td>Expone métodos que recuperan información sobre las opciones de presentación de una carpeta, seleccionan los elementos especificados en esa carpeta y establecen el modo de vista de la carpeta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewhost"><strong>IFolderViewHost</strong></a><br/></td>
<td>Expone un método que hospeda un objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a> en una ventana.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewoptions"><strong>IFolderViewOptions</strong></a><br/></td>
<td>Expone métodos que permiten controlar las opciones de la vista de carpetas específicas de las vistas de Windows 7 y versiones posteriores.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderviewsettings"><strong>IFolderViewSettings</strong></a><br/></td>
<td>Expone métodos para obtener la configuración de la vista de carpetas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpane"><strong>IFrameworkInputPane</strong></a><br/></td>
<td>Proporciona métodos que permiten informar a las aplicaciones de los cambios de estado y la ubicación del panel de entrada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpanehandler"><strong>IFrameworkInputPaneHandler</strong></a><br/></td>
<td>Permite a una aplicación recibir una notificación cuando se muestra u oculta el panel de entrada (el teclado en pantalla o el panel de escritura a mano). Esto permite que la ventana de la aplicación ajuste su presentación para que ninguna área de entrada (como un cuadro de texto) quede oculta en el panel de entrada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost"><strong>IHandlerActivationHost</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandlerinfo"><strong>IHandlerInfo</strong></a><br/></td>
<td>Proporciona métodos que proporcionan información sobre el controlador a los métodos de la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost"><strong>IHandlerActivationHost</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup"><strong>IHomeGroup</strong></a><br/></td>
<td>Expone métodos que determinan el estado de pertenencia a un grupo en el hogar del equipo y muestran el Asistente para uso compartido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler"><strong>IHWEventHandler</strong></a><br/></td>
<td>Se llama mediante reproducción automática para implementar el control de los tipos de medios registrados.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler2"><strong>IHWEventHandler2</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler"><strong>IHWEventHandler</strong></a> para direccionar la elevación de control de cuentas de usuario (UAC) para los controladores de dispositivos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iidentityname"><strong>IIdentityName</strong></a><br/></td>
<td>Expone métodos para comparar dos elementos y ver si son iguales.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iimagerecompress"><strong>IImageRecompress</strong></a><br/></td>
<td>Expone un método que recomprime las imágenes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a><br/></td>
<td>Expone un método único que se usa para inicializar objetos que implementan <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate"><strong>IExplorerCommandState</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> o <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> con el nombre de comando especificado por la aplicación y sus propiedades registradas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl/nn-shobjidl-iinitializenetworkfolder"><strong>IInitializeNetworkFolder</strong></a><br/></td>
<td>Expone un método que inicializa el origen de datos de red CLSID_NetworkPlaces tal como se especifica.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithbindctx"><strong>IInitializeWithBindCtx</strong></a><br/></td>
<td>Expone un método que inicializa un controlador, como un controlador de propiedad, un controlador de miniaturas o un controlador de vista previa, con un contexto de enlace.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile"><strong>IInitializeWithFile</strong></a><br/></td>
<td>Expone un método para inicializar un controlador, como un controlador de propiedad, un controlador de miniaturas o un controlador de vista previa, con una ruta de acceso de archivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem"><strong>IInitializeWithItem</strong></a><br/></td>
<td>Expone un método que se usa para inicializar un controlador, como un controlador de propiedad, un controlador de miniaturas o un controlador de vista previa, con un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithpropertystore"><strong>IInitializeWithPropertyStore</strong></a><br/></td>
<td>Expone un método que inicializa un controlador, como un controlador de propiedad, un controlador de miniaturas o un controlador de vista previa, con un almacén de propiedades.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream"><strong>IInitializeWithStream</strong></a><br/></td>
<td>Expone un método que inicializa un controlador, como un controlador de propiedad, un controlador de miniaturas o un controlador de vista previa, con una secuencia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithwindow"><strong>IInitializeWithWindow</strong></a><br/></td>
<td>Expone un método a través del cual un cliente puede proporcionar una ventana propietaria a un objeto Windows Runtime utilizado en una aplicación de escritorio.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject"><strong>IInputObject</strong></a><br/></td>
<td>Expone métodos que cambian la activación de la interfaz de usuario y aceleradores de procesos para un objeto de entrada de usuario incluido en el shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject2"><strong>IInputObject2</strong></a><br/></td>
<td>Expone un método que extiende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject"><strong>IInputObject</strong></a> controlando los aceleradores globales.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite"><strong>IInputObjectSite</strong></a><br/></td>
<td>Expone un método que se utiliza para comunicar los cambios de foco de un objeto de entrada de usuario incluido en el shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration"><strong>IInputPanelConfiguration</strong></a><br/></td>
<td>Proporciona funcionalidad para que las aplicaciones de escritorio participen en el mecanismo de seguimiento de foco usado en las aplicaciones de la tienda Windows.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelinvocationconfiguration"><strong>IInputPanelInvocationConfiguration</strong></a><br/></td>
<td>Permite a las aplicaciones de la tienda Windows rechazar el comportamiento de invocación automática.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iiocancelinformation"><strong>IIOCancelInformation</strong></a><br/></td>
<td>Expone métodos para publicar un mensaje de la ventana cancelar en el subproceso del proceso desde el cuadro de diálogo de progreso. <br/> Esta interfaz permite que el cuadro de diálogo de progreso publique un mensaje de subproceso a través de <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea"><strong>PostThreadMessage</strong></a> en el subproceso de trabajo para cancelar sus operaciones. El subproceso de trabajo debe comprobar periódicamente la cola de mensajes mediante <a href="/windows/desktop/api/winuser/nf-winuser-getmessage"><strong>GetMessage</strong></a>, <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea"><strong>PeekMessage</strong></a> o <a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex"><strong>MsgWaitForMultipleObjectsEx</strong></a>.<br/> El método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iiocancelinformation-setcancelinformation"><strong>IIOCancelInformation:: SetCancelInformation</strong></a> indica al cuadro de diálogo de progreso qué identificador de subproceso y qué mensaje se <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea"><strong>PostThreadMessage</strong></a> cuando el usuario hace clic en <strong>Cancelar</strong>. Un ID. de subproceso de &quot; cero &quot; deshabilita la operación de envío para el mensaje de cancelación.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iitemnamelimits"><strong>IItemNameLimits</strong></a><br/></td>
<td>Recupera una lista de caracteres válidos y no válidos, o la longitud máxima de un nombre en el espacio de nombres. Use esta interfaz para el análisis y la traducción de la validación.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder"><strong>IKnownFolder</strong></a><br/></td>
<td>Expone métodos que permiten a una aplicación recuperar información sobre la categoría, el tipo, el GUID, el valor de PIDL, las capacidades de redirección y la definición de una carpeta conocida. Proporciona un método para el recuperación del objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> de una carpeta conocida. También proporciona métodos para obtener o establecer la ruta de acceso de la carpeta conocida.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager"><strong>IKnownFolderManager</strong></a><br/></td>
<td>Expone métodos que crean, enumeran o administran carpetas conocidas existentes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceappusermodelid"><strong>ILaunchSourceAppUserModelId</strong></a><br/></td>
<td>Proporciona un método para recuperar un <a href="appids.md">AppUserModelId</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceviewsizepreference"><strong>ILaunchSourceViewSizePreference</strong></a><br/></td>
<td>Proporciona métodos para recuperar información sobre la aplicación de origen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetmonitor"><strong>ILaunchTargetMonitor</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetviewsizepreference"><strong>ILaunchTargetViewSizePreference</strong></a><br/></td>
<td>Proporciona un método para recuperar el tamaño de vista preferido para una nueva ventana de la aplicación.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/shell-extensibility-bumper"><strong>IMarkupCallback</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup"><strong>IMenuPopup</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup"><strong>IMenuPopup</strong></a> puede modificarse o no estar disponible.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow"><strong>IModalWindow</strong></a><br/></td>
<td>Expone un método que representa una ventana modal. Esta interfaz se usa en el Asistente de Windows XP Passport.<br/></td>
</tr>
<tr class="odd">
<td><a href="imultimonitordockingsite.md"><strong>IMultiMonitorDockingSite</strong></a><br/></td>
<td>Implementado por el explorador. Expone métodos que administran el monitor que contiene la barra de tareas de Windows en un sistema de varios monitores. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-inamedpropertybag"><strong>INamedPropertyBag</strong></a><br/></td>
<td>Expone métodos que proporcionan un objeto con un contenedor de propiedades especificado en el que el objeto puede guardar sus propiedades.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-inamedpropertystore"><strong>INamedPropertyStore</strong></a><br/></td>
<td>Expone métodos que obtienen y establecen propiedades con nombre.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreeaccessible"><strong>INameSpaceTreeAccessible</strong></a><br/></td>
<td>Expone métodos que realizan acciones de accesibilidad en un elemento de Shell desde un control de árbol de espacios de nombres.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a><br/></td>
<td>Expone los métodos utilizados para ver y manipular los nodos de un árbol de elementos de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrol2"><strong>INameSpaceTreeControl2</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a> proporcionando métodos que obtienen y establecen los estilos de presentación de los controles TreeView para su uso con elementos de espacio de nombres de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>INameSpaceTreeControlCustomDraw</strong></a><br/></td>
<td>Expone métodos que permiten al usuario dibujar un control de árbol de espacios de nombres personalizado y sus elementos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontroldrophandler"><strong>INameSpaceTreeControlDropHandler</strong></a><br/></td>
<td>Expone métodos de controlador para arrastrar y colocar. Lo utiliza el control de árbol de espacios de nombres para notificar al cliente de cualquier operación de arrastrar y colocar que se produzca en el control. Proporciona una forma para que un cliente intercepte una operación de colocar y realice su propia acción, o para devolver el efecto de colocación deseado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolevents"><strong>INameSpaceTreeControlEvents</strong></a><br/></td>
<td>Expone métodos para controlar los eventos <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrolfoldercapabilities"><strong>INameSpaceTreeControlFolderCapabilities</strong></a><br/></td>
<td>Expone un método único que recupera el estado de la compatibilidad con el filtrado <a href="/windows/desktop/properties/props-system-ispinnedtonamespacetree">System. IsPinnedToNameSpaceTree</a> de una carpeta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk"><strong>INamespaceWalk</strong></a><br/></td>
<td>Expone métodos que recorren un espacio de nombres desde un nodo raíz determinado. Se especifica la profundidad del recorrido y se devuelve una matriz opcional que contiene los identificadores de todos los nodos examinados.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a><br/></td>
<td>Una interfaz de devolución de llamada que expone métodos usados con <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk"><strong>INamespaceWalk</strong></a>. Después de realizar un recorrido con <strong>INamespaceWalk</strong>, un objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> que representa los nodos recorridos se pasa a los métodos <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a> . Lo que hacen esos métodos con la información depende del objeto que los implementa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb2"><strong>INamespaceWalkCB2</strong></a><br/></td>
<td>Extiende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a> con un método necesario para completar un recorrido del espacio de nombres. Este método quita los datos recopilados durante el recorrido. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inewmenuclient"><strong>INewMenuClient</strong></a><br/></td>
<td>Expone métodos que permiten la manipulación de los elementos de un menú de Windows 7.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka"><strong>INewShortcutHook</strong></a><br/></td>
<td>Expone métodos para crear un nuevo acceso directo a Internet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inewwindowmanager"><strong>INewWindowManager</strong></a><br/></td>
<td>Expone un método que determina si se debe mostrar o bloquear una ventana iniciada por otra ventana, lo que permite el control de ventanas emergentes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica"><strong>INotifyReplica</strong></a><br/></td>
<td>Expone un método que proporciona el creador de un objeto con los medios para notificar al objeto que puede estar sujeto a una conciliación posterior. El reconciliador del maletín es responsable de la implementación de esta interfaz.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Objectarray/nn-objectarray-iobjectarray"><strong>IObjectArray</strong></a><br/></td>
<td>Expone métodos que permiten a los clientes tener acceso a los elementos de una colección de objetos que admiten <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectcollection"><strong>IObjectCollection</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/Objectarray/nn-objectarray-iobjectarray"><strong>IObjectArray</strong></a> proporcionando métodos que permiten a los clientes agregar y quitar objetos que admiten <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> en una colección.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectprovider"><strong>IObjectProvider</strong></a><br/></td>
<td>Expone un método para detectar objetos que se denominan con un <strong>GUID</strong> de otro objeto. A diferencia de <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a> , esta interfaz no delegará su funcionalidad en otros objetos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithappusermodelid"><strong>IObjectWithAppUserModelID</strong></a><br/></td>
<td>Expone métodos que permiten a los implementadores de un objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler"><strong>IAssocHandler</strong></a> personalizado proporcionar acceso a su identificador de modelo de usuario de aplicación explícito (AppUserModelID). Esta información se usa para determinar si un tipo de archivo determinado se puede Agregar a la Jump List de una aplicación.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithbackreferences"><strong>IObjectWithBackReferences</strong></a><br/></td>
<td>Proporciona un método para interactuar con las referencias inversas retenidas por un objeto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithcancelevent"><strong>IObjectWithCancelEvent</strong></a><br/></td>
<td>Proporciona a un llamador un evento que se señalizará mediante el objeto al que se llama para indicar la cancelación de una tarea.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>IObjectWithFolderEnumMode</strong></a><br/></td>
<td>Expone métodos que obtienen y establecen los modos de enumeración de un elemento analizado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithprogid"><strong>IObjectWithProgID</strong></a><br/></td>
<td>Expone métodos que proporcionan acceso al identificador de programa (ProgID) asociado a un objeto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-iobjectwithpropertykey"><strong>IObjectWithPropertyKey</strong></a><br/></td>
<td>Expone métodos para obtener y establecer la clave de propiedad.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a><br/></td>
<td>Expone métodos que obtienen o establecen los elementos seleccionados representados por una matriz de elementos de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iobjmgr"><strong>IObjMgr</strong></a><br/></td>
<td>Expone métodos que permiten a un cliente anexar o quitar un objeto de una colección de objetos administrados por un objeto de servidor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel"><strong>IOpenControlPanel</strong></a><br/></td>
<td>Expone métodos que recuperan el estado de vista del panel de control, la ruta de acceso de los elementos individuales del panel de control y que abren el panel de control en sí o un elemento individual del panel de control.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopensearchsource"><strong>IOpenSearchSource</strong></a><br/></td>
<td>Expone un método para obtener los resultados de búsqueda de un origen de datos de OpenSearch del lado cliente personalizado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ioperationsprogressdialog"><strong>IOperationsProgressDialog</strong></a><br/></td>
<td>Expone métodos para obtener, establecer y consultar un cuadro de diálogo de progreso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ipackagedebugsettings"><strong>IPackageDebugSettings</strong></a><br/></td>
<td>Permite a los desarrolladores del depurador controlar el ciclo de vida de una aplicación de la tienda Windows, como suspender o reanudar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackageexecutionstatechangenotification"><strong>IPackageExecutionStateChangeNotification</strong></a><br/></td>
<td>Habilita la recepción de notificaciones de cambio de estado de paquete durante la depuración de aplicaciones de la tienda Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a><br/></td>
<td>Expone métodos que obtienen y establecen el primario y el identificador secundario del elemento primario. Aunque <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a> se implementa normalmente en IShellItems, no es específico de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparseandcreateitem"><strong>IParseAndCreateItem</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder"><strong>IPersistFolder</strong></a><br/></td>
<td>Expone un método que inicializa objetos de carpeta de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2"><strong>IPersistFolder2</strong></a><br/></td>
<td>Expone métodos que obtienen información de los objetos de la carpeta de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3"><strong>IPersistFolder3</strong></a><br/></td>
<td>Extiende las interfaces <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder"><strong>IPersistFolder</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2"><strong>IPersistFolder2</strong></a> permitiendo que un objeto de carpeta implemente el control no predeterminado de los accesos directos a carpetas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistidlist"><strong>IPersistIDList</strong></a><br/></td>
<td>Expone métodos que se usan para conservar listas de identificadores de elementos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-ipersistserializedpropstorage"><strong>IPersistSerializedPropStorage</strong></a><br/></td>
<td>Expone métodos para conservar los datos de almacenamiento de propiedades serializadas para su uso posterior y restaurar los datos persistentes en una nueva instancia del almacén de propiedades.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-ipersistserializedpropstorage2"><strong>IPersistSerializedPropStorage2</strong></a><br/></td>
<td>Expone métodos para conservar los datos de almacenamiento de propiedades serializadas para su uso posterior y restaurar los datos persistentes en una nueva instancia del almacén de propiedades.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh707033(v=vs.85)"><strong>IPlaybackManager</strong></a><br/></td>
<td>Proporciona métodos que permiten a las aplicaciones multimedia comunicarse con el administrador de reproducción de Windows.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh707034(v=vs.85)"><strong>IPlaybackManagerEvents</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler"><strong>IPreviewHandler</strong></a><br/></td>
<td>Expone métodos para la presentación de vistas previas enriquecidas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe"><strong>IPreviewHandlerFrame</strong></a><br/></td>
<td>Permite a los controladores de vista previa pasar los métodos abreviados de teclado al host. Esta interfaz recupera una lista de métodos abreviados de teclado y dirige el host para que controle un método abreviado de teclado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals"><strong>IPreviewHandlerVisuals</strong></a><br/></td>
<td>Expone métodos para aplicar información de color y de fuente a los controladores de vista previa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewitem"><strong>IPreviewItem</strong></a><br/></td>
<td>Identifica un elemento que se mostrará en el panel de vista previa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipreviousversionsinfo"><strong>IPreviousVersionsInfo</strong></a><br/></td>
<td>Expone un método que comprueba las versiones anteriores de los archivos o carpetas del servidor, almacenadas con el fin de reversión de la tecnología de <em>instantáneas</em> proporcionada con Windows Server 2003.<br/></td>
</tr>
<tr class="odd">
<td><a href="iprivateidentitymanager.md"><strong>IPrivateIdentityManager</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="iprivateidentitymanager2.md"><strong>IPrivateIdentityManager2</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iprofferservice"><strong>IProfferService</strong></a><br/></td>
<td>Expone un mecanismo general para que los objetos ofrezcan servicios a otros objetos en el mismo host.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog"><strong>IProgressDialog</strong></a><br/></td>
<td>Expone métodos que proporcionan opciones para que una aplicación muestre un cuadro de diálogo de progreso. Esta interfaz se exporta mediante el objeto de cuadro de diálogo de progreso (CLSID_ProgressDialog). Este objeto es una manera genérica de mostrar un usuario Cómo progresa una operación. Normalmente se utiliza al eliminar, cargar, copiar, mover o descargar un gran número de archivos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp"><strong>IPublishedApp</strong></a><br/></td>
<td>Expone métodos que representan aplicaciones para agregar o quitar programas en el panel de control. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp2"><strong>IPublishedApp2</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp"><strong>IPublishedApp</strong></a> proporcionando un método de instalación adicional.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipublishingwizard"><strong>IPublishingWizard</strong></a><br/></td>
<td>Expone métodos para trabajar con el Asistente para impresión en línea, el Asistente para publicación en Web y el Asistente para agregar ubicación de red. En Windows Vista, <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipublishingwizard"><strong>IPublishingWizard</strong></a> ya no es compatible con el Asistente para publicación web o el Asistente para impresión en línea.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a><br/></td>
<td>Expone métodos que simplifican el proceso de recuperación de la información almacenada en el registro en asociación con la definición de un tipo de archivo o protocolo y su asociación con una aplicación.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iquerycancelautoplay"><strong>IQueryCancelAutoPlay</strong></a><br/></td>
<td>Expone un método que invalida mediante programación la <a href="autorun2k-intro.md">reproducción automática</a> o la <a href="autoplay.md">ejecución</a>automática. Esto le permite personalizar la ubicación y el tipo de contenido que se inicia cuando se inserta el medio.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iquerycodepage"><strong>IQueryCodePage</strong></a><br/></td>
<td>Obtiene y establece el valor numérico (identificador de la página de códigos) de la página de códigos ANSI.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue"><strong>IQueryContinue</strong></a><br/></td>
<td>Expone un método que proporciona un mecanismo simple y estándar para que los objetos consulten a un cliente para obtener permiso para continuar una operación. Los clientes de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a>, por ejemplo, deben pasar una implementación de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue"><strong>IQueryContinue</strong></a> al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-show"><strong>IUserNotification:: show</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iquerycontinuewithstatus"><strong>IQueryContinueWithStatus</strong></a><br/></td>
<td>Expone métodos que proporcionan un mecanismo estándar para que los proveedores de credenciales llamen a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iquerycontinue-querycontinue"><strong>QueryContinue</strong></a> mientras intentan conectarse a la red para determinar si deben continuar estos intentos. Los proveedores de credenciales también pueden usar esta interfaz para mostrar los mensajes al usuario al intentar establecer una conexión de red.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo"><strong>IQueryInfo</strong></a><br/></td>
<td>Expone los métodos que usa el shell para recuperar las marcas e información sobre las sugerencias de información de un elemento que reside en una implementación de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> . Las sugerencias de información se muestran normalmente dentro de un control <a href="/windows/desktop/Controls/tooltip-controls">ToolTip</a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irelateditem"><strong>IRelatedItem</strong></a><br/></td>
<td>Expone métodos que derivan elementos relacionados con relaciones específicas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer"><strong>IRemoteComputer</strong></a><br/></td>
<td>Expone un método que enumera o Inicializa una extensión de espacio de nombres cuando se invoca en un objeto remoto. Esta interfaz se usa, por ejemplo, para inicializar la carpeta virtual de impresoras remotas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iresolveshelllink"><strong>IResolveShellLink</strong></a><br/></td>
<td>Expone un método que permite a una aplicación solicitar que un objeto de carpeta de Shell resuelva un vínculo para uno de sus elementos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iresultsfolder"><strong>IResultsFolder</strong></a><br/></td>
<td>Expone métodos que contienen elementos de un objeto de datos.<br/> Un <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iresultsfolder"><strong>IResultsFolder</strong></a> es una carpeta que puede contener elementos de todo el espacio de nombres y representarlos al usuario en una sola carpeta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irunnabletask"><strong>IRunnableTask</strong></a><br/></td>
<td>Interfaz de subprocesamiento libre que puede ser expuesta por un objeto para permitir que se realicen operaciones en un subproceso en segundo plano. Por ejemplo, si el método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iextractimage-getlocation"><strong>IExtractImage:: GetLocation</strong></a> devuelve E_PENDING, la aplicación que realiza la llamada puede extraer la imagen en un subproceso en segundo plano.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-isearchboxinfo"><strong>ISearchBoxInfo</strong></a><br/></td>
<td>Expone métodos que permiten al llamador recuperar información escrita en un cuadro de búsqueda.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-isearchcontext"><strong>ISearchContext</strong></a><br/></td>
<td>Expone métodos que muestran información de personalización del canal en los enlaces de búsqueda.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory"><strong>ISearchFolderItemFactory</strong></a><br/></td>
<td>Expone métodos que crean y modifican carpetas de búsqueda. Primero se llama a los métodos set para configurar los parámetros de la búsqueda. Cuando no se llama a, se usarán los valores predeterminados. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getidlist"><strong>ISearchFolderItemFactory:: GetIDList</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getshellitem"><strong>ISearchFolderItemFactory:: GetShellItem</strong></a> devuelven las dos formas de la búsqueda especificada por estos parámetros. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-isharedbitmap"><strong>ISharedBitmap</strong></a><br/></td>
<td>Expone métodos eficientes en memoria para tener acceso a los mapas de bits. Esta interfaz se usa como un contenedor fino alrededor de los objetos HBITMAP, lo que permite que se cuenten las referencias de estos objetos y que los datos subyacentes cambien.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isharingconfigurationmanager"><strong>ISharingConfigurationManager</strong></a><br/></td>
<td>Expone métodos que establecen y recuperan información acerca de la configuración de uso compartido predeterminada de un equipo para la carpeta <strong>usuarios</strong> ( <code>C:\Users</code> ) o <strong>pública</strong> ( <code>C:\Users\Public</code> ). También expone un conjunto de métodos que permiten controlar el uso compartido de impresoras.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ishellapp"><strong>IShellApp</strong></a><br/></td>
<td>Expone métodos que proporcionan información general acerca de una aplicación a la aplicación agregar o quitar programas. No se puede usar fuera de la aplicación agregar o quitar programas. La información proporcionada por esta interfaz incluye una lista de acciones de administración admitidas y si la aplicación está instalada actualmente. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a><br/></td>
<td>Implementado por los hosts de las vistas de Shell (objetos que implementan <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>). Expone métodos que proporcionan servicios para la vista que hospeda y otros objetos que se ejecutan en el contexto de la ventana del explorador. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellchangenotify"><strong>IShellChangeNotify</strong></a><br/></td>
<td>Expone un método que notifica a una extensión de espacio de nombres del shell cuando el identificador de un elemento ha cambiado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails"><strong>IShellDetails</strong></a><br/></td>
<td>Expuesto por las carpetas de Shell para proporcionar información detallada sobre los elementos de una carpeta. Esta es la misma información que se muestra en el explorador de Windows cuando la vista de la carpeta se establece en detalles. En los sistemas Windows 2000 y versiones posteriores, <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails"><strong>IShellDetails</strong></a> se reemplaza por <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2"><strong>IShellFolder2</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit"><strong>IShellExtInit</strong></a><br/></td>
<td>Expone un método que inicializa extensiones de Shell para hojas de propiedades, menús contextuales y controladores de arrastrar y colocar (extensiones que agregan elementos a los menús contextuales durante operaciones de arrastrar y colocar no predeterminadas).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a><br/></td>
<td>Expuesto por todos los objetos de carpeta de espacio de nombres de Shell, sus métodos se utilizan para administrar carpetas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2"><strong>IShellFolder2</strong></a><br/></td>
<td>Extiende las capacidades de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a>. Sus métodos proporcionan una gran variedad de información sobre el contenido de una carpeta de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="ishellfoldersearchable.md"><strong>IShellFolderSearchable</strong></a><br/></td>
<td>Expone métodos que permiten que una extensión de Shell proporcione un espacio de nombres de búsqueda.<br/></td>
</tr>
<tr class="even">
<td><a href="ishellfoldersearchablecallback.md"><strong>IShellFolderSearchableCallback</strong></a><br/></td>
<td>Expone rutinas de devolución de llamada para supervisar el proceso de búsqueda.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellfolderviewcb"><strong>IShellFolderViewCB</strong></a><br/></td>
<td>Expone un método que permite la comunicación entre el explorador de Windows y una vista de carpeta implementada mediante el objeto de vista de carpeta del sistema (el objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> que se devuelve a través de <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a>) para que la vista de carpetas pueda recibir notificaciones de eventos y modificar su vista en consecuencia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual"><strong>IShellFolderViewDual</strong></a><br/></td>
<td>Expone métodos que modifican la vista y seleccionan los elementos de la carpeta actual. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual2"><strong>IShellFolderViewDual2</strong></a><br/></td>
<td>Expone métodos que modifican la vista y seleccionan los elementos de la carpeta actual.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual3"><strong>IShellFolderViewDual3</strong></a><br/></td>
<td>Expone métodos que modifican la vista de carpeta actual.<br/></td>
</tr>
<tr class="odd">
<td><a href="ishellfolderviewtype.md"><strong>IShellFolderViewType</strong></a><br/></td>
<td>Expone métodos que permiten que una carpeta de Shell admita vistas diferentes en su contenido (diferentes diseños jerárquicos de sus datos).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellicon"><strong>IShellIcon</strong></a><br/></td>
<td>Expone un método que obtiene un índice de icono para un objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlay"><strong>IShellIconOverlay</strong></a><br/></td>
<td>Expone métodos usados por una extensión de espacio de nombres para especificar superposiciones de iconos para los objetos que contiene.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier"><strong>IShellIconOverlayIdentifier</strong></a><br/></td>
<td>Expone métodos que controlan toda la comunicación entre los controladores de superposición de iconos y el shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedataabort"><strong>IShellImageDataAbort</strong></a><br/></td>
<td>Expone un método único que se usa para anular los procesos de <a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata"><strong>IShellImageData</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedatafactory"><strong>IShellImageDataFactory</strong></a><br/></td>
<td>Expone métodos que crean instancias de <a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata"><strong>IShellImageData</strong></a> basadas en varios orígenes de imagen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a><br/></td>
<td>Expone métodos que recuperan información sobre un elemento de Shell. <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a> son representaciones preferidas de elementos en cualquier código nuevo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a><br/></td>
<td>Extiende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> con métodos que recuperan varios valores de propiedad del elemento. <strong>IShellItem</strong> y <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a> son representaciones preferidas de elementos en cualquier código nuevo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray"><strong>IShellItemArray</strong></a><br/></td>
<td>Expone métodos que crean y manipulan matrices de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>elementos de Shell</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemfilter"><strong>IShellItemFilter</strong></a><br/></td>
<td>Expuesto por un cliente para especificar cómo filtrar la enumeración de un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>elemento de Shell</strong></a> por parte de una aplicación de servidor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemimagefactory"><strong>IShellItemImageFactory</strong></a><br/></td>
<td>Expone un método para devolver iconos o miniaturas para los elementos de Shell. Si no hay ninguna miniatura o icono disponible para el elemento solicitado, se puede proporcionar un icono por clase desde el shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemresources"><strong>IShellItemResources</strong></a><br/></td>
<td>Expone métodos para manipular y consultar recursos de elementos de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary"><strong>IShellLibrary</strong></a><br/></td>
<td>Expone métodos para crear y administrar bibliotecas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a><br/></td>
<td>Expone métodos que crean, modifican y resuelven vínculos de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a><br/></td>
<td>Expone métodos que permiten a una aplicación adjuntar bloques de datos adicionales a un <a href="/windows/desktop/shell/links">vínculo de Shell</a>. Estos métodos agregan, copian o quitan bloques de datos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu"><strong>IShellMenu</strong></a><br/></td>
<td>Expone métodos que interactúan con menús de Shell, como el menú <strong>Inicio</strong> y el menú <strong>Favoritos</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback"><strong>IShellMenuCallback</strong></a><br/></td>
<td>Una interfaz de devolución de llamada que expone un método que recibe los mensajes de una banda de menús.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext"><strong>IShellPropSheetExt</strong></a><br/></td>
<td>Expone métodos que permiten al controlador de la hoja de propiedades agregar o reemplazar páginas en la hoja de propiedades que se muestra para un objeto de archivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl/nn-shobjidl-ishellrundll"><strong>IShellRunDll</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a><br/></td>
<td>Expone métodos que presentan una vista en las ventanas del explorador de Windows o de la carpeta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a><br/></td>
<td>Extiende las capacidades de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ishellview3"><strong>IShellView3</strong></a><br/></td>
<td>Extiende las capacidades de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a> proporcionando un método para reemplazar <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2:: CreateViewWindow2</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a><br/></td>
<td>Proporciona acceso a la colección de ventanas de Shell abiertas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istartmenupinnedlist"><strong>IStartMenuPinnedList</strong></a><br/></td>
<td>Expone un método que desancla un acceso directo de aplicación desde el menú <strong>Inicio</strong> o la barra de tareas.<br/></td>
</tr>
<tr class="odd">
<td><a href="nn-shobjidl-istorageprovidercopyhook.md"><strong>IStorageProviderCopyHook</strong></a><br/></td>
<td>Expone un método que determina si el shell podrá moverse, copiar, eliminar o cambiar el nombre de una carpeta en la raíz de sincronización de un proveedor de la nube.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderhandler"><strong>IStorageProviderHandler</strong></a><br/></td>
<td>Recupera el <a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler"><strong>IStorageProviderPropertyHandler</strong></a> asociado a un archivo o carpeta específicos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler"><strong>IStorageProviderPropertyHandler</strong></a><br/></td>
<td>Proporciona una colección de propiedades asociadas a un archivo o carpeta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istreamasync"><strong>IStreamAsync</strong></a><br/></td>
<td>Expone métodos para administrar la entrada/resultados (e/s) en una secuencia asincrónica. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istreamunbufferedinfo"><strong>IStreamUnbufferedInfo</strong></a><br/></td>
<td>Expone un método que determina el tamaño del sector como ayuda para la alineación de bytes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isuspensiondependencymanager"><strong>ISuspensionDependencyManager</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflict"><strong>ISyncMgrConflict</strong></a><br/></td>
<td>Expone métodos que proporcionan información sobre un conflicto recuperado de un almacén de conflictos y permite resolver el conflicto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a><br/></td>
<td>Expone un método que obtiene la lista de IDENTIFICADOres de conflicto para un objeto de conflicto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictitems"><strong>ISyncMgrConflictItems</strong></a><br/></td>
<td>Expone métodos que obtienen datos de elementos de conflicto y el recuento de elementos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>ISyncMgrConflictPresenter</strong></a><br/></td>
<td>Expone un método que presenta un conflicto para el usuario.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictresolutionitems"><strong>ISyncMgrConflictResolutionItems</strong></a><br/></td>
<td>Expone métodos que obtienen información del elemento y el recuento de elementos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo"><strong>ISyncMgrConflictResolveInfo</strong></a><br/></td>
<td>Expone métodos que obtienen y establecen información acerca de la resolución de conflictos del administrador de sincronización.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictstore"><strong>ISyncMgrConflictStore</strong></a><br/></td>
<td>Expone métodos que permiten a un controlador proporcionar conflictos que aparecen en la carpeta conflictos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a><br/></td>
<td>Expone métodos que permiten a una aplicación o un controlador iniciar o detener una sincronización, notificar al centro de sincronización los cambios realizados en el conjunto de controladores o elementos, o notificar los cambios en los valores de propiedad.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a><br/></td>
<td>Expone métodos que enumeran a través de una matriz de estructuras <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a> . Cada una de estas estructuras proporciona información sobre un elemento que se puede sincronizar. <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a> tiene los mismos métodos que todas las interfaces de enumerador estándar: Next, SKIP, RESET y Clone.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrevent"><strong>ISyncMgrEvent</strong></a><br/></td>
<td>Expone métodos que recuperan datos de un almacén de eventos. Un almacén de eventos permite al centro de sincronización obtener un enumerador de todos los eventos del almacén, así como recuperar eventos individuales.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgreventlinkuioperation"><strong>ISyncMgrEventLinkUIOperation</strong></a><br/></td>
<td>Proporciona un método al que se llama cuando se hace clic en los vínculos de eventos en la carpeta de resultados de la sincronización.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgreventstore"><strong>ISyncMgrEventStore</strong></a><br/></td>
<td>Expone métodos que permiten a un controlador proporcionar su propio almacén de eventos y administrar sus propios eventos de sincronización, en lugar de usar el almacén de eventos del centro de sincronización predeterminado. Estos eventos se muestran en la carpeta resultados de la sincronización.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler"><strong>ISyncMgrHandler</strong></a><br/></td>
<td>Expone métodos que componen la interfaz principal implementada por un controlador de sincronización. El centro de sincronización crea una instancia del controlador a través de esta interfaz para obtener las propiedades, enumerar los elementos de sincronización y modificar el estado. El centro de sincronización crea una instancia independiente del controlador en un subproceso independiente para realizar una sincronización o una operación de la interfaz de usuario.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlercollection"><strong>ISyncMgrHandlerCollection</strong></a><br/></td>
<td>Expone métodos que proporcionan un enumerador de identificadores de controlador de sincronización y crean instancias de esos controladores de sincronización.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo"><strong>ISyncMgrHandlerInfo</strong></a><br/></td>
<td>Expone métodos que permiten que un controlador proporcione información de propiedades y estado al centro de sincronización.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a><br/></td>
<td>Expone métodos para que una aplicación se pueda registrar con el administrador de sincronización. Esto se puede lograr a través de la interfaz <a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a> o registrando directamente en el registro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrresolutionhandler"><strong>ISyncMgrResolutionHandler</strong></a><br/></td>
<td>Expone métodos que administran conflictos de sincronización. Implemente esta interfaz para construir un controlador de conflictos de sincronización. La interfaz de usuario (UI) de resolución de conflictos llamará a esta interfaz para resolver el conflicto que se presenta al usuario. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrschedulewizarduioperation"><strong>ISyncMgrScheduleWizardUIOperation</strong></a><br/></td>
<td>Expone un método que permite a un controlador mostrar el Asistente para programación de sincronización para el controlador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsessioncreator"><strong>ISyncMgrSessionCreator</strong></a><br/></td>
<td>Expone un método único a través del cual un controlador o una aplicación externa pueden notificar al centro de sincronización que ha comenzado la sincronización, así como notificar el progreso y los eventos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynccallback"><strong>ISyncMgrSyncCallback</strong></a><br/></td>
<td>Expone métodos que permiten a un proceso de sincronización informar sobre el progreso y los eventos en el centro de sincronización, o para consultar si se ha cancelado el proceso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize"><strong>ISyncMgrSynchronize</strong></a><br/></td>
<td>Expone métodos que permiten que la aplicación o el servicio registrados reciban notificaciones del administrador de sincronización.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback"><strong>ISyncMgrSynchronizeCallback</strong></a><br/></td>
<td>Expone métodos que administran el proceso de sincronización.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke"><strong>ISyncMgrSynchronizeInvoke</strong></a><br/></td>
<td>Expone métodos que permiten a una aplicación registrada invocar al administrador de sincronización para actualizar los elementos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem"><strong>ISyncMgrSyncItem</strong></a><br/></td>
<td>Expone métodos que actúan sobre y recuperan información de un solo elemento de sincronización, lo que permite a los controladores administrar los elementos de sincronización como objetos independientes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer"><strong>ISyncMgrSyncItemContainer</strong></a><br/></td>
<td>Expone métodos que proporcionan información a los controladores sobre los elementos que contienen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo"><strong>ISyncMgrSyncItemInfo</strong></a><br/></td>
<td>Expone métodos que proporcionan información de propiedades y estado para un único elemento de sincronización.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncresult"><strong>ISyncMgrSyncResult</strong></a><br/></td>
<td>Expone un método que las aplicaciones que llaman a <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a> pueden usar para obtener el resultado de una llamada a <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync"><strong>ISyncMgrControl:: StartHandlerSync</strong></a> o <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync"><strong>ISyncMgrControl:: StartItemSync</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgruioperation"><strong>ISyncMgrUIOperation</strong></a><br/></td>
<td>Expone un método a través del cual un controlador de sincronización o un elemento de sincronización puede mostrar un objeto de interfaz de usuario cuando lo solicita el centro de sincronización.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist"><strong>ITaskbarList</strong></a><br/></td>
<td>Expone métodos que controlan la barra de tareas. Permite agregar, quitar y activar elementos de forma dinámica en la barra de tareas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2"><strong>ITaskbarList2</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist"><strong>ITaskbarList</strong></a> al exponer un método para marcar una ventana como una pantalla completa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a><br/></td>
<td>Extiende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2"><strong>ITaskbarList2</strong></a> mediante la exposición de métodos que admiten la funcionalidad de botón de la barra de tareas de inicio y conmutación unificada agregada en Windows 7. Esta funcionalidad incluye representaciones en miniatura y destinos de conmutador basados en pestañas individuales en una aplicación con pestañas, barras de herramientas en miniatura, superposiciones de notificación y estado e indicadores de progreso.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist4"><strong>ITaskbarList4</strong></a><br/></td>
<td>Extiende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a> proporcionando un método que permite al llamador controlar dos valores de propiedad para la vista en miniatura y la característica de búsqueda de la pestaña.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailcache"><strong>IThumbnailCache</strong></a><br/></td>
<td>Expone métodos para una caché de miniaturas del sistema que se comparte entre las aplicaciones.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbcache/nn-thumbcache-ithumbnailcacheprimer"><strong>IThumbnailCachePrimer</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ithumbnailhandlerfactory"><strong>IThumbnailHandlerFactory</strong></a><br/></td>
<td>Expone un método para recuperar el controlador de miniaturas de un elemento. Implemente esta interfaz si desea especificar qué extractor se usa para un IDList secundario.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider"><strong>IThumbnailProvider</strong></a><br/></td>
<td>Expone un método para obtener una imagen en miniatura y está diseñado para implementarse para los controladores de miniaturas. El objeto que implementa esta interfaz también debe implementar <a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream"><strong>IInitializeWithStream</strong></a>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailsettings"><strong>IThumbnailSettings</strong></a><br/></td>
<td>Proporciona un método que permite a un proveedor de miniaturas determinar el contexto de usuario de una solicitud en miniatura.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache"><strong>IThumbnailStreamCache</strong></a><br/></td>
<td>Obtiene o establece la secuencia en miniatura. Esta interfaz es solo para uso interno y la aplicación fotos solo puede llamarla.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-itrackshellmenu"><strong>ITrackShellMenu</strong></a><br/></td>
<td>Expone métodos que amplían la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu"><strong>IShellMenu</strong></a> al proporcionar la capacidad de coordinar los botones de la barra de herramientas con un menú, así como mostrar un menú emergente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Imagetranscode/nn-imagetranscode-itranscodeimage"><strong>ITranscodeImage</strong></a><br/></td>
<td>Expone un método que permite la conversión a formatos de imagen JPEG o de mapa de bits (BMP) de cualquier tipo de imagen compatible con Windows. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferadvisesink"><strong>ITransferAdviseSink</strong></a><br/></td>
<td>Expone métodos que admiten la recopilación de estado y la información de errores.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a><br/></td>
<td>Expone métodos que crean un elemento de Shell de destino para una operación de copia o movimiento. Esta interfaz se proporciona para permitir más control sobre las operaciones de archivo proporcionando un método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferdestination-advise"><strong>ITransferDestination:: Advise</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfermediumitem"><strong>ITransferMediumItem</strong></a><br/></td>
<td>Lo utiliza un motor de copia para obtener el elemento en el que se llama a <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> para devolver un puntero a la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a> o interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a>. Estas interfaces se pueden consultar y enumerar para operaciones de copia, movimiento o eliminación.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a><br/></td>
<td>Expone métodos para manipular <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>, incluidos copiar, trasladar, reciclar y otros. Esta interfaz se ofrece para proporcionar más control sobre las operaciones de archivo proporcionando un método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-advise"><strong>ITransferSource:: Advise</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-itraydeskband"><strong>ITrayDeskBand</strong></a><br/></td>
<td>Expone métodos que muestran, ocultan y consultan deskbands.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iupdateidlist"><strong>IUpdateIDList</strong></a><br/></td>
<td>Proporciona un método para actualizar el <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> del elemento secundario de un objeto de carpeta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook"><strong>IURLSearchHook</strong></a><br/></td>
<td>Expone un método que el explorador usa para traducir la dirección de un protocolo de dirección URL desconocido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook2"><strong>IURLSearchHook2</strong></a><br/></td>
<td>Expone un método que el explorador usa para traducir la dirección de un protocolo de dirección URL desconocido mediante el uso de un objeto de contexto de búsqueda.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iuseraccountchangecallback"><strong>IUserAccountChangeCallback</strong></a><br/></td>
<td>Expone un método al que se llama cuando se cambia la imagen que representa una cuenta de usuario.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a><br/></td>
<td>Expone métodos que establecen información de notificación y, a continuación, muestran la notificación al usuario en un globo que aparece junto con el área de notificación de la barra de tareas. <br/>
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a> difiere de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a> solo en el método <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>Show</strong></a> , que agrega un parámetro adicional para que una interfaz de devolución de llamada se comunique con la notificación. De lo contrario, las dos interfaces son idénticas en el formulario y la función. CLSID_UserNotification implementa ambas versiones de <strong>Show</strong> como una sobrecarga.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a><br/></td>
<td>Expone métodos que establecen información de notificación y, a continuación, muestran la notificación al usuario en un globo que aparece junto con el área de notificación de la barra de tareas. <br/>
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a> no hereda de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a>. <strong>IUserNotification2</strong> difiere de <strong>IUserNotification</strong> solo en el método <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>Show</strong></a> , que agrega un parámetro adicional para que una interfaz de devolución de llamada se comunique con la notificación. De lo contrario, las dos interfaces son idénticas en el formulario y la función. CLSID_UserNotification implementa ambas versiones de <strong>Show</strong> como una sobrecarga.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotificationcallback"><strong>IUserNotificationCallback</strong></a><br/></td>
<td>Expone un método para controlar el acceso de un clic del mouse o del menú contextual en un globo de notificación. Se usa con <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>IUserNotification2:: show</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl/nn-shobjidl-iusetobrowseitem"><strong>IUseToBrowseItem</strong></a><br/></td>
<td>Busca el elemento que se debe usar al examinar este elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iviewstateidentityitem"><strong>IViewStateIdentityItem</strong></a><br/></td>
<td>Proporciona un elemento de persistencia canónico, un elemento para el que se recordarán las personalizaciones de vistas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/nn-shobjidl_core-ivirtualdesktopmanager"><strong>IVirtualDesktopManager</strong></a><br/></td>
<td>Expone métodos que permiten a una aplicación interactuar con grupos de ventanas que forman áreas de trabajo virtuales.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ivisualproperties"><strong>IVisualProperties</strong></a><br/></td>
<td>Expone métodos que establecen y obtienen propiedades visuales.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwebwizardextension"><strong>IWebWizardExtension</strong></a><br/></td>
<td>Extiende la interfaz <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardextension"><strong>IWizardExtension</strong></a> exponiendo métodos para establecer la dirección URL inicial de la extensión del asistente y una dirección URL específica en caso de error.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardextension"><strong>IWizardExtension</strong></a><br/></td>
<td>Lo usan los asistentes como el Asistente para publicación en Web y el Asistente para la ordenación de impresión en línea que hospedan las páginas de contenido del servidor. Esta interfaz expone métodos para especificar las páginas de extensión admitidas y navegar dentro y fuera de esas páginas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardsite"><strong>IWizardSite</strong></a><br/></td>
<td>Expone métodos usados por una extensión de Asistente para navegar por los bordes entre sí y el resto del asistente.<br/></td>
</tr>
<tr class="odd">
<td><a href="taskcompletionclient.md"><strong>TaskCompletionClient</strong></a><br/></td>
<td>Habilita la finalización de tareas. <br/></td>
</tr>
</tbody>
</table>



 

 

 