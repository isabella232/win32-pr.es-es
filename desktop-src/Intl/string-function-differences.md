---
description: En este tema se describen las diferencias entre las funciones de cadena usadas en el control de la información de Unicode y del juego de caracteres. Estas funciones tienen unicode y Windows de página de códigos para admitir Unicode y Windows de página de códigos.
ms.assetid: 52a15957-b44b-49ba-b915-e5c8e003a7e6
title: Diferencias de función de cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60a6208e858eceac65ac8826ffbff6303b970969cae6f635d0bcc027dd6d9f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146998"
---
# <a name="string-function-differences"></a>Diferencias de función de cadena

En este tema se describen las diferencias entre las funciones de cadena usadas en el control de la información de Unicode y del juego de caracteres. Estas funciones tienen [unicode](unicode.md) y Windows de página [de](code-pages.md) códigos para admitir Unicode y Windows de página de códigos.

Las siguientes funciones de cadena no requieren un comentario especial. Sus implementaciones de Windows y Unicode funcionan de forma idéntica.

-   [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta)
-   [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva)
-   [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [ **StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)
-   [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [ **StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa)
-   [**StrCbLength**](/windows/win32/api/strsafe/nf-strsafe-stringcblengtha), [ **StrCchLength**](/windows/win32/api/strsafe/nf-strsafe-stringcchlengtha)

El valor de longitud recuperado por una de las funciones de longitud de cadena siempre se basa en el ancho de caracteres normal: 8 bits para Windows páginas de códigos, 16 bits para Unicode. Este valor se conoce a menudo como "recuento de caracteres". Este término es estrictamente correcto porque Windows [](double-byte-character-sets.md) páginas de códigos que usan juegos de caracteres de doble byte (DBCS) tienen algunos caracteres de ancho completo representados realmente por dos bytes consecutivos. Se produce una situación similar para [los suplentes](surrogates-and-supplementary-characters.md) en Unicode.

Las siguientes funciones de cadena son sensibles a la configuración regional del subproceso actual, derivada del idioma que el usuario selecciona en el Panel de control. Las [**funciones lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) y [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) no realizan comparaciones de bytes como sus nombres ANSI, por ejemplo, [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp). En su lugar, comparan cadenas según las reglas de la configuración regional.

-   [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
-   [**CharLowerBuff**](/windows/win32/api/winuser/nf-winuser-charlowerbuffa)
-   [**CharUpper**](/windows/win32/api/winuser/nf-winuser-charuppera)
-   [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
-   [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)
-   [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)

Las siguientes funciones convierten entre el juego de caracteres OEM y la página de códigos Windows actual o Unicode, dependiendo de la versión que se utilice:

-   [**CharToOem**](/windows/win32/api/winuser/nf-winuser-chartooema)
-   [**CharToOemBuff**](/windows/win32/api/winuser/nf-winuser-chartooembuffa)
-   [**OemToCharBuff**](/windows/win32/api/winuser/nf-winuser-oemtocharbuffa)

Las funciones de impresión, por ejemplo, [**StringCbPrintf,**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa)admiten Unicode proporcionando los siguientes tipos de datos nuevos y modificados en sus especificaciones de formato. Estas especificaciones de formato afectan a la forma en que las funciones interpretan el parámetro de entrada correspondiente.



| Especificación de formato | Tipo de datos para la Windows de la página de códigos | Tipo de datos para la versión Unicode |
|----------------------|-----------------------------------------|-------------------------------|
| c                    | CHAR                                    | WCHAR                         |
| C                    | WCHAR                                   | CHAR                          |
| hc, hC               | CHAR                                    | CHAR                          |
| hs, hS               | LPSTR                                   | LPSTR                         |
| lc, lC               | WCHAR                                   | WCHAR                         |
| ls, lS               | LPWSTR                                  | LPWSTR                        |
| s                    | LPSTR                                   | LPWSTR                        |
| S                    | LPWSTR                                  | LPSTR                         |



 

El tipo de datos del texto de salida siempre depende de la versión de la función. Cuando el tipo de datos del parámetro de entrada y el tipo de datos del texto de salida no están de acuerdo, la función print realiza una conversión de Unicode a la página de códigos Windows actual, o viceversa, según sea necesario.

Para la versión Unicode de las funciones de impresión, la cadena de formato es Unicode, al igual que el texto de salida.

> [!Caution]  
> Un control de búfer deficiente se implica en muchos problemas de seguridad que implican saturaciones del búfer. Consulte [La referencia de Strsafe.h](../menurc/strsafe-ovw.md). Las funciones definidas en Strsafe.h proporcionan procesamiento adicional para el control adecuado del búfer en el código. Por este motivo, están diseñados para reemplazar sus homólogos de C/C++ integrados, así como implementaciones específicas de Windows Microsoft. Para obtener más información, vea [Security Considerations: International Features](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Unicode en la API de Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
