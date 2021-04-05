---
description: En este tema se describen las diferencias entre las funciones de cadena utilizadas para controlar la información de Unicode y del juego de caracteres. Estas funciones tienen implementaciones de páginas de códigos Unicode y de Windows para admitir los parámetros de página de códigos Unicode y Windows.
ms.assetid: 52a15957-b44b-49ba-b915-e5c8e003a7e6
title: Diferencias de las funciones de cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c940aa8be1603f7958fb1993cc521ca7b1ed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001566"
---
# <a name="string-function-differences"></a>Diferencias de las funciones de cadena

En este tema se describen las diferencias entre las funciones de cadena utilizadas para controlar la información de Unicode y del juego de caracteres. Estas funciones tienen implementaciones de [páginas de códigos](code-pages.md) [Unicode](unicode.md) y de Windows para admitir los parámetros de página de códigos Unicode y Windows.

Las siguientes funciones de cadena no requieren un comentario especial. Sus implementaciones de páginas de códigos de Windows y Unicode funcionan de manera idéntica.

-   [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta)
-   [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva)
-   [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [ **StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)
-   [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [ **StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa)
-   [**StrCbLength**](/windows/win32/api/strsafe/nf-strsafe-stringcblengtha), [ **StrCchLength**](/windows/win32/api/strsafe/nf-strsafe-stringcchlengtha)

El valor de longitud recuperado por una de las funciones de longitud de cadena siempre se basa en el ancho normal de caracteres: 8 bits para páginas de códigos de Windows, 16 bits para Unicode. Este valor a menudo se conoce como "recuento de caracteres". Este término es estrictamente correcto porque las páginas de códigos de Windows que usan [juegos de caracteres de doble byte](double-byte-character-sets.md) (DBCS) tienen algunos caracteres de ancho completo que realmente representan dos bytes consecutivos. Se produce una situación similar para los [suplentes](surrogates-and-supplementary-characters.md) de Unicode.

Las siguientes funciones de cadena son sensibles a la configuración regional del subproceso actual, derivada del idioma que el usuario selecciona en el panel de control. Las funciones [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) y [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) no realizan comparaciones de bytes como su namesakes ANSI, por ejemplo, [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp). En su lugar, comparan cadenas según las reglas de la configuración regional.

-   [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
-   [**CharLowerBuff**](/windows/win32/api/winuser/nf-winuser-charlowerbuffa)
-   [**CharUpper**](/windows/win32/api/winuser/nf-winuser-charuppera)
-   [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
-   [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)
-   [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)

Las siguientes funciones convierten entre el juego de caracteres OEM y la página de códigos de Windows actual o Unicode, dependiendo de la versión utilizada:

-   [**CharToOem**](/windows/win32/api/winuser/nf-winuser-chartooema)
-   [**CharToOemBuff**](/windows/win32/api/winuser/nf-winuser-chartooembuffa)
-   [**OemToCharBuff**](/windows/win32/api/winuser/nf-winuser-oemtocharbuffa)

Las funciones de impresión, por ejemplo, [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), admiten Unicode proporcionando los siguientes tipos de datos nuevos y modificados en sus especificaciones de formato. Estas especificaciones de formato afectan a la manera en que las funciones interpretan el parámetro de entrada correspondiente.



| Especificación de formato | Tipo de datos para la versión de la página de códigos de Windows | Tipo de datos para la versión Unicode |
|----------------------|-----------------------------------------|-------------------------------|
| c                    | CHAR                                    | WCHAR                         |
| C                    | WCHAR                                   | CHAR                          |
| HC, hC               | CHAR                                    | CHAR                          |
| HS, hS               | LPSTR                                   | LPSTR                         |
| LC, lC               | WCHAR                                   | WCHAR                         |
| LS, lS               | LPWSTR                                  | LPWSTR                        |
| s                    | LPSTR                                   | LPWSTR                        |
| S                    | LPWSTR                                  | LPSTR                         |



 

El tipo de datos para el texto de salida siempre depende de la versión de la función. Cuando el tipo de datos del parámetro de entrada y el tipo de datos del texto de salida no coinciden, la función print realiza una conversión de Unicode a la página de códigos actual de Windows, o viceversa, según sea necesario.

Para la versión Unicode de las funciones de impresión, la cadena de formato es Unicode, como es el texto de salida.

> [!Caution]  
> Un control deficiente del búfer es implicado en muchos problemas de seguridad que implican saturaciones del búfer. Consulte [referencia de strsafe. h](../menurc/strsafe-ovw.md). Las funciones definidas en strsafe. h proporcionan procesamiento adicional para el control de búfer adecuado en el código. Por este motivo, están diseñados para reemplazar sus homólogos de C/C++ integrados, así como las implementaciones específicas de Microsoft Windows. Para obtener más información, vea [consideraciones de seguridad: características internacionales](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Unicode en la API de Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
