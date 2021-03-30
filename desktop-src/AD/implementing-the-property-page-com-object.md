---
title: Implementación de la página de propiedades de objeto COM
description: Una extensión de la hoja de propiedades es un objeto COM implementado como un servidor en proceso.
ms.assetid: 77a71086-1949-4828-801e-073ea5a6838b
ms.tgt_platform: multiple
keywords:
- Implementación de la página de propiedades de objeto COM
- Objeto COM de la página de propiedades, implementar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55962002ca059ad6e9c137925d1ba21ba9adc513
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904493"
---
# <a name="implementing-the-property-page-com-object"></a>Implementación de la página de propiedades de objeto COM

Una extensión de la hoja de propiedades es un objeto COM implementado como un servidor en proceso. La extensión de la hoja de propiedades debe implementar las interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) y [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) . Se crea una instancia de una extensión de la hoja de propiedades cuando el usuario muestra la hoja de propiedades de un objeto de una clase para la que se ha registrado la extensión de la hoja de propiedades en el especificador de presentación de la clase.

-   [Implementación de IShellExtInit](#implementing-ishellextinit)
-   [Implementación de IShellPropSheetExt](#implementing-ishellpropsheetext)
-   [Pasar el objeto de extensión a la página de propiedades](#passing-the-extension-object-to-the-property-page)
-   [Trabajar con el objeto de notificación](#working-with-the-notification-object)
-   [Varios](#miscellaneous)
-   [Hojas de propiedades de selección múltiple](#multiple-selection-property-sheets)
-   [Novedades de Windows Server 2003](#new-with-windows-server-2003)
-   [Temas relacionados](#related-topics)

## <a name="implementing-ishellextinit"></a>Implementación de IShellExtInit

Después de crear una instancia del objeto COM de la extensión de la hoja de propiedades, se llama al método [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) . **IShellExtInit:: Initialize** proporciona la extensión de la hoja de propiedades con un objeto [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) que contiene los datos que pertenecen al objeto de directorio que se aplica a la hoja de propiedades.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contiene datos en el formato [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) . El formato de datos **\_ DSOBJECTNAMES de CFSTR** es un **HGLOBAL** que contiene una estructura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) . La estructura **DSOBJECTNAMES** contiene los datos del objeto de directorio que se aplica a la extensión de la hoja de propiedades.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) también contiene datos en el formato [**CFSTR \_ DS \_ Display \_ Spec \_ Options**](cfstr-ds-display-spec-options.md) . El formato de datos **CFSTR \_ DS \_ Display \_ Spec \_ Options** es un **HGLOBAL** que contiene una estructura [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) . **DSDISPLAYSPECOPTIONS** contiene datos de configuración para su uso por la extensión.

Si se devuelve un valor distinto de **S \_ OK** de [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), no se muestra la hoja de propiedades.

No se usan los parámetros *pidlFolder* y *HkeyProgID* del método [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) .

La extensión puede guardar el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) incrementando el recuento de referencias de **IDataObject**. Esta interfaz se debe liberar cuando ya no se necesite.

## <a name="implementing-ishellpropsheetext"></a>Implementación de IShellPropSheetExt

Después de que [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) devuelva, se llama al método [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) . La extensión de la hoja de propiedades debe agregar la página o páginas durante este método. Una página de propiedades se crea rellenando una estructura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) y pasando después esta estructura a la función [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . A continuación, se agrega la página de propiedades a la hoja de propiedades mediante una llamada a la función de devolución de llamada que se pasa a **IShellPropSheetExt:: AddPages** en el parámetro *lpfnAddPage* .

Si se devuelve un valor distinto de **S \_ OK** de [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages), no se muestra la hoja de propiedades.

Si no se requiere la extensión de la hoja de propiedades para agregar páginas a la hoja de propiedades, no debe llamar a la función de devolución de llamada que se pasa a [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) en el parámetro *lpfnAddPage* .

No se usa el método [**IShellPropSheetExt:: ReplacePage**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) .

## <a name="passing-the-extension-object-to-the-property-page"></a>Pasar el objeto de extensión a la página de propiedades

El objeto de extensión de la hoja de propiedades es independiente de la página de propiedades. En muchos casos, es conveniente poder usar el objeto de extensión u otro objeto de la página de propiedades. Para ello, establezca el miembro **lParam** de la estructura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) en el puntero de objeto. A continuación, la página de propiedades puede recuperar este valor cuando procesa el mensaje de [**\_ INITDIALOG de WM**](../dlgbox/wm-initdialog.md) . En el caso de una página de propiedades, el parámetro *lParam* del mensaje de **\_ INITDIALOG de WM** es un puntero a la estructura **PROPSHEETPAGE** . Recupere el puntero de objeto convirtiendo el *lParam* del mensaje de **\_ INITDIALOG de WM** en un puntero de **PROPSHEETPAGE** y, a continuación, recuperando el miembro **lParam** de la estructura **PROPSHEETPAGE** .

En el ejemplo de código de C++ siguiente se muestra cómo pasar un objeto a una página de propiedades.


```C++
case WM_INITDIALOG:
    {
        LPPROPSHEETPAGE pPage = (LPPROPSHEETPAGE)lParam;

        if(NULL != pPage)
        {
            CPropSheetExt *pPropSheetExt;
            pPropSheetExt = (CPropSheetExt*)pPage->lParam;

            if(pPropSheetExt)
            {
                return pPropSheetExt>OnInitDialog(wParam, lParam);
            }
        }
    }
    break;
```



Tenga en cuenta que después de llamar a [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) , la hoja de propiedades liberará el objeto de extensión de la hoja de propiedades y nunca lo volverá a usar. Esto significa que el objeto de extensión se eliminaría antes de que se muestre la página de propiedades. Cuando la página intente obtener acceso al puntero del objeto, se habrá liberado la memoria y el puntero no será válido. Para corregirlo, incremente el recuento de referencias del objeto de extensión cuando se agregue la página y, a continuación, libere el objeto cuando se destruya el cuadro de diálogo de la página de propiedades. Esto crea otro problema porque el cuadro de diálogo Página de propiedades no se crea hasta la primera vez que se muestra la página. Si el usuario nunca selecciona la página de la extensión, la página nunca se crea ni se destruye. Esto hace que el objeto de extensión no se libere nunca, por lo que se produce una fuga de memoria. Para evitar esto, implemente una función de devolución de llamada de página de propiedades. Para ello, agregue la marca **PSP \_ USECALLBACK** al miembro **DwFlags** de la estructura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) y establezca el miembro **pfnCallback** de la estructura **PROPSHEETPAGE** en la dirección de la función [**PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) implementada. Cuando la función **PropSheetPageProc** recibe la notificación de **\_ versión PSPCB** , el parámetro *ppsp* del **PropSheetPageProc** contiene un puntero a la estructura **PROPSHEETPAGE** . El miembro **lParam** de la estructura **PROPSHEETPAGE** contiene el puntero de extensión que se puede usar para liberar el objeto.

En el ejemplo de código de C++ siguiente se muestra cómo liberar un objeto de extensión.


```C++
UINT CALLBACK CPropSheetExt::PageCallbackProc(  HWND hWnd,
                                                UINT uMsg,
                                                LPPROPSHEETPAGE ppsp)
{
    switch(uMsg)
    {
    case PSPCB_CREATE:
        // Must return TRUE to enable the page to be created.
        return TRUE;

    case PSPCB_RELEASE:
        {
            /*
            Release the object. This is called even if the page dialog box was 
            never actually created.
            */
            CPropSheetExt *pPropSheetExt = (CPropSheetExt*)ppsp->lParam;

            if(pPropSheetExt)
            {
                pPropSheetExt->Release();
            }
        }
        break;
    }

    return FALSE;
}
```



## <a name="working-with-the-notification-object"></a>Trabajar con el objeto de notificación

Dado que las páginas de extensión de la hoja de propiedades se muestran en una hoja de propiedades creada por un componente desconocido para la extensión, es necesario utilizar un "administrador" para controlar la transferencia de datos entre las páginas de extensión y la hoja de propiedades. Este "administrador" se denomina objeto de notificación. El objeto de notificación funciona como un moderador entre las páginas individuales y la hoja de propiedades.

Cuando se inicializa el objeto de extensión de la hoja de propiedades, la extensión debe crear un objeto de notificación llamando a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj), pasando los [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtenidos de [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) y el nombre del objeto de directorio. No es necesario incrementar el recuento de referencias de la interfaz **IDataObject** , ya que el objeto de notificación creado por la función **ADsPropCreateNotifyObj** lo hará. El identificador de objeto de notificación proporcionado por **ADsPropCreateNotifyObj** debe guardarse para su uso posterior. Se puede llamar a **ADsPropCreateNotifyObj** durante **IShellExtInit:: Initialize** o [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages). Cuando se cierra la extensión de la hoja de propiedades, debe enviar un mensaje de [**\_ salida de \_ notificación \_ de WM ADSPROP**](wm-adsprop-notify-exit.md) al objeto de notificación. Esto hace que el objeto de notificación se destruya a sí mismo. Esto se recomienda cuando la función [**PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) recibe la notificación **de \_ versión de PSPCB** .

La extensión de la hoja de propiedades puede obtener datos además de los proporcionados por el formato del portapapeles de [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) mediante una llamada a [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo). Una de las ventajas de usar **ADsPropGetInitInfo** es que proporciona un objeto [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) que se usa para trabajar mediante programación con el objeto de directorio.

> [!Note]  
> A diferencia de la mayoría de los métodos y funciones COM, [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) no incrementa el recuento de referencias para el objeto [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) . No se debe liberar **IDirectoryObject** a menos que primero se incremente el recuento de referencias manualmente.

 

Cuando se crea por primera vez la página de propiedades, la extensión debe registrar la página con el objeto de notificación llamando a [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) con el identificador de ventana de la página.

[**ADsPropCheckIfWritable**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcheckifwritable) es una función de utilidad que puede usar la extensión de la hoja de propiedades para determinar si se puede escribir una propiedad.

## <a name="miscellaneous"></a>Varios

El identificador de la página de propiedades se pasa al procedimiento del cuadro de diálogo de la página. La hoja de propiedades es el elemento primario directo de la página de propiedades, por lo que se puede obtener el identificador de la hoja de propiedades mediante una llamada a la función [**GetParent**](/windows/win32/api/winuser/nf-winuser-getparent) con el identificador de la página de propiedades.

Cuando el contenido de la página de extensión cambia, la extensión debe usar la macro [**PropSheet \_ Changed**](/windows/win32/api/prsht/nf-prsht-propsheet_changed) para notificar a la hoja de propiedades los cambios. A continuación, la hoja de propiedades habilitará el botón aplicar.

## <a name="multiple-selection-property-sheets"></a>Multiple-Selection hojas de propiedades

Con Windows Server 2003 y los sistemas operativos posteriores, los complementos de MMC administrativos Active Directory admiten extensiones de la hoja de propiedades para varios objetos de directorio. Estas hojas de propiedades se muestran cuando se ven las propiedades de más de un elemento a la vez. La principal diferencia entre una extensión de hoja de propiedades de selección única y una extensión de la hoja de propiedades de selección múltiple es que la estructura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) proporcionada por el formato del portapapeles de [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) en [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) contendrá más de una estructura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .

Cuando se crea el objeto de notificación, una extensión de la hoja de propiedades de selección múltiple debe pasar un nombre único proporcionado por el complemento en lugar de un nombre creado por la extensión. Para obtener el nombre único, solicite el formato del portapapeles de [**\_ \_ MULTISELECTPROPPAGE de CFSTR DS**](cfstr-ds-multiselectproppage.md) de la [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtenida de [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize). Estos datos son un **HGLOBAL** que contiene una cadena Unicode terminada en null que es el nombre único. Este nombre único se pasa a la función [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) para crear el objeto de notificación. La función de ejemplo **CreateADsNotificationObject** del [código de ejemplo para la implementación del objeto com de la hoja de propiedades](example-code-for-implementation-of-the-property-sheet-com-object.md) muestra cómo hacerlo correctamente, así como la compatibilidad con versiones anteriores del complemento que no admiten hojas de propiedades de selección múltiple.

En el caso de las hojas de propiedades de selección múltiple, el sistema solo se enlaza al primer objeto de la matriz [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) . Por este motivo, [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) solo proporciona los atributos [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) y grabable para el primer objeto de la matriz. Los demás objetos de la matriz no están enlazados a.

Una extensión de la hoja de propiedades de selección múltiple se registra en el atributo [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .

## <a name="new-with-windows-server-2003"></a>Novedades de Windows Server 2003

Las siguientes características son nuevas en Windows Server 2003.

Si la página de propiedades encuentra un error, se puede llamar a [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) con los datos de error adecuados. **ADsPropSendErrorMessage** almacenará todos los mensajes de error en una cola. Estos mensajes se mostrarán la próxima vez que se llame a [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) . Cuando **ADsPropShowErrorDialog** devuelve, se eliminan los mensajes en cola.

Windows Server 2003 presenta la función [**ADsPropSetHwndWithTitle**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwndwithtitle) . Esta función es similar a [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd), pero incluye el título de la página. Esto permite que el cuadro de diálogo de error que muestra [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) proporcione datos más útiles al usuario. Si la extensión de la hoja de propiedades utiliza la función **ADsPropShowErrorDialog** , la extensión debe usar **ADsPropSetHwndWithTitle** en lugar de **ADsPropSetHwnd**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Código de ejemplo para la implementación del objeto COM de la hoja de propiedades](example-code-for-implementation-of-the-property-sheet-com-object.md)
</dt> </dl>

 

 