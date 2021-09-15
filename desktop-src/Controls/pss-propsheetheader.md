---
title: Estructura PROPSHEETHEADER (Prsht.h)
description: Define el marco y las páginas de una hoja de propiedades.
keywords:
- Propiedades de la estructura PROPSHEETHEADER Windows controles
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568580"
---
# <a name="propsheetheader--structure"></a>PropSHEETHEADER (estructura)

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

## <a name="members"></a>Members

*dwSize* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Tamaño, en bytes, de esta estructura. El administrador de hoja de propiedades usa este miembro para determinar qué versión de la **estructura PROPSHEETHEADER** está usando. Para obtener más información, vea la sección Notas.

*dwFlags* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Marcas que indican qué opciones se van a usar cuando se cree la página de la hoja de propiedades. Este miembro puede ser una combinación de los valores siguientes.

| Value | Significado |
|-------|---------|
| PSH_DEFAULT (0x00000000) | Usa el significado predeterminado para todos los miembros de la estructura y crea una hoja de propiedades normal. Esta marca tiene un valor de cero y no se combina con otras marcas. |
| PSH_AEROWIZARD (0x00004000) | [Versión 6.00](common-control-versions.md) y posteriores. Crea una hoja de propiedades del asistente que usa el estilo Deer. También PSH_WIZARD debe establecerse la marca de configuración. Se debe usar el modelo de apartamento de un solo subproceso (STA). |
| PSH_HASHELP (0x00000200) | Permite que las páginas de hojas de propiedades muestren un **botón Ayuda.** También debe establecer la marca PSP_HASHELP en la estructura [PROPSHEETPAGE](pss-propsheetpage.md) de la página cuando se crea la página. Si alguna de las páginas iniciales de la hoja de propiedades habilita **un** botón Ayuda, PSH_HASHELP se establecerá automáticamente. Si ninguna de las  páginas iniciales habilita un botón Ayuda, debe establecer explícitamente PSH_HASHELP si desea tener botones de Ayuda en las páginas que se puedan agregar más adelante. Esta marca no se admite junto con PSH_AEROWIZARD.|
| PSH_HEADER (0x00080000) | [Versión 5.80](common-control-versions.md) y posteriores. Indica que se usará un mapa de bits de encabezado con un Asistente97. También debe establecer la marca PSH_WIZARD97 datos. Si se PSH_USEHBMHEADER marca de encabezado, el mapa de bits del encabezado se obtiene del *miembro hbmHeader.* De lo contrario, el mapa de bits del encabezado se obtiene del *miembro psheader.* Esta marca no se admite junto con PSH_AEROWIZARD. |
| PSH_HEADERBITMAP (0x08000000) | [Versión 6.00](common-control-versions.md) y posteriores. El *miembro psheader especifica* un mapa de bits que se muestra en el área de encabezado. Debe usarse en combinación con PSH_AEROWIZARD. |
| PSH_MODELESS (0x00000400) | Hace que [la función PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) cree la hoja de propiedades como un cuadro de diálogo no modal en lugar de como un cuadro de diálogo modal. Cuando se establece esta marca, [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) devuelve inmediatamente después de crear el cuadro de diálogo y el valor devuelto de [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) es el identificador de ventana del cuadro de diálogo de la hoja de propiedades. Esta marca no se admite junto con PSH_AEROWIZARD. |
| PSH_NOAPPLYNOW (0x00000080) | Quita el **botón** Aplicar. Esta marca no se admite junto con PSH_AEROWIZARD. |
| PSH_NOCONTEXTHELP (0x02000000) | [Versión 5.80](common-control-versions.md) y posteriores. Quita el botón ayuda contextual ("?"), que normalmente está presente en la barra de título de las hojas de propiedades. Esta marca no es válida para los asistentes. Vea [Acerca de las hojas de](property-sheets.md) propiedades para obtener una explicación sobre cómo quitar el botón Ayuda de la barra de subtítulos para versiones anteriores de los controles comunes.  Esta marca no se admite junto con PSH_AEROWIZARD. |
| PSH_NOMARGIN (0x10000000) | [Versión 6.00](common-control-versions.md) o posterior. Especifica que no se inserta ningún margen entre la página y el marco. Debe usarse en combinación con PSH_AEROWIZARD. |
| PSH_PROPSHEETPAGE (0x00000008) | Usa el *miembro ppsp* y omite el *miembro phpage* al crear las páginas para la hoja de propiedades. |
| PSH_PROPTITLE (0x00000001) | Indica que *pszCaption* es el nombre de la cosa para la que se muestran las propiedades. Windows realiza un ajuste dependiente de la versión y del idioma al título. Por ejemplo, en inglés, la frase "Properties for" se antepone a un *pszCaption* no vacío (y si *pszCaption* genera un título vacío, el título es simplemente "Properties"). Si se omite esta marca, pszCaption se usa sin modificar.  |
| PSH_RESIZABLE (0x04000000) | Permite que el usuario cambie el tamaño del asistente. Los botones Maximizar y minimizar aparecen en el marco del asistente y el marco es ajustable. Para usar esta marca, también debe establecer PSH_AEROWIZARD. |
| PSH_RTLREADING (0x00000800) | Establece la hoja de propiedades o la ventana del asistente en el orden de lectura de derecha a izquierda (RTL), adecuado para idiomas como hebreo y árabe. Si no se especifica esta marca, las ventanas de hoja de propiedades tienen como valor predeterminado el orden de lectura de izquierda a derecha (LTR) y las ventanas del asistente coinciden con el orden de lectura de la página actual. |
| PSH_STRETCHWATERMARK (0x00040000) | Extiende la marca de agua en asistentes de estilo Wizard97. Esta marca no se admite junto con PSH_AEROWIZARD. Esta marca de estilo solo se incluye para proporcionar compatibilidad con versiones anteriores para determinadas aplicaciones. No se recomienda su uso y solo es compatible con las versiones 4.0 y 4.01 de los controles comunes. Con los controles comunes de la versión 5.80 y posteriores, se omite esta marca. |
| PSH_USECALLBACK (0x00000100) | Llama a la función especificada por el *parámetro pfnCallback* cuando se producen determinados eventos. Para obtener más información, vea la descripción de la función de devolución de llamada [PFNPROPSHEETCALLBACK.](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) |
| PSH_USEHBMHEADER (0x00100000) | [Versión 5.80.](common-control-versions.md) Obtiene el mapa de bits del encabezado del *miembro hbmHeader* en lugar del *miembro psheader.* También debe establecer la marca PSH_AEROWIZARD o la PSH_WIZARD97 junto con la PSH_HEADER marca. |
| PSH_USEHBMWATERMARK (0x00010000) | [Versión 5.80.](common-control-versions.md) Obtiene el mapa de bits de marca de agua del *miembro hbmWatermark* en lugar del *miembro psforestmWatermark.* También debe establecer PSH_WIZARD97 y PSH_WATERMARK. Esta marca no se admite junto con PSH_AEROWIZARD. |
| PSH_USEHICON (0x00000002) | Usa *hIcon como* icono pequeño en la barra de título del cuadro de diálogo de hoja de propiedades. |
| PSH_USEHPLWATERMARK (0x00020000) | [Versión 5.80.](common-control-versions.md) Usa la **estructura HPALETTE** a la que apunta el miembro *hplWatermark* en lugar de la paleta predeterminada para dibujar el mapa de bits de marca de agua o el mapa de bits de encabezado para un asistente Wizard97. También debe establecer PSH_WIZARD97 y PSH_WATERMARK o PSH_HEADER. Esta marca no se admite junto con PSH_AEROWIZARD.  |
| PSH_USEICONID (0x00000004) | Usa *pszIcon como* nombre del recurso de icono que se cargará y usará como icono pequeño en la barra de título del cuadro de diálogo de hoja de propiedades. |
| PSH_USEPAGELANG (0x00200000) | [Versión 5.80.](common-control-versions.md) Especifica que el idioma de la hoja de propiedades se tomará del recurso de la primera página. Esa página debe especificarse mediante el identificador de recurso. |
| PSH_USEPSTARTPAGE (0x00000040) | Usa el *miembro pStartPage* en lugar del *miembro nStartPage* al mostrar la página inicial de la hoja de propiedades. |
| PSH_WATERMARK (0x00008000) | [Versión 5.80.](common-control-versions.md) Especifica que se usará un mapa de bits de marca de agua con un asistente Wizard97 en las páginas que tienen el PSP_HIDEHEADER de marca de agua. También debe establecer la marca PSH_WIZARD97 configuración. El mapa de bits de marca de agua se obtiene del *miembro psforestmWatermark,* a menos PSH_USEHBMWATERMARK se establezca. En ese caso, el mapa de bits del encabezado se obtiene del *miembro hbmWatermark.* Esta marca no se admite junto con PSH_AEROWIZARD.  |
| PSH_WIZARD (0x00000020) | Crea una hoja de propiedades del asistente. Al usar PSH_AEROWIZARD, también debe establecer esta marca. |
| PSH_WIZARD97 (0x01000000) | [Versión 5.80.](common-control-versions.md) Crea una hoja de propiedades de estilo Wizard97, que admite mapas de bits en el encabezado de páginas interiores y en el lado izquierdo de las páginas exteriores. Esta marca no se admite junto con PSH_AEROWIZARD. |
| PSH_WIZARDCONTEXTHELP (0x00001000) | Agrega un botón de Ayuda **contextual** ("?"), que normalmente no está en la barra de subtítulos de un asistente. Esta marca no es válida para las hojas de propiedades normales. Esta marca no se admite junto con PSH_AEROWIZARD. |
| PSH_WIZARDHASFINISH (0x00000010)  | Siempre muestra el **botón** Finalizar en el asistente. También debe establecer PSH_WIZARD, PSH_WIZARD97 o PSH_AEROWIZARD. |
| PSH_WIZARD_LITE (0x00400000) | [Versión 5.80.](common-control-versions.md) Usa el estilo Wizard-lite. Este estilo es similar en apariencia a PSH_WIZARD97, pero se implementa de forma muy similar a PSH_WIZARD. Hay algunas restricciones en el formato de las páginas. Por ejemplo, no hay bordes obligatorios y el estilo PSH_WIZARD_LITE no pinta la marca de agua y los mapas de bits de encabezado de la manera en que lo hace Wizard97. Esta marca no se admite junto con PSH_AEROWIZARD. |

