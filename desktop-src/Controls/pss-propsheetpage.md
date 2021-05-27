---
title: Estructura PROPSHEETPAGE (Prsht.h)
description: Define una página en una hoja de propiedades.
keywords:
- PropSHEETPAGE (estructura) Controles de Windows
topic_type:
- apiref
api_name:
- PROPSHEETPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/23/2021
ms.openlocfilehash: 78e1d1e4e6b4b2067083443bdb5dc4db5df59558
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550350"
---
# <a name="propsheetpage-structure"></a>PropSHEETPAGE (estructura)

Define una página en una hoja de propiedades.

## <a name="syntax"></a>Sintaxis

```cpp
typedef struct {
    DWORD      dwSize;
    DWORD      dwFlags;
    HINSTANCE  hInstance;
    union {
        LPCSTR                 pszTemplate;
        PROPSHEETPAGE_RESOURCE pResource;
    };
    union {
        HICON  hIcon;
        LPCSTR pszIcon;
    };
    LPCSTR          pszTitle;
    DLGPROC         pfnDlgProc;
    LPARAM          lParam;
    LPFNPSPCALLBACK pfnCallback;
    UINT            *pcRefParent;
    LPCTSTR         pszHeaderTitle;
    LPCTSTR         pszHeaderSubTitle;
    HANDLE          hActCtx;
    union 
    {
        HBITMAP     hbmHeader;
        LPCSTR      pszbmHeader;
    }
} PROPSHEETPAGE, *LPPROPSHEETPAGE;
```

## <a name="members"></a>Members

*dwSize* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Tamaño, en bytes, de esta estructura.

*dwFlags* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Marcas que indican qué opciones se van a usar cuando se cree la página de la hoja de propiedades. Este miembro puede ser una combinación de los valores siguientes.

| Value | Significado |
|-------|---------|
| PSP_DEFAULT | Usa el significado predeterminado para todos los miembros de la estructura. Esta marca no se admite cuando se usa el asistente de estilo Avión ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_DLGINDIRECT | Crea la página a partir de la plantilla de cuadro de diálogo en memoria a la que apunta el *miembro pResource.* La [función PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) supone que la plantilla que está en memoria no está protegida por escritura. Una plantilla de solo lectura producirá una excepción en algunas versiones de Windows. |
| PSP_HASHELP | Habilita el botón Ayuda **de la hoja** de propiedades cuando la página está activa. Esta marca no se admite cuando se usa el asistente de estilo Avión ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_HIDEHEADER | [Versión 5.80](common-control-versions.md) y posteriores. Hace que la hoja de propiedades del asistente oculte el área de encabezado cuando se selecciona la página. Si se ha proporcionado una marca de agua, se pintará en el lado izquierdo de la página. Esta marca debe establecerse para las páginas de bienvenida y finalización, y omitirse para las páginas interiores. Esta marca no se admite cuando se usa el Asistente de estilo de acrob ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_PREMATURE | [Versión 4.71](common-control-versions.md) o posterior. Hace que la página se cree cuando se crea la hoja de propiedades. Si no se especifica esta marca, la página no se creará hasta que se seleccione por primera vez. Esta marca no se admite cuando se usa el Asistente de estilo de acrob ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_RTLREADING | Invierte la dirección en la que *se muestra pszTitle.* Las ventanas normales muestran todo el texto, *incluido pszTitle,* de izquierda a derecha (LTR). Para los idiomas como hebreo o árabe que leen de derecha a izquierda (RTL), se puede reflejar una ventana y se mostrará todo el texto RTL. Si PSP_RTLREADING se establece, *pszTitle* leerá en su lugar RTL en una ventana primaria normal y LTR en una ventana primaria reflejada. |
| PSP_USECALLBACK | Llama a la función especificada por el *miembro pfnCallback* al crear o destruir la página de hoja de propiedades definida por esta estructura. |
| PSP_USEFUSIONCONTEXT | [Versión 6.0](common-control-versions.md) y posteriores. Use un contexto de activación. Para usar un contexto de activación, debe establecer esta marca y asignar el identificador de contexto de activación *a hActCtx*. Consulte los comentarios. |
| PSP_USEHEADERSUBTITLE | [Versión 5.80](common-control-versions.md) o posterior. Muestra la cadena a la que apunta el *miembro pszHeaderSubTitle* como subtítulo del área de encabezado de una página Wizard97. Para usar esta marca, también debe establecer la PSH_WIZARD97 en el *miembro dwFlags* de la estructura [PROPSHEETHEADER](pss-propsheetheader.md) asociada. La PSP_USEHEADERSUBTITLE se omite si PSP_HIDEHEADER se establece. En los asistentes de estilo Avión, el título aparece cerca de la parte superior del área de cliente. |
| PSP_USEHEADERTITLE | [Versión 5.80](common-control-versions.md) o posterior. Muestra la cadena a la que apunta el *miembro pszHeaderTitle* como título en el encabezado de una página interior Wizard97. También debe establecer la marca PSH_WIZARD97 en el *miembro dwFlags* de la estructura [PROPSHEETHEADER](pss-propsheetheader.md) asociada. La PSP_USEHEADERTITLE se omite si PSP_HIDEHEADER se establece. Esta marca no se admite cuando se usa el asistente de estilo Avión ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_USEHICON | Usa *hIcon* como icono pequeño en la pestaña de la página. Esta marca no se admite cuando se usa el asistente de estilo Avión ([PSH_AEROWIZARD](pss-propsheetheader.md)).  |
| PSP_USEICONID | Usa *pszIcon como* nombre del recurso de icono para cargar y usar como icono pequeño en la pestaña de la página. Esta marca no se admite cuando se usa el asistente de estilo Avión ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_USEREFPARENT | Mantiene el recuento de referencias especificado por el miembro *pcRefParent* durante la vigencia de la página de hoja de propiedades creada a partir de esta estructura. |
| PSP_USETITLE | Usa el *miembro pszTitle* como título del cuadro de diálogo de hoja de propiedades en lugar del título almacenado en la plantilla de cuadro de diálogo. Esta marca no se admite cuando se usa el Asistente de estilo de acrob ([PSH_AEROWIZARD](pss-propsheetheader.md)). |

*hInstance* 

Tipo: [HINSTANCE](../winprog/windows-data-types.md)

Identificador de la instancia desde la que se va a cargar un icono o un recurso de cadena. Si el *miembro pszIcon*, *pszTitle,* *pszHeaderTitle* o *pszHeaderSubTitle* identifica un recurso que se va a cargar, se debe especificar *hInstance.*

*pszTemplate* 

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Plantilla de cuadro de diálogo que se usará para crear la página. Este miembro puede especificar el identificador de recurso de la plantilla o la dirección de una cadena que especifica el nombre de la plantilla. Si se PSP_DLGINDIRECT marca en el *miembro dwFlags,* *pszTemplate* se omite. Este miembro se declara como una unión con *pResource*.

*pResource* 

Tipo: **LPCDLGTEMPLATE**

Puntero a una plantilla de cuadro de diálogo en memoria. La [función PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) supone que la plantilla no está protegida por escritura. Una plantilla de solo lectura provocará una excepción en algunas versiones de Windows. Para usar este miembro, debe establecer la marca PSP_DLGINDIRECT en el *miembro dwFlags.* Este miembro se declara como una unión con *pszTemplate*.

*hIcon* 

Tipo: [HICON](../winprog/windows-data-types.md)

Controle el icono que se usará como icono en la pestaña de la página. Si el *miembro dwFlags* no incluye PSP_USEHICON, se omite este miembro. Este miembro se declara como una unión con *pszIcon*.

*pszIcon* 

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Recurso de icono que se usará como icono en la pestaña de la página. Este miembro puede especificar el identificador del recurso de icono o la dirección de la cadena que especifica el nombre del recurso de icono. Para usar este miembro, debe establecer la marca PSP_USEICONID en el *miembro dwFlags.* Este miembro se declara como una unión con *hIcon*.

*pszTitle* 

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Título del cuadro de diálogo de hoja de propiedades. Este título invalida el título especificado en la plantilla de cuadro de diálogo. Este miembro puede especificar el identificador de un recurso de cadena o la dirección de una cadena que especifica el título. Para usar este miembro, debe establecer la marca PSP_USETITLE en el *miembro dwFlags.*

*pfnDlgProc* 

Tipo: **DLGPROC**

Puntero al procedimiento de cuadro de diálogo de la página. Dado que las páginas se crean como cuadros de diálogo modeless, el procedimiento del cuadro de diálogo no debe llamar a [la función EndDialog.](/windows/win32/api/winuser/nf-winuser-enddialog)

*lParam* 

Tipo: [LPARAM](../winprog/windows-data-types.md)

