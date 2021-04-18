---
title: Estructura PROPSHEETHEADER (Prsht. h)
description: Define el marco y las páginas de una hoja de propiedades.
keywords:
- PROPSHEETHEADER estructura de Windows (controles)
topic_type:
- apiref
api_name:
- PROPSHEETHEADER
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/23/2021
ms.openlocfilehash: 90a11ff727b491a1801f8071e28c39a3a6594408
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105721563"
---
# <a name="propsheetheader--structure"></a>Estructura PROPSHEETHEADER

Define el marco y las páginas de una hoja de propiedades.

## <a name="syntax"></a>Sintaxis

```cpp
typedef struct {
    DWORD      dwSize;
    DWORD      dwFlags;
    HWND       hwndParent;
    HINSTANCE  hInstance;
    union {
        HICON   hIcon;
        LPCTSTR pszIcon;
    };
    LPCTSTR  pszCaption;
    UINT     nPages;
    union {
        UINT    nStartPage;
        LPCTSTR pStartPage;
    };
    union {
        LPCPROPSHEETPAGE ppsp;
        HPROPSHEETPAGE   *phpage;
    };
    PFNPROPSHEETCALLBACK pfnCallback;
    union {
        HBITMAP hbmWatermark;
        LPCTSTR pszbmWatermark;
    };
    HPALETTE  hplWatermark;
    union {
        HBITMAP hbmHeader;
        LPCSTR  pszbmHeader;
    };
} PROPSHEETHEADER, *LPPROPSHEETHEADER;
```

## <a name="members"></a>Miembros

*dwSize* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Tamaño, en bytes, de esta estructura. El administrador de la hoja de propiedades utiliza este miembro para determinar la versión de la estructura **PROPSHEETHEADER** que está usando. Para obtener más información, vea la sección Notas.

*dwFlags* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Marcas que indican qué opciones se van a usar cuando se cree la página de la hoja de propiedades. Este miembro puede ser una combinación de los valores siguientes.

