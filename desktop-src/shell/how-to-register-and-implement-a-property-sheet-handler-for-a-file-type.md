---
description: Cuando el usuario hace clic con el botón secundario en un miembro de un tipo de archivo para mostrar la hoja de propiedades propiedades, el shell llama a los controladores de hoja de propiedades que se registran para el tipo de archivo. Cada controlador puede Agregar una página personalizada a la hoja de propiedades predeterminada.
title: Cómo registrar e implementar un controlador de hoja de propiedades para un tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cf54886f7819fa910da23393c6db488ddfee72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997700"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a>Cómo registrar e implementar un controlador de hoja de propiedades para un tipo de archivo

Cuando el usuario hace clic con el botón secundario en un miembro de un tipo de archivo para mostrar la hoja de propiedades propiedades, el shell llama a los controladores de hoja de propiedades que se registran para el tipo de archivo. Cada controlador puede Agregar una página personalizada a la hoja de propiedades predeterminada.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   Shell

### <a name="prerequisites"></a>Requisitos previos

-   Descripción de los menús contextuales

## <a name="instructions"></a>Instrucciones

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a>Paso 1: registrar un controlador de la hoja de propiedades para un tipo de archivo

Además del registro de modelo de objetos componentes (COM) normal, agregue una subclave **PropertySheetHandlers** a la subclave **shellex** de la clave ProgID de la aplicación asociada al tipo de archivo. Cree una subclave de **PropertySheetHandlers** con el nombre del controlador y establezca el valor predeterminado en la forma de cadena del GUID del identificador de clase (CLSID) del controlador de la hoja de propiedades.

Para agregar más de una página a la hoja de propiedades, registre un controlador para cada página. El número máximo de páginas que puede admitir una hoja de propiedades es 32. Para registrar varios controladores, cree una clave en la clave **shellex** para cada controlador, con el valor predeterminado establecido en el GUID de CLSID del controlador. No es necesario crear un objeto distinto para cada controlador, lo que significa que varios controladores pueden tener el mismo valor de GUID. Las páginas se mostrarán en el orden en que aparecen en **shellex**.

En el ejemplo siguiente se muestra una entrada del registro que habilita dos controladores de extensión de la hoja de propiedades para un tipo de archivo. MYP de ejemplo. En este ejemplo, se usa un objeto independiente para cada página, pero también se puede usar un único objeto para ambos.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {Page 1 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet1.dll
            ThreadingModel = Apartment
      {Page 2 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet2.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         PropertySheetHandlers
            MyPropSheet1
               (Default) = {Page1 Property Sheet Handler CLSID GUID}
            MyPropSheet2
               (Default) = {Page2 Property Sheet Handler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a>Paso 2: implementar un controlador de hoja de propiedades para un tipo de archivo

Además de la implementación general que se describe en [Cómo funcionan los controladores de hoja de propiedades](propsheet-handlers.md), un controlador de hoja de propiedades para un tipo de archivo también debe tener una implementación adecuada de la interfaz [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) . Solo el método [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) necesita una implementación que no sea de token. El shell no llama a [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).

El método [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) permite que un controlador de hoja de propiedades agregue una página a una hoja de propiedades. El método tiene dos parámetros de entrada. El primero, *lpfnAddPage*, es un puntero a una función de devolución de llamada [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) que se usa para proporcionar al shell la información necesaria para agregar la página a la hoja de propiedades. El segundo, *lParam*, es un valor definido por el shell que no es procesado por el controlador. Simplemente se devuelve al shell cuando se llama a la función de devolución de llamada.

El procedimiento general para implementar [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) es el siguiente.

**Implementar el método AddPages**

1.  Asigne los valores adecuados a los miembros de una estructura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) . En concreto:
    -   Asigne la variable que contiene el recuento de referencias del controlador al miembro **pcRefParent** . Esta práctica evita que el objeto de controlador se descargue mientras la hoja de propiedades todavía se está mostrando.
    -   También puede implementar una función de devolución de llamada [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) y asignar su puntero a un miembro **pfnCallback** . Se llama a esta función cuando se crea la página y cuando está a punto de ser destruida.
2.  Cree el identificador de HPAGE de la página pasando la estructura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) a la función [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) .
3.  Llame a la función a la que apunta *lpfnAddPage*. Establezca su primer parámetro en el identificador de HPAGE que se creó en el paso anterior. Establezca el segundo parámetro en el valor *lParam* que se pasó a [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) por el shell.
4.  Los mensajes asociados a la página se pasarán al procedimiento del cuadro de diálogo que se asignó al miembro **pfnDlgProc** de la estructura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) .
5.  Si ha asignado una función de devolución de llamada [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) a **pfnCallback**, se le llamará cuando la página esté a punto de ser destruida. Después, el controlador puede realizar las operaciones de limpieza necesarias, como liberar las referencias que contiene.

En el ejemplo de código siguiente se muestra una implementación de [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) simple.


```C++
STDMETHODIMP CShellPropSheetExt::AddPages(LPFNADDPROPSHEETPAGE, lpfnAddPage, LPARAM lParam)
{
    PROPSHEETPAGE  psp;
    HPROPSHEETPAGE hPage;

    psp.dwSize        = sizeof(psp);
    psp.dwFlags       = PSP_USEREFPARENT | PSP_USETITLE | PSP_USECALLBACK;
    psp.hInstance     = g_hInst;
    psp.pszTemplate   = MAKEINTRESOURCE(IDD_PAGEDLG);
    psp.hIcon         = 0;
    psp.pszTitle      = TEXT("Extension Page");
    psp.pfnDlgProc    = (DLGPROC)PageDlgProc;
    psp.pcRefParent   = &g_DllRefCount;
    psp.pfnCallback   = PageCallbackProc;
    psp.lParam        = (LPARAM)this;

    hPage = CreatePropertySheetPage(&psp);
            
    if(hPage) 
    {
        if(lpfnAddPage(hPage, lParam))
        {
            this->AddRef();
            return S_OK;
        }
        else
        {
            DestroyPropertySheetPage(hPage);
        }
    }
    else
    {
        return E_OUTOFMEMORY;
    }
    return E_FAIL;
}
```



La variable **g \_ HINST** es el identificador de instancia de la dll y IDD \_ PAGEDLG es el identificador de recurso de la plantilla de cuadro de diálogo de la página. La función **PageDlgProc** es el procedimiento de cuadro de diálogo que controla los mensajes de la página. La variable **g \_ DllRefCount** contiene el recuento de referencias del objeto. El método [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) llama a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) para incrementar el recuento. Sin embargo, el recuento de referencias se libera mediante la función de devolución de llamada, **PageCallbackProc**, cuando la página está a punto de ser destruida.

## <a name="remarks"></a>Observaciones

Para obtener información general sobre cómo registrar controladores de extensión de Shell, vea [crear controladores de extensión de Shell](handlers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 
