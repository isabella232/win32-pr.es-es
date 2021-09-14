---
description: En este tema se describen las diferencias entre las funciones de cadena usadas en el control de la información de unicode y juego de caracteres. Estas funciones tienen implementaciones unicode y Windows de página de códigos para admitir Unicode Windows parámetros de página de códigos.
ms.assetid: 52a15957-b44b-49ba-b915-e5c8e003a7e6
title: Diferencias de función de cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c940aa8be1603f7958fb1993cc521ca7b1ed7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171897"
---
# <a name="string-function-differences"></a>Diferencias de función de cadena

En este tema se describen las diferencias entre las funciones de cadena usadas en el control de la información de unicode y juego de caracteres. Estas funciones tienen [implementaciones de](unicode.md) [páginas de códigos](code-pages.md) Unicode Windows para admitir Unicode Windows parámetros de página de códigos.

Las siguientes funciones de cadena no requieren un comentario especial. Sus implementaciones de Windows unicode y de página de códigos funcionan de forma idéntica.

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

Las siguientes funciones convierten entre el juego de caracteres oem y la página Windows de códigos actual o Unicode, en función de la versión que se utilice:

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



 

El tipo de datos para el texto de salida siempre depende de la versión de la función. Cuando el tipo de datos del parámetro de entrada y el tipo de datos del texto de salida no están de acuerdo, la función print realiza una conversión de Unicode Windows la página de códigos Windows actual, o viceversa, según sea necesario.

Para la versión Unicode de las funciones de impresión, la cadena de formato es Unicode, al igual que el texto de salida.

> [!Caution]  
> El control deficiente del búfer se implica en muchos problemas de seguridad que implican saturaciones de búfer. Vea [Referencia de Strsafe.h.](../menurc/strsafe-ovw.md) Las funciones definidas en Strsafe.h proporcionan procesamiento adicional para el control adecuado del búfer en el código. Por esta razón, están diseñados para reemplazar sus homólogos integrados de C/C++, así como implementaciones de microsoft Windows específicas. Para obtener más información, vea [Security Considerations: International Features](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Unicode en la API de Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