| Value | Significado |
|-------|---------|
| PSH_DEFAULT (0x00000000) | Utiliza el significado predeterminado para todos los miembros de estructura y crea una hoja de propiedades normal. Esta marca tiene un valor de cero y no se combina con otras marcas. |
| PSH_AEROWIZARD (0x00004000) | [Versión 6,00](common-control-versions.md) y versiones posteriores. Crea una hoja de propiedades del asistente que usa el estilo Aero. También se debe establecer la marca PSH_WIZARD. Se debe usar el modelo de contenedor uniproceso (STA). |
| PSH_HASHELP (0x00000200) | Permite que las páginas de la hoja de propiedades muestren un botón **ayuda** . También debe establecer la marca PSP_HASHELP en la estructura [PROPSHEETPAGE](pss-propsheetpage.md) de la página cuando se crea la página. Si alguna de las páginas de la hoja de propiedades inicial habilita un botón **ayuda** , PSH_HASHELP se establecerá automáticamente. Si ninguna de las páginas iniciales habilita un botón **ayuda** , debe establecer explícitamente PSH_HASHELP si desea tener botones de ayuda en las páginas que se puedan agregar más adelante. Esta marca no se admite junto con PSH_AEROWIZARD.|
| PSH_HEADER (0x00080000) | [Versión 5,80](common-control-versions.md) y versiones posteriores. Indica que se usará un mapa de bits de encabezado con un asistente para Wizard97. También debe establecer la marca PSH_WIZARD97. Si se establece la marca de PSH_USEHBMHEADER, se obtiene el mapa de bits del encabezado del miembro *hbmHeader* . De lo contrario, se obtiene el mapa de bits del encabezado del miembro *pszbmHeader* . Esta marca no se admite junto con PSH_AEROWIZARD. |
| PSH_HEADERBITMAP (0x08000000) | [Versión 6,00](common-control-versions.md) y versiones posteriores. El miembro *pszbmHeader* especifica un mapa de bits que se muestra en el área de encabezado. Debe usarse junto con PSH_AEROWIZARD. |
| PSH_MODELESS (0x00000400) | Hace que la función [hoja](/windows/win32/api/prsht/nf-prsht-propertysheeta) cree la hoja de propiedades como un cuadro de diálogo no modal en lugar de como un cuadro de diálogo modal. Cuando se establece esta marca, [hoja](/windows/win32/api/prsht/nf-prsht-propertysheeta) vuelve inmediatamente después de crear el cuadro de diálogo y el valor devuelto de [hoja](/windows/win32/api/prsht/nf-prsht-propertysheeta) es el identificador de ventana del cuadro de diálogo de la hoja de propiedades. Esta marca no se admite junto con PSH_AEROWIZARD. |
| PSH_NOAPPLYNOW (0x00000080) | Quita el botón **aplicar** . Esta marca no se admite junto con PSH_AEROWIZARD. |
| PSH_NOCONTEXTHELP (0x02000000) | [Versión 5,80](common-control-versions.md) y versiones posteriores. Quita el botón de ayuda contextual ("?"), que normalmente se encuentra en la barra de título de las hojas de propiedades. Esta marca no es válida para los asistentes. Vea [acerca](property-sheets.md) de las hojas de propiedades para obtener una explicación de cómo quitar el botón **ayuda** de la barra de título para versiones anteriores de los controles comunes. Esta marca no se admite junto con PSH_AEROWIZARD. |
| PSH_NOMARGIN (0x10000000) | [Versión 6,00](common-control-versions.md) o posterior. Especifica que no se inserta ningún margen entre la página y el marco. Debe usarse junto con PSH_AEROWIZARD. |
| PSH_PROPSHEETPAGE (0x00000008) | Utiliza el miembro *ppsp* y omite el miembro *phpage* al crear las páginas para la hoja de propiedades. |
| PSH_PROPTITLE (0x00000001) | Indica que *pszCaption* es el nombre del elemento para el que se muestran las propiedades. Windows realiza un ajuste dependiente de la versión y el idioma en el título. Por ejemplo, en inglés, la frase "propiedades para" se antepone a un *pszCaption* no vacío (y si el *pszCaption* genera un título vacío, el título simplemente es "propiedades"). Si se omite esta marca, el pszCaption se usa sin modificar.  |
| PSH_RESIZABLE (0x04000000) | Permite que el usuario cambie el tamaño del asistente. Los botones maximizar y minimizar aparecen en el marco del asistente y el marco es ajustable. Para usar esta marca, también debe establecer PSH_AEROWIZARD. |
| PSH_RTLREADING (0x00000800) | Establece la hoja de propiedades o la ventana del asistente en orden de lectura de derecha a izquierda (RTL), adecuado para idiomas como el hebreo y el árabe. Si no se especifica esta marca, la hoja de propiedades de Windows de forma predeterminada es el orden de lectura de izquierda a derecha (LTR) y las ventanas del asistente coinciden con el orden de lectura de la página actual. |
| PSH_STRETCHWATERMARK (0x00040000) | Ajusta la marca de agua en los asistentes de estilo Wizard97. Esta marca no se admite junto con PSH_AEROWIZARD. Esta marca de estilo solo se incluye para proporcionar compatibilidad con versiones anteriores para determinadas aplicaciones. No se recomienda su uso, y solo se admite en los controles comunes versiones 4,0 y 4,01. Con los controles comunes versión 5,80 y versiones posteriores, esta marca se omite. |
| PSH_USECALLBACK (0x00000100) | Llama a la función especificada por el parámetro *pfnCallback* cuando se producen determinados eventos. Para obtener más información, vea la descripción de la función de devolución de llamada [PFNPROPSHEETCALLBACK](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) . |
| PSH_USEHBMHEADER (0x00100000) | [Versión 5,80](common-control-versions.md). Obtiene el mapa de bits del encabezado del miembro *hbmHeader* en lugar del miembro *pszbmHeader* . También debe establecer la marca PSH_AEROWIZARD o la marca PSH_WIZARD97 junto con la marca PSH_HEADER. |
| PSH_USEHBMWATERMARK (0x00010000) | [Versión 5,80](common-control-versions.md). Obtiene el mapa de bits de marca de agua del miembro *hbmWatermark* en lugar del miembro *pszbmWatermark* . También debe establecer PSH_WIZARD97 y PSH_WATERMARK. Esta marca no se admite junto con PSH_AEROWIZARD. |
| PSH_USEHICON (0x00000002) | Usa *hIcon* como icono pequeño en la barra de título del cuadro de diálogo hoja de propiedades. |
| PSH_USEHPLWATERMARK (0x00020000) | [Versión 5,80](common-control-versions.md). Utiliza la estructura **HPALETTE** señalada por el miembro *hplWatermark* en lugar de la paleta predeterminada para dibujar el mapa de bits de marca de agua y/o el mapa de bits del encabezado para un asistente para Wizard97. También debe establecer PSH_WIZARD97 y PSH_WATERMARK o PSH_HEADER. Esta marca no se admite junto con PSH_AEROWIZARD.  |
| PSH_USEICONID (0x00000004) | Usa *pszIcon* como el nombre del recurso de icono que se va a cargar y usar como icono pequeño en la barra de título del cuadro de diálogo hoja de propiedades. |
| PSH_USEPAGELANG (0x00200000) | [Versión 5,80](common-control-versions.md). Especifica que el idioma de la hoja de propiedades se tomará del recurso de la primera página. La página debe especificarse mediante el identificador de recursos. |
| PSH_USEPSTARTPAGE (0x00000040) | Usa el miembro *pStartPage* en lugar del miembro *nStartPage* cuando se muestra la página inicial de la hoja de propiedades. |
| PSH_WATERMARK (0x00008000) | [Versión 5,80](common-control-versions.md). Especifica que se usará un mapa de bits de marca de agua con un asistente para Wizard97 en las páginas que tienen el estilo PSP_HIDEHEADER. También debe establecer la marca PSH_WIZARD97. El mapa de bits de marca de agua se obtiene del miembro *pszbmWatermark* , a menos que se establezca PSH_USEHBMWATERMARK. En ese caso, el mapa de bits del encabezado se obtiene del miembro *hbmWatermark* . Esta marca no se admite junto con PSH_AEROWIZARD.  |
| PSH_WIZARD (0x00000020) | Crea una hoja de propiedades del asistente. Al usar PSH_AEROWIZARD, también debe establecer esta marca. |
| PSH_WIZARD97 (0x01000000) | [Versión 5,80](common-control-versions.md). Crea una hoja de propiedades de estilo Wizard97, que admite mapas de bits en el encabezado de las páginas interiores y en el lado izquierdo de las páginas exteriores. Esta marca no se admite junto con PSH_AEROWIZARD. |
| PSH_WIZARDCONTEXTHELP (0x00001000) | Agrega un botón de **ayuda** contextual ("?"), que normalmente no está presente en la barra de título de un asistente. Esta marca no es válida para hojas de propiedades normales. Esta marca no se admite junto con PSH_AEROWIZARD. |
| PSH_WIZARDHASFINISH (0x00000010)  | Siempre muestra el botón **Finalizar** en el asistente. También debe establecer PSH_WIZARD, PSH_WIZARD97 o PSH_AEROWIZARD. |
| PSH_WIZARD_LITE (0x00400000) | [Versión 5,80](common-control-versions.md). Usa el estilo Wizard-Lite. Este estilo tiene un aspecto similar al de PSH_WIZARD97, pero se implementa de forma muy parecida a PSH_WIZARD. Existen algunas restricciones sobre cómo se da formato a las páginas. Por ejemplo, no hay ningún borde aplicado y el estilo de PSH_WIZARD_LITE no pinta los mapas de bits de la marca de agua y el encabezado de la forma en que lo hace Wizard97. Esta marca no se admite junto con PSH_AEROWIZARD. |

