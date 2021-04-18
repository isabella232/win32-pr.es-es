---
description: En cada versión principal de Windows, hay fuentes agregadas para admitir lenguajes y scripts internacionales.
ms.assetid: 77b8c200-2682-4651-855a-602f768edc9b
title: Enumeración y selección de fuentes internacionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e5d0d07a0953f72f097f8578f5e32b3ee49093
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361654"
---
# <a name="international-font-enumeration-and-selection"></a>Enumeración y selección de fuentes internacionales

En cada versión principal de Windows, hay fuentes agregadas para admitir lenguajes y scripts internacionales. Consulte [compatibilidad con scripts y fuentes en Windows](https://msdn.microsoft.com/globalization/mt791278) para las fuentes que se agregaron en cada versión de Windows desde Windows 2000, así como sus scripts, regiones e idiomas admitidos.

## <a name="enumfontfamiliesex"></a>EnumFontFamiliesEx

Para enumerar las fuentes internacionales en la aplicación, puede usar la función [**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) . **EnumFontFamiliesEx** permite enumerar las fuentes basándose en el nombre del tipo de letra y el juego de caracteres pasando un puntero a una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contiene el nombre del tipo de letra y la información del juego de caracteres. Para llamar a **EnumFontFamiliesEx**, puede especificar un nombre de tipo de letra o un juego de caracteres, o puede solicitar el que esté disponible. Al establecer el nombre del tipo de letra de **LOGFONT** en **null** se enumeran todos los nombres de tipo de letra. Al establecer el campo charset en el **\_ juego de caracteres predeterminado** , se enumeran todos los juegos de caracteres.

Tenga en cuenta que los juegos de caracteres son una noción heredada que corresponde a los juegos de caracteres anteriores a Unicode. En este momento, no hay ningún mecanismo para enumerar las fuentes que admiten scripts arbitrarios o intervalos de caracteres en Unicode. La estructura [**NEWTEXTMETRICEX**](/windows/win32/api/wingdi/ns-wingdi-newtextmetricexa) pasada por [**EnumFontFamExProc**](/previous-versions//dd162618(v=vs.85)) incluye la estructura [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) , que incluye declaraciones más detalladas proporcionadas por el desarrollador de fuentes en cuanto a las páginas de códigos y los intervalos Unicode que admite la fuente. Para determinar con más precisión qué intervalos de caracteres admite una fuente determinada, seleccione la fuente en un contexto de dispositivo y llame a [**GetFontUnicodeRanges**](/windows/win32/api/wingdi/nf-wingdi-getfontunicoderanges). Tenga en cuenta que esta API no admite los planos complementarios Unicode.

## <a name="choosefont"></a>ChooseFont

Puede usar la función [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) para mostrar un cuadro de diálogo común que permite al usuario seleccionar fuentes internacionales basadas en el juego de caracteres. Puede especificar una de las tres marcas para determinar, en función del juego de caracteres, qué fuentes se muestran en el cuadro de diálogo ChooseFont: **CF \_ SCRIPTSONLY**, **CF \_ SELECTSCRIPT** o **CF \_ NOSCRIPTSEL**.

La marca **CF \_ SCRIPTSONLY** indica a la API que enumere las fuentes para todos los juegos de caracteres que no son Symbol ni OEM.

Si desea mostrar solo las fuentes que cubren un juego de caracteres determinado, debe especificar la marca **CF \_ SELECTSCRIPT**. Antes de llamar a [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)), inicialice el campo *lfCharSet* de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . Si solo le interesa especificar el juego de caracteres, establezca los demás campos de la estructura **LOGFONT** en **null**. Para que **ChooseFont** examine la estructura **LOGFONT** , también debe especificar la marca INITTOLOGFONTSTRUCT de **CF \_** .

Por último, al igual que con cualquier otro campo del cuadro de diálogo fuente, puede optar por mostrar un cuadro de lista script en blanco. Esta capacidad es útil si el usuario ha resaltado varias fuentes diferentes que abarcan varios juegos de caracteres. En este caso, llamaría a [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) con la marca **\_ NOSCRIPTSEL de CF** .

A partir de Windows 7, [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) implementa compatibilidad para ocultar fuentes de las listas de selección de fuentes. **ChooseFont** solo mostrará las fuentes que se muestran y filtrará las fuentes ocultas al mostrar las fuentes en el cuadro de lista. La marca adicional (**CF \_ INACTIVEFONTS**) en el miembro flags de la estructura [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) se agrega para permitir que se muestren todas las fuentes instaladas en la lista fuente, igual que **ChooseFont** comportado antes de Windows 7. Para obtener información detallada sobre las diferencias de comportamiento en Windows 7 para la función **ChooseFont** , vea el [**cuadro de diálogo común de Win32 ()**](../win7appqual/choosefont-win32-common-dialog.md) en la guía de calidad de la [aplicación de Windows 7](../win7appqual/windows-7-application-quality-cookbook.md). Haga referencia a la función **ChooseFont** y a la estructura **ChooseFont** para conocer las diferencias de experiencia del usuario final en Windows 7.

Tenga en cuenta que los juegos de caracteres son una noción heredada que corresponde a los juegos de caracteres anteriores a Unicode. En este momento, no hay ningún mecanismo para filtrar las fuentes en función de los scripts Unicode o los intervalos de caracteres.

## <a name="font-controls-in-windows-scenic-ribbon"></a>Controles de fuente en Windows Scenic cinta de opciones

Windows 7 presenta la cinta de Windows Scenic, que incluye un conjunto de controles destinados a la selección de fuentes. Estos controles de fuente admiten el nuevo comportamiento de ocultación de fuentes de Windows 7. Puede usar esos controles de fuente para mostrar solo las fuentes que se muestran y permitir que el usuario seleccione la fuente.

> [!Note]  
> La compatibilidad con la ocultación de fuentes no está disponible cuando la cinta de Windows Scenic se está ejecutando en cualquier plataforma anterior a Windows 7.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)
</dt> <dt>

[**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))
</dt> <dt>

[**Estructura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**Controles de fuente en Windows Scenic cinta de opciones**](../windowsribbon/windowsribbon-element-fontcontrol.md)
</dt> <dt>

[**Cuadro de diálogo común de Win32 ChooseFont ()**](../win7appqual/choosefont-win32-common-dialog.md)
</dt> </dl>

 

 
