---
title: Implementar el objeto COM de la página de propiedades
description: Una extensión de hoja de propiedades es un objeto COM implementado como un servidor en proceso.
ms.assetid: 77a71086-1949-4828-801e-073ea5a6838b
ms.tgt_platform: multiple
keywords:
- Implementar el objeto COM de la página de propiedades
- Objeto COM de la página de propiedades, implementar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504c27bcf4703bb49a3e8620c287c30ae9017ab6e65345d003f2acb6c9b544e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187616"
---
# <a name="implementing-the-property-page-com-object"></a>Implementar el objeto COM de la página de propiedades

Una extensión de hoja de propiedades es un objeto COM implementado como un servidor en proceso. La extensión de hoja de propiedades debe implementar las interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) [**e IShellPropSheetExt.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) Se crea una instancia de una extensión de hoja de propiedades cuando el usuario muestra la hoja de propiedades de un objeto de una clase para la que se ha registrado la extensión de hoja de propiedades en el especificador de presentación de la clase .

-   [Implementación de IShellExtInit](#implementing-ishellextinit)
-   [Implementación de IShellPropSheetExt](#implementing-ishellpropsheetext)
-   [Pasar el objeto de extensión a la página de propiedades](#passing-the-extension-object-to-the-property-page)
-   [Trabajar con el objeto de notificación](#working-with-the-notification-object)
-   [Varios](#miscellaneous)
-   [Hojas de propiedades de selección múltiple](#multiple-selection-property-sheets)
-   [Novedades de Windows Server 2003](#new-with-windows-server-2003)
-   [Temas relacionados](#related-topics)

## <a name="implementing-ishellextinit"></a>Implementación de IShellExtInit

Después de crear una instancia del objeto COM de extensión de hoja de propiedades, se llama al método [**IShellExtInit::Initialize.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) **IShellExtInit::Initialize** proporciona la extensión de hoja de propiedades con un objeto [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) que contiene datos que pertenecen al objeto de directorio al que se aplica la hoja de propiedades.

[**IDataObject contiene**](/windows/win32/api/objidl/nn-objidl-idataobject) datos en el formato [**CFSTR \_ DSOBJECTNAMES.**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) El **formato de datos \_ CFSTR DSOBJECTNAMES** es **un HGLOBAL** que contiene una [**estructura DSOBJECTNAMES.**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) La **estructura DSOBJECTNAMES** contiene datos de objeto de directorio a los que se aplica la extensión de hoja de propiedades.

[**IDataObject también**](/windows/win32/api/objidl/nn-objidl-idataobject) contiene datos en el formato [**CFSTR \_ DS DISPLAY SPEC \_ \_ \_ OPTIONS.**](cfstr-ds-display-spec-options.md) El **formato de datos \_ CFSTR DS \_ DISPLAY SPEC \_ \_ OPTIONS** es **un HGLOBAL** que contiene una [**estructura DSDISPLAYSPECOPTIONS.**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) **DSDISPLAYSPECOPTIONS** contiene datos de configuración para su uso por parte de la extensión.

Si se devuelve un valor distinto de **S \_ OK** desde [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), no se muestra la hoja de propiedades.

No se usan los parámetros *pidlFolder* y *hkeyProgID* del método [**IShellExtInit::Initialize.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)

La extensión puede guardar el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) incrementando el recuento de referencias de **IDataObject**. Esta interfaz debe liberarse cuando ya no sea necesario.

## <a name="implementing-ishellpropsheetext"></a>Implementación de IShellPropSheetExt

Una [**vez que se devuelve IShellExtInit::Initialize,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) se llama al método [**IShellPropSheetExt::AddPages.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) La extensión de hoja de propiedades debe agregar la página o páginas durante este método. Una página de propiedades se crea rellenando una [**estructura PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) y, a continuación, pasando esta estructura a la [**función CreatePropertySheetPage.**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) A continuación, la página de propiedades se agrega a la hoja de propiedades mediante una llamada a la función de devolución de llamada pasada a **IShellPropSheetExt::AddPages** en el *parámetro lpfnAddPage.*

Si se devuelve un valor distinto de **S \_ OK** desde [**IShellPropSheetExt::AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages), no se muestra la hoja de propiedades.

Si la extensión de hoja de propiedades no es necesaria para agregar ninguna página a la hoja de propiedades, no debe llamar a la función de devolución de llamada pasada a [**IShellPropSheetExt::AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) en el *parámetro lpfnAddPage.*

No [**se usa el método IShellPropSheetExt::ReplacePage.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage)

## <a name="passing-the-extension-object-to-the-property-page"></a>Pasar el objeto de extensión a la página de propiedades

El objeto de extensión de hoja de propiedades es independiente de la página de propiedades. En muchos casos, es conveniente poder usar el objeto de extensión, o cualquier otro objeto, desde la página de propiedades. Para ello, establezca el miembro **lParam** de [**la estructura PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) en el puntero de objeto. A continuación, la página de propiedades puede recuperar este valor cuando procesa el [**\_ mensaje WM INITDIALOG.**](../dlgbox/wm-initdialog.md) Para una página de propiedades, el *parámetro lParam* del **mensaje WM \_ INITDIALOG** es un puntero a la **estructura PROPSHEETPAGE.** Recupere el puntero de objeto al convertir *el elemento lParam* del mensaje **WM \_ INITDIALOG** en un puntero **PROPSHEETPAGE** y, a continuación, recuperar el miembro **lParam** de la **estructura PROPSHEETPAGE.**

En el siguiente ejemplo de código de C++ se muestra cómo pasar un objeto a una página de propiedades.


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



Tenga en cuenta que después de llamar a [**IShellPropSheetExt::AddPages,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) la hoja de propiedades liberará el objeto de extensión de hoja de propiedades y nunca lo volverá a usar. Esto significa que el objeto de extensión se eliminaría antes de que se muestre la página de propiedades. Cuando la página intenta acceder al puntero de objeto, se habrá liberando la memoria y el puntero no será válido. Para corregirlo, incremente el recuento de referencias para el objeto de extensión cuando se agrega la página y, a continuación, suelte el objeto cuando se destruya el cuadro de diálogo de la página de propiedades. Esto crea otro problema porque el cuadro de diálogo de la página de propiedades no se crea hasta la primera vez que se muestra la página. Si el usuario nunca selecciona la página de extensión, la página nunca se crea y destruye. Esto da como resultado que el objeto de extensión nunca se libera, por lo que se produce una pérdida de memoria. Para evitarlo, implemente una función de devolución de llamada de página de propiedades. Para ello, agregue la marca **\_ USECALLBACK** de PSP al miembro **dwFlags** de la estructura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) y establezca el miembro **pfnCallback** de la estructura **PROPSHEETPAGE** en la dirección de la [**función PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) implementada. Cuando la **función PropSheetPageProc** recibe la notificación **PSPCB \_ RELEASE,** el parámetro *ppsp* de **PropSheetPageProc** contiene un puntero a la **estructura PROPSHEETPAGE.** El **miembro lParam** de la **estructura PROPSHEETPAGE** contiene el puntero de extensión que se puede usar para liberar el objeto.

En el siguiente ejemplo de código de C++ se muestra cómo liberar un objeto de extensión.


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

Dado que las páginas de extensión de hoja de propiedades se muestran dentro de una hoja de propiedades creada por un componente desconocido para la extensión, es necesario usar un "administrador" para controlar la transferencia de datos entre las páginas de extensión y la hoja de propiedades. Este "administrador" se denomina el objeto de notificación. El objeto de notificación funciona como un moderador entre las páginas individuales y la hoja de propiedades.

Cuando se inicializa el objeto de extensión de hoja de propiedades, la extensión debe crear un objeto de notificación llamando a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj), pasando el [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtenido de [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) y el nombre del objeto de directorio. No es necesario incrementar el recuento de referencias de la interfaz **IDataObject,** ya que el objeto de notificación creado por la función **ADsPropCreateNotifyObj** lo hará. El identificador de objeto de notificación proporcionado por **ADsPropCreateNotifyObj** debe guardarse para su uso posterior. **Se puede llamar a ADsPropCreateNotifyObj** durante **IShellExtInit::Initialize** o [**IShellPropSheetExt::AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages). Cuando se cierra la extensión de hoja de propiedades, debe enviar un mensaje [**\_ WM ADSPROP NOTIFY \_ \_ EXIT**](wm-adsprop-notify-exit.md) al objeto de notificación. Esto hace que el objeto de notificación se destruya a sí mismo. Esto se hace mejor cuando la [**función PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) recibe la **notificación DE LANZAMIENTO \_ de PSPCB.**

La extensión de hoja de propiedades puede obtener datos además de los proporcionados por el formato del Portapapeles [**\_ CFSTR DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) llamando [**a ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo). Una de las ventajas de **usar ADsPropGetInitInfo** es que proporciona un objeto [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) que se usa para trabajar mediante programación con el objeto de directorio.

> [!Note]  
> A diferencia de la mayoría de los métodos y funciones COM, [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) no incrementa el recuento de referencias para el [**objeto IDirectoryObject.**](/windows/desktop/api/iads/nn-iads-idirectoryobject) **IDirectoryObject no** debe liberarse a menos que el recuento de referencias se incremente manualmente primero.

 

Cuando se crea la página de propiedades por primera vez, la extensión debe registrar la página con el objeto de notificación llamando [**a ADsPropSetHwnd con**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) el identificador de ventana de la página.

[**ADsPropCheckIfWritable**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcheckifwritable) es una función de utilidad que la extensión de hoja de propiedades puede usar para determinar si se puede escribir una propiedad.

## <a name="miscellaneous"></a>Varios

El identificador de la página de propiedades se pasa al procedimiento del cuadro de diálogo de página. La hoja de propiedades es el elemento primario directo de la página de propiedades, por lo que el identificador de la hoja de propiedades se puede obtener llamando a la función [**GetParent**](/windows/win32/api/winuser/nf-winuser-getparent) con el identificador de página de propiedades.

Cuando cambia el contenido de la página de extensión, la extensión debe usar la macro [**PropSheet \_ Changed**](/windows/win32/api/prsht/nf-prsht-propsheet_changed) para notificar los cambios a la hoja de propiedades. A continuación, la hoja de propiedades habilitará el botón Aplicar.

## <a name="multiple-selection-property-sheets"></a>Multiple-Selection de propiedades

Con Windows Server 2003 y sistemas operativos posteriores, Active Directory complementos MMC administrativos admiten extensiones de hoja de propiedades para varios objetos de directorio. Estas hojas de propiedades se muestran cuando las propiedades se ven para más de un elemento a la vez. La principal diferencia entre una extensión de hoja de propiedades de selección única y una extensión de hoja de propiedades de selección múltiple es que la estructura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) proporcionada por el formato del Portapapeles [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) en [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) contendrá más de una estructura [**DSOBJECT.**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)

Cuando se crea el objeto de notificación, una extensión de hoja de propiedades de selección múltiple debe pasar un nombre único proporcionado por el complemento en lugar de un nombre creado por la extensión. Para obtener el nombre único, solicite el formato del Portapapeles [**\_ \_ MULTISELECTPROPPAGE de CFSTR DS**](cfstr-ds-multiselectproppage.md) del [**objeto IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtenido de [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize). Estos datos son **un HGLOBAL** que contiene una cadena Unicode terminada en NULL que es el nombre único. A continuación, este nombre único se pasa a la función [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) para crear el objeto de notificación. La función de ejemplo **CreateADsNotificationObject** del código de ejemplo para la implementación del objeto [COM](example-code-for-implementation-of-the-property-sheet-com-object.md) de hoja de propiedades muestra cómo hacerlo correctamente, además de ser compatible con versiones anteriores del complemento que no admiten hojas de propiedades de selección múltiple.

Para las hojas de propiedades de selección múltiple, el sistema solo se enlaza al primer objeto de la [**matriz DSOBJECT.**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) Por este problema, [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) solo proporciona los atributos [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) y write-able para el primer objeto de la matriz. Los demás objetos de la matriz no están enlazados a .

Se registra una extensión de hoja de propiedades de selección múltiple en el [**atributo adminMultiselectPropertyPages.**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages)

## <a name="new-with-windows-server-2003"></a>Novedades de Windows Server 2003

Las siguientes características son nuevas con Windows Server 2003.

Si la página de propiedades encuentra un error, se puede llamar [**a ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) con los datos de error adecuados. **ADsPropSendErrorMessage almacenará** todos los mensajes de error en una cola. Estos mensajes se mostrarán la próxima vez que se llame [**a ADsPropShowErrorDialog.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) Cuando **se devuelve ADsPropShowErrorDialog,** se eliminan los mensajes en cola.

Windows Server 2003 presenta la [**función ADsPropSetHwndWithTitle.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwndwithtitle) Esta función es similar [**a ADsPropSetHwnd,**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)pero incluye el título de la página. Esto permite que el cuadro de diálogo de error mostrado por [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) proporcione datos más útiles al usuario. Si la extensión de hoja de propiedades usa la función **ADsPropShowErrorDialog,** la extensión debe usar **ADsPropSetHwndWithTitle** en lugar de **ADsPropSetHwnd**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Código de ejemplo para la implementación del objeto COM de hoja de propiedades](example-code-for-implementation-of-the-property-sheet-com-object.md)
</dt> </dl>

 

 