*hwndParent* 

Tipo: [hWnd](../winprog/windows-data-types.md)

Identificador de la ventana propietaria de la hoja de propiedades.

*hInstance* 

Tipo: [hInstance](../winprog/windows-data-types.md)

Identificador de la instancia de la que se va a cargar el icono, el recurso de cadena de título, el nombre de la página de inicio, el mapa de bits del encabezado o la marca de agua. Si el miembro *pszIcon*, *pszCaption*, *pStartPage*, *pszbmHeader* o *pszbmWatermark* identifica un recurso que se va a cargar, se debe especificar este miembro.

*hIcon* 

Tipo: [HICON](../winprog/windows-data-types.md)

Identificador del icono que se va a usar como icono pequeño en la barra de título del cuadro de diálogo hoja de propiedades. Este miembro se utiliza si el miembro *dwFlags* incluye PSH_USEHICON. Este miembro se declara como una unión con *pszIcon*.

*pszIcon* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

Recurso de icono que se va a usar como icono pequeño en la barra de título del cuadro de diálogo hoja de propiedades. Este miembro se utiliza si el miembro *dwFlags* incluye PSH_USEICONID. Este miembro puede especificar el identificador del recurso de icono o la dirección de la cadena que especifica el nombre del recurso de icono. En ambos casos, el icono se carga desde la instancia proporcionada por el miembro *hInstance* . Este miembro se declara como una unión con *hIcon*.