*hwndParent* 

Tipo: [HWND](../winprog/windows-data-types.md)

Identificador de la ventana de propietario de la hoja de propiedades.

*hInstance* 

Tipo: [HINSTANCE](../winprog/windows-data-types.md)

Identificador en la instancia desde la que se va a cargar el icono, el recurso de cadena de título, el nombre de página inicial, el mapa de bits del encabezado o la marca de agua. Si el *miembro pszIcon*, *pszCaption,* *pStartPage*, *psgregómHeader* o *psiconmWatermark* identifica un recurso que se va a cargar, se debe especificar este miembro.

*hIcon* 

Tipo: [HICON](../winprog/windows-data-types.md)

Controle el icono para usarlo como icono pequeño en la barra de título del cuadro de diálogo de hoja de propiedades. Este miembro se usa si el *miembro dwFlags* incluye PSH_USEHICON. Este miembro se declara como una unión con *pszIcon*.

*pszIcon* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

Recurso de icono que se usará como icono pequeño en la barra de título del cuadro de diálogo de hoja de propiedades. Este miembro se usa si el *miembro dwFlags* incluye PSH_USEICONID. Este miembro puede especificar el identificador del recurso de icono o la dirección de la cadena que especifica el nombre del recurso de icono. En ambos casos, el icono se carga desde la instancia proporcionada por el *miembro hInstance.* Este miembro se declara como una unión con *hIcon*.

