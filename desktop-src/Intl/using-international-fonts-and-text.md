---
description: En cada versión principal de Windows, hay fuentes agregadas para admitir scripts y lenguajes internacionales.
ms.assetid: 77b8c200-2682-4651-855a-602f768edc9b
title: Enumeración y selección de fuentes internacionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e5d0d07a0953f72f097f8578f5e32b3ee49093
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254858"
---
# <a name="international-font-enumeration-and-selection"></a>Enumeración y selección de fuentes internacionales

En cada versión principal de Windows, hay fuentes agregadas para admitir scripts y lenguajes internacionales. Consulte [Compatibilidad](https://msdn.microsoft.com/globalization/mt791278) con scripts y fuentes en Windows para las fuentes que se han agregado en cada versión de Windows desde Windows 2000, así como sus scripts, regiones e idiomas admitidos.

## <a name="enumfontfamiliesex"></a>EnumFontFamiliesEx

Para enumerar fuentes internacionales en la aplicación, puede usar la [**función EnumFontFamiliesEx.**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) **EnumFontFamiliesEx** permite enumerar fuentes basadas en el nombre del tipo de letra y el juego de caracteres pasando un puntero a una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contiene el nombre del tipo de letra y la información del juego de caracteres. Para llamar **a EnumFontFamiliesEx,** puede especificar un nombre de tipo de letra o un juego de caracteres, o bien puede solicitar lo que esté disponible. Al establecer el nombre del tipo de letra **de LOGFONT** en **NULL,** se enumeran todos los nombres de tipo de letra. Al establecer el campo de juego de caracteres **en DEFAULT \_ CHARSET** se enumeran todos los conjuntos de caracteres.

Tenga en cuenta que los juegos de caracteres son una noción heredada correspondiente a los juegos de caracteres anteriores a Unicode. En este momento, no hay ningún mecanismo para enumerar las fuentes que admiten scripts arbitrarios o intervalos de caracteres en Unicode. La estructura [**NEWTEXTMETRICEX**](/windows/win32/api/wingdi/ns-wingdi-newtextmetricexa) pasada por [**EnumFontFamExProc**](/previous-versions//dd162618(v=vs.85)) incluye la estructura [**FONTSIGNATURE,**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) que incluye declaraciones más detalladas proporcionadas por el desarrollador de fuentes sobre qué páginas de códigos y qué rangos Unicode admite la fuente. Para determinar de forma más precisa qué intervalos de caracteres admite una fuente determinada, seleccione la fuente en un contexto de dispositivo y llame a [**GetFontUnicodeRanges**](/windows/win32/api/wingdi/nf-wingdi-getfontunicoderanges). Tenga en cuenta que esta API no admite planos adicionales Unicode.

## <a name="choosefont"></a>ChooseFont

Puede usar la función [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) para mostrar un cuadro de diálogo común que permite al usuario seleccionar fuentes internacionales basadas en un juego de caracteres. Puede especificar una de las tres marcas para determinar, en función del juego de caracteres, qué fuentes se muestran en el cuadro de diálogo ChooseFont: **CF \_ SCRIPTSONLY,** **CF \_ SELECTSCRIPT** o **CF \_ NOSCRIPTSEL**.

La **marca SCRIPTS DE \_ CFONLY** indica a la API que enumere las fuentes de todos los juegos de caracteres que no son symbol ni OEM.

Si desea mostrar solo las fuentes que cubren un juego de caracteres determinado, debe especificar la marca **CF \_ SELECTSCRIPT**. Antes de [**llamar a ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)), inicialice *el campo lfCharSet* de la [**estructura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta) Si está interesado en especificar solo el juego de caracteres, establezca los demás campos de la estructura **LOGFONT** en **NULL.** Para que **ChooseFont** vea la estructura **LOGFONT,** también debe especificar la marca **CF \_ INITTOLOGFONTSTRUCT.**

Por último, al igual que con cualquier otro campo del cuadro de diálogo Fuente, puede elegir mostrar un cuadro de lista de scripts en blanco. Esta funcionalidad es útil si el usuario ha resaltado varias fuentes diferentes que abarcan varios conjuntos de caracteres. En este caso, llamaría a [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) con la **marca CF \_ NOSCRIPTSEL.**

A partir Windows 7, [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) implementa compatibilidad para ocultar fuentes de listas de selección de fuentes. **ChooseFont** solo enumerará las fuentes mostradas y filtrará las fuentes ocultas mientras se muestran las fuentes en el cuadro de lista. La marca adicional **(CF \_ INACTIVEFONTS)** en el miembro flags de la estructura [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) se agrega para que pueda mostrar todas las fuentes instaladas en la lista de fuentes, igual que **ChooseFont** se comportó antes de Windows 7. Para obtener más información sobre las diferencias de comportamiento en Windows 7 para la función **ChooseFont,** vea [**ChooseFont() Win32 Common Dialog**](../win7appqual/choosefont-win32-common-dialog.md) (Cuadro de diálogo común de Win32) en la guía de calidad de la aplicación [Windows 7](../win7appqual/windows-7-application-quality-cookbook.md). Consulte la **función ChooseFont** y **la estructura CHOOSEFONT** para ver las diferencias de experiencia del usuario final Windows 7.

Tenga en cuenta que los juegos de caracteres son una noción heredada correspondiente a los juegos de caracteres anteriores a Unicode. En este momento, no hay ningún mecanismo para filtrar fuentes basadas en scripts Unicode o intervalos de caracteres.

## <a name="font-controls-in-windows-scenic-ribbon"></a>Controles de fuente en la Windows ribbon de Ribbon

Windows 7 presenta la cinta de opciones Windows, que incluye un conjunto de controles destinados a la selección de fuentes. Estos controles de fuente admiten la nueva Windows comportamiento de ocultación de fuentes 7. Puede usar esos controles de fuente para enumerar solo las fuentes mostradas y permitir que el usuario seleccione la fuente.

> [!Note]  
> La compatibilidad con la ocultación de fuentes no está disponible cuando la cinta Windows ribbon de Ribbon se ejecuta en cualquier plataforma anterior a Windows 7.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)
</dt> <dt>

[**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))
</dt> <dt>

[**CHOOSEFONT (estructura)**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**Controles de fuente en Windows cinta de opciones de Ribbon**](../windowsribbon/windowsribbon-element-fontcontrol.md)
</dt> <dt>

[**Cuadro de diálogo común chooseFont() Win32**](../win7appqual/choosefont-win32-common-dialog.md)
</dt> </dl>

 

 