Cuando se crea la página, se pasa una copia de la estructura **PROPSHEETPAGE** de la página al procedimiento del cuadro de diálogo con [WM_INITDIALOG](../dlgbox/wm-initdialog.md) mensaje. El *miembro lParam* se proporciona para permitirle pasar información específica de la aplicación al procedimiento del cuadro de diálogo. No afecta a la propia página.

*pfnCallback* 

Tipo: **LPFNPSPCALLBACK**

Puntero a una función de devolución de llamada definida por la aplicación a la que se llama cuando se crea la página y cuando está a punto de destruirse. Para obtener más información sobre la función de devolución de llamada, vea FUNCIÓN de devolución de [llamada LPFNPSPCALLBACKA](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka). Para usar este miembro, debe establecer la marca PSP_USECALLBACK en el *miembro dwFlags.*

*pcRefParent* 

Tipo: [UINT*](../winprog/windows-data-types.md)

Puntero al valor de recuento de referencias. Para usar este miembro, debe establecer la marca PSP_USEREFPARENT en el *miembro dwFlags.*

> [!NOTE]
> Cuando se crea una página de hoja de propiedades, se incrementa el valor al que apunta *pcRefParent.* Cree implícitamente una página de hoja de propiedades estableciendo la marca PSH_PROPSHEETPAGE en el *miembro dwFlags* de [PROPSHEETHEADER](pss-propsheetheader.md) y llamando a [la función PropertySheet.](/windows/win32/api/prsht/nf-prsht-propertysheeta) Puede hacerlo explícitamente mediante la [función CreatePropertySheetPage.](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) Cuando se destruye una página de hoja de propiedades, se disminuye el valor al que apunta el *miembro pcRefParent.* Esto tiene lugar automáticamente cuando se destruye la hoja de propiedades. Puede destruir explícitamente una página de hoja de propiedades mediante la [función DestroyPropertySheetPage.](/windows/win32/api/prsht/nf-prsht-destroypropertysheetpage)

*pszHeaderTitle* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

[Versión 5.80](common-control-versions.md) o posterior. Título del área de encabezado. Para usar este miembro en el asistente de estilo Wizard97, también debe hacer lo siguiente:

* Establezca la PSP_USEHEADERTITLE en el *miembro dwFlags.*
* Establezca la PSH_WIZARD97 en el *miembro dwFlags* de la [estructura PROPSHEETHEADER de la](pss-propsheetheader.md) página.
* Asegúrese de que la PSP_HIDEHEADER en el *miembro dwFlags* no está establecida.

*pszHeaderSubTitle* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

[Versión 5.80](common-control-versions.md) o posterior. Subtítulo del área de encabezado. Para usar este miembro, debe hacer lo siguiente:

* Establezca la PSP_USEHEADERSUBTITLE en el *miembro dwFlags.*
* Establezca la PSH_WIZARD97 en el *miembro dwFlags* de la [estructura PROPSHEETHEADER de la](pss-propsheetheader.md) página.
* Asegúrese de que la PSP_HIDEHEADER en el *miembro dwFlags* no está establecida.

> [!NOTE]
> Este miembro se omite cuando se usa el asistente de estilo Avión ([PSH_AEROWIZARD](pss-propsheetheader.md))

*hActCtx* 

Tipo: [HANDLE](../winprog/windows-data-types.md)

[Versión 6.0](common-control-versions.md) o posterior. Identificador de contexto de activación. Establezca este miembro en el identificador que se devuelve al crear el contexto de activación [con CreateActCtx](/windows/win32/api/winbase/nf-winbase-createactctxa). El sistema activará este contexto antes de crear el cuadro de diálogo. No es necesario usar este miembro si usa un manifiesto global.

*hbmHeader* 

Tipo: [HBITMAP](../winprog/windows-data-types.md)

Este miembro se declara como una unión con *psheader .*

*psheadermHeader*

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Este miembro se declara como una unión con *hbmHeader*.

## <a name="remarks"></a>Comentarios

Comctl32.dll versión 6 y posteriores no son redistribuibles. Para usar Comctl32.dll versión 6 o posterior, especifique el archivo .dll en un manifiesto. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Solo aplicaciones de escritorio de Windows Vista \[\]                                    |
| Servidor mínimo compatible | Solo aplicaciones de escritorio de Windows Server 2003 \[\]                              |
| Encabezado                   | Prsht.h |
| Nombres Unicode y ANSI                   | **PROPSHEETHEADERW** (Unicode) y **PROPSHEETHEADERA** (ANSI) |