*pszCaption* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

Título del cuadro de diálogo de hoja de propiedades. Este miembro puede especificar el identificador de un recurso de cadena (cargado desde la instancia especificada por el *miembro hInstance)* o la dirección de una cadena que especifica el título. Si el *miembro dwFlags* incluye PSH_PROPTITLE, la cadena **Propiedades de** se inserta al principio del título. Este campo se omite para los asistentes de Wizard97. En el caso de los asistentes de Aero, la cadena solo se usa para el título, independientemente de si se establece PSH_PROPTITLE marca.

*nPages* 

Tipo: [UINT](../winprog/windows-data-types.md)

Número de páginas de hoja de propiedades proporcionadas en la *matriz ppsp* *o phpage.*

*nStartPage* 

Tipo: [UINT](../winprog/windows-data-types.md)

Índice de base cero de la página inicial que aparece cuando se crea el cuadro de diálogo de hoja de propiedades. Este miembro se usa si el *miembro dwFlags* no incluye la marca PSH_USEPSTARTPAGE datos. Este miembro se declara como una unión con *pStartPage*.

*pStartPage* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

Nombre de la página inicial que aparece cuando se crea el cuadro de diálogo de hoja de propiedades. Este miembro se usa si el *miembro dwFlags* incluye PSH_USESTARTPAGE marca. Este miembro puede especificar el identificador de un recurso de cadena (cargado desde la instancia especificada por el *miembro hInstance)* o la dirección de una cadena que especifica el nombre. El nombre de la página de inicio coincide con los títulos de las páginas. Este miembro se declara como una unión con *nStartPage*.