*pszCaption* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

Título del cuadro de diálogo de la hoja de propiedades. Este miembro puede especificar el identificador de un recurso de cadena (cargado desde la instancia especificada por el miembro *hInstance* ) o la dirección de una cadena que especifica el título. Si el miembro *dwFlags* incluye PSH_PROPTITLE, las **propiedades de cadena de** se insertan al principio del título. Este campo se omite para los asistentes de Wizard97. En el caso de los asistentes de Aero, solo se usa la cadena para el título, independientemente de si se ha establecido la marca de PSH_PROPTITLE.

*nPages* 

Tipo: [uint](../winprog/windows-data-types.md)

Número de páginas de hoja de propiedades proporcionadas en la matriz *ppsp* o *phpage* .

*nStartPage* 

Tipo: [uint](../winprog/windows-data-types.md)

Índice de base cero de la página inicial que aparece cuando se crea el cuadro de diálogo hoja de propiedades. Este miembro se utiliza si el miembro *dwFlags* no incluye la marca PSH_USEPSTARTPAGE. Este miembro se declara como una unión con *pStartPage*.

*pStartPage* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

Nombre de la página inicial que aparece cuando se crea el cuadro de diálogo hoja de propiedades. Este miembro se utiliza si el miembro *dwFlags* incluye la marca PSH_USESTARTPAGE. Este miembro puede especificar el identificador de un recurso de cadena (cargado desde la instancia especificada por el miembro *hInstance* ) o la dirección de una cadena que especifica el nombre. El nombre de la página de inicio coincide con los títulos de las páginas. Este miembro se declara como una unión con *nStartPage*.

*ppsp* 

Tipo: **LPCPROPSHEETPAGE**

Puntero a una matriz de estructuras [PROPSHEETPAGE](pss-propsheetpage.md) que definen las páginas de la hoja de propiedades. Si el miembro *dwFlags* no incluye PSH_PROPSHEETPAGE, se omite este miembro. Tenga en cuenta que la estructura **PROPSHEETPAGE** tiene un tamaño variable. Las aplicaciones que analizan la matriz a la que apunta *ppsp* deben tener en cuenta el tamaño de cada página. Este miembro se declara como una unión con *phpage*.

