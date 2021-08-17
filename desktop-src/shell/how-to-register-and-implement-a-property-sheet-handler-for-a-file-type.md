---
description: Cuando el usuario hace clic con el botón derecho en un miembro de un tipo de archivo para mostrar la hoja de propiedades Propiedades, el Shell llama a los controladores de hoja de propiedades registrados para el tipo de archivo. Cada controlador puede agregar una página personalizada a la hoja de propiedades predeterminada.
title: Cómo registrar e implementar un controlador de hoja de propiedades para un tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce0451071ba1f454ffae9ca1444f30428909946442f5aead853e74095d0c0c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049811"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a>Cómo registrar e implementar un controlador de hoja de propiedades para un tipo de archivo

Cuando el usuario hace clic con el botón derecho en un miembro de un tipo de archivo para mostrar la hoja de propiedades Propiedades, el Shell llama a los controladores de hoja de propiedades registrados para el tipo de archivo. Cada controlador puede agregar una página personalizada a la hoja de propiedades predeterminada.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   Shell

### <a name="prerequisites"></a>Requisitos previos

-   Descripción de los menús contextuales

## <a name="instructions"></a>Instructions

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a>Paso 1: Registrar un controlador de hoja de propiedades para un tipo de archivo

Además del registro normal del Modelo de objetos componentes (COM), agregue una subclave **PropertySheetHandlers** a la **subclave shellex** de la clave ProgID de la aplicación asociada al tipo de archivo. Cree una subclave **de PropertySheetHandlers** con el nombre del controlador y establezca el valor predeterminado en el formato de cadena del GUID del identificador de clase (CLSID) del controlador de hoja de propiedades.

Para agregar más de una página a la hoja de propiedades, registre un controlador para cada página. El número máximo de páginas que puede admitir una hoja de propiedades es 32. Para registrar varios controladores, cree una clave bajo la clave **shellex** para cada controlador, con el valor predeterminado establecido en el GUID de CLSID del controlador. No es necesario crear un objeto distinto para cada controlador, lo que significa que varios controladores pueden tener el mismo valor GUID. Las páginas se mostrarán en el orden en que sus claves aparecen en **shellex**.

En el ejemplo siguiente se muestra una entrada del Registro que habilita dos controladores de extensión de hoja de propiedades para un tipo de archivo .myp de ejemplo. En este ejemplo, se usa un objeto independiente para cada página, pero también se podría usar un único objeto para ambos.

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

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a>Paso 2: Implementar un controlador de hoja de propiedades para un tipo de archivo

Además de la implementación general que se describe en Funcionamiento de los controladores de hoja de propiedades [,](propsheet-handlers.md)un controlador de hoja de propiedades para un tipo de archivo también debe tener una implementación adecuada de la interfaz [**IShellPropSheetExt.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) Solo el [**método IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) necesita una implementación sintoken. El shell no llama a [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).

El [**método IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) permite que un controlador de hoja de propiedades agregue una página a una hoja de propiedades. El método tiene dos parámetros de entrada. El primero, *lpfnAddPage*, es un puntero a una función de devolución de llamada [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) que se usa para proporcionar al Shell la información necesaria para agregar la página a la hoja de propiedades. El segundo, *lParam*, es un valor definido por Shell que el controlador no procesa. Simplemente se pasa al Shell cuando se llama a la función de devolución de llamada.

El procedimiento general para implementar [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) es el siguiente.

**Implementar el método AddPages**

1.  Asigne los valores adecuados a los miembros de una [**estructura PROPSHEETPAGE.**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) En concreto:
    -   Asigne la variable que contiene el recuento de referencias del controlador al **miembro pcRefParent.** Esta práctica impide que el objeto de controlador se descargue mientras se sigue mostrndo la hoja de propiedades.
    -   También puede implementar una función de devolución [*de llamada PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) y asignar su puntero a un **miembro pfnCallback.** Se llama a esta función cuando se crea la página y cuando está a punto de destruirse.
2.  Cree el identificador HPAGE de la página pasando la [**estructura PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) a la [**función CreatePropertySheetPage.**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea)
3.  Llame a la función a la que *apunta lpfnAddPage*. Establezca su primer parámetro en el identificador HPAGE que se creó en el paso anterior. Establezca su segundo parámetro en el *valor lParam* que el shell pasó a [**AddPages.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)
4.  Los mensajes asociados a la página se pasarán al procedimiento del cuadro de diálogo que se asignó al **miembro pfnDlgProc** de la [**estructura PROPSHEETPAGE.**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3)
5.  Si asignó una función de devolución de llamada [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) a **pfnCallback,** se llamará cuando la página esté a punto de destruirse. A continuación, el controlador puede realizar las operaciones de limpieza necesarias, como liberar las referencias que contiene.

En el ejemplo de código siguiente se muestra una implementación [**simple de AddPages.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)


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



La **variable g \_ hInst** es el identificador de instancia del archivo DLL e IDD PAGEDLG es el identificador de recurso de la plantilla de cuadro \_ de diálogo de la página. La **función PageDlgProc** es el procedimiento de cuadro de diálogo que controla los mensajes de la página. La **variable g \_ DllRefCount** contiene el recuento de referencias del objeto. El [**método AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) llama [**a AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) para incrementar el recuento. Sin embargo, la función de devolución de llamada **PageCallbackProc** libera el recuento de referencias cuando la página está a punto de destruirse.

## <a name="remarks"></a>Comentarios

Para obtener una explicación general de cómo registrar controladores de extensión de Shell, vea [Creating Shell Extension Handlers](handlers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 