*ppsp* 

Tipo: **LPCPROPSHEETPAGE**

Puntero a una matriz de [estructuras PROPSHEETPAGE](pss-propsheetpage.md) que definen las páginas de la hoja de propiedades. Si el *miembro dwFlags* no incluye PSH_PROPSHEETPAGE, este miembro se omite. Tenga en cuenta que **la estructura PROPSHEETPAGE** tiene un tamaño variable. Las aplicaciones que analizan la matriz a la que *apunta ppsp* deben tener en cuenta el tamaño de cada página. Este miembro se declara como una unión con *phpage*.

*phpage* 

Tipo: **HPROPSHEETPAGE \***

Puntero a una matriz de identificadores a las páginas de la hoja de propiedades. Este miembro se usa si el *miembro dwFlags* no incluye PSH_PROPSHEETPAGE. Cada identificador debe haber sido creado por una llamada anterior a la [función CreatePropertySheetPage.](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) Cuando se [devuelve la función PropertySheet,](/windows/win32/api/prsht/nf-prsht-propertysheeta) se habrán destruido todos los identificadores HPROPSHEETPAGE de la matriz *phpage.* Este miembro se declara como una unión con *ppsp*.

*pfnCallback* 

Tipo: **PFNPROPSHEETCALLBACK**

Puntero a una función de devolución de llamada definida por la aplicación a la que se llama cuando se producen determinados eventos. Para obtener más información sobre la función de devolución de llamada, vea la descripción de la función de devolución de [llamada PFNPROPSHEETCALLBACK.](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) Si el *miembro dwFlags* no incluye PSH_USECALLBACK, este miembro se omite.

*hbmWatermark* 

Tipo: [HBITMAP](../winprog/windows-data-types.md)

[Versión 5.80](common-control-versions.md) o posterior. Identificador del mapa de bits de marca de agua. Si el *miembro dwFlags* no incluye PSH_USEHBMWATERMARK, este miembro se omite.

*pswatermWatermark* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

[Versión 5.80](common-control-versions.md) o posterior. Recurso de mapa de bits que se usará como marca de agua. Este miembro puede especificar el identificador del recurso de mapa de bits o la dirección de la cadena que especifica el nombre del recurso de mapa de bits. Si el *miembro dwFlags* incluye PSH_USEHBMWATERMARK, este miembro se omite.

*hplWatermark*

Tipo: [HPATTE](../winprog/windows-data-types.md)

[Versión 5.80](common-control-versions.md) o posterior. **Estructura HPATTE usada** para dibujar el mapa de bits de marca de agua o el mapa de bits de encabezado. Si el *miembro dwFlags* no incluye PSH_USEHPLWATERMARK, este miembro se omite.

*hbmHeader*

Tipo: [HBITMAP](../winprog/windows-data-types.md)

[Versión 5.80](common-control-versions.md) o posterior. Identificador del mapa de bits del encabezado. Si el *miembro dwFlags* no incluye PSH_USEHBMHEADER, este miembro se omite.

*psheadermHeader*

Tipo: [LPCSTR](../winprog/windows-data-types.md)

[Versión 5.80](common-control-versions.md) o posterior. Recurso de mapa de bits que se usará como encabezado. Este miembro puede especificar el identificador del recurso de mapa de bits o la dirección de la cadena que especifica el nombre del recurso de mapa de bits. Si el *miembro dwFlags* incluye PSH_USEHBMHEADER, este miembro se omite.

## <a name="remarks"></a>Observaciones

Si el usuario elige un valor como Fuentes grandes, que amplía el cuadro de diálogo, también se ampliará la marca de agua que se pinta en las páginas de inicio y fin. El tamaño y la posición del mapa de bits original seguirán siendo los mismos. El área adicional se rellenará con el color del píxel en la esquina superior izquierda del mapa de bits.

Los PSH_WIZARD, PSH_WIZARD97 y PSH_WIZARD_LITE son mutuamente incompatibles. Solo se debe establecer una de estas marcas de estilo. PSH_AEROWIZARD debe combinarse con PSH_WIZARD.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows Solo \[ aplicaciones de escritorio de Vista\]                                    |
| Servidor mínimo compatible | Windows Solo aplicaciones de escritorio de Server 2003 \[\]                              |
| Encabezado                   | Prsht.h |
| Nombres Unicode y ANSI                   | **PROPSHEETHEADERW** (Unicode) y **PROPSHEETHEADERA** (ANSI) |