*phpage* 

Tipo: **HPROPSHEETPAGE \***

Puntero a una matriz de identificadores de las páginas de la hoja de propiedades. Este miembro se utiliza si el miembro *dwFlags* no incluye PSH_PROPSHEETPAGE. Cada identificador debe haber sido creado por una llamada anterior a la función [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . Cuando la función [hoja](/windows/win32/api/prsht/nf-prsht-propertysheeta) devuelve, se destruirán todos los identificadores HPROPSHEETPAGE de la matriz *phpage* . Este miembro se declara como una unión con *ppsp*.

*pfnCallback* 

Tipo: **PFNPROPSHEETCALLBACK**

Puntero a una función de devolución de llamada definida por la aplicación a la que se llama cuando se producen determinados eventos. Para obtener más información sobre la función de devolución de llamada, vea la descripción de la función de devolución de llamada [PFNPROPSHEETCALLBACK](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) . Si el miembro *dwFlags* no incluye PSH_USECALLBACK, se omite este miembro.

*hbmWatermark* 

Tipo: [hBitmap](../winprog/windows-data-types.md)

[Versión 5,80](common-control-versions.md) o posterior. Identificador del mapa de bits de marca de agua. Si el miembro *dwFlags* no incluye PSH_USEHBMWATERMARK, se omite este miembro.

*pszbmWatermark* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

[Versión 5,80](common-control-versions.md) o posterior. Recurso de mapa de bits que se va a usar como marca de agua. Este miembro puede especificar el identificador del recurso de mapa de bits o la dirección de la cadena que especifica el nombre del recurso de mapa de bits. Si el miembro *dwFlags* incluye PSH_USEHBMWATERMARK, se omite este miembro.

*hplWatermark*

Tipo: [HPALETTE](../winprog/windows-data-types.md)

[Versión 5,80](common-control-versions.md) o posterior. Estructura **HPALETTE** utilizada para dibujar el mapa de bits de marca de agua y/o el mapa de bits del encabezado. Si el miembro *dwFlags* no incluye PSH_USEHPLWATERMARK, se omite este miembro.

*hbmHeader*

Tipo: [hBitmap](../winprog/windows-data-types.md)

[Versión 5,80](common-control-versions.md) o posterior. Identificador del mapa de bits del encabezado. Si el miembro *dwFlags* no incluye PSH_USEHBMHEADER, se omite este miembro.

*pszbmHeader*

Tipo: [LPCSTR](../winprog/windows-data-types.md)

[Versión 5,80](common-control-versions.md) o posterior. Recurso de mapa de bits que se va a usar como encabezado. Este miembro puede especificar el identificador del recurso de mapa de bits o la dirección de la cadena que especifica el nombre del recurso de mapa de bits. Si el miembro *dwFlags* incluye PSH_USEHBMHEADER, se omite este miembro.

## <a name="remarks"></a>Observaciones

Si el usuario elige una configuración como fuentes grandes, que amplía el cuadro de diálogo, también se ampliará la marca de agua que se pinta en las páginas de inicio y de finalización. El tamaño y la posición del mapa de bits original seguirán siendo los mismos. El área adicional se rellenará con el color del píxel en la esquina superior izquierda del mapa de bits.

Los estilos PSH_WIZARD, PSH_WIZARD97 y PSH_WIZARD_LITE son mutuamente incompatibles. Solo se debe establecer una de estas marcas de estilo. PSH_AEROWIZARD debe combinarse con PSH_WIZARD.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Solo aplicaciones de escritorio de Windows Vista \[\]                                    |
| Servidor mínimo compatible | Solo aplicaciones de escritorio de Windows Server 2003 \[\]                              |
| Encabezado                   | Prsht. h |
| Nombres Unicode y ANSI                   | **PROPSHEETHEADERW** (Unicode) y **PROPSHEETHEADERA** (ANSI) |
