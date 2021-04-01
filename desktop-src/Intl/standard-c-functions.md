---
description: Las bibliotecas en tiempo de ejecución estándar de C contienen versiones Unicode UTF-16 (caracteres anchos) de funciones de cadena que se pueden usar con versiones Unicode y orientadas a bytes de funciones de cadena que se pueden usar con caracteres de juegos de caracteres de un solo byte (SBCSs). El tipo de datos Unicode WCHAR es compatible con el tipo de datos WCHAR \_ t en ANSI C y permite el acceso a las funciones de cadena Unicode. Las versiones Unicode de las funciones comienzan con las letras &\# 0034; wcs&\# 0034; (o a veces &\# 0034; \_ WCS&\# 0034;). El tipo de datos CHAR utilizado para las páginas de códigos es compatible con el tipo de datos de caracteres char en ANSI C, para permitir el acceso a las funciones de cadena de caracteres. Las versiones de caracteres de las funciones comienzan con las letras &\# 0034; str&\# 0034;. También hay versiones especiales de juegos de caracteres de doble byte (DBCS) que comienzan con las letras &\# 0034; \_ MBS&\# 0034;.
ms.assetid: a86626c1-7f90-4924-bfdd-384729bd0cc5
title: Funciones estándar de C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6247b3707f96908ef16d887462ba06573fd8dd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913522"
---
# <a name="standard-c-functions"></a>Funciones estándar de C

Las bibliotecas en tiempo de ejecución estándar de C contienen versiones Unicode UTF-16 (caracteres anchos) de funciones de cadena que se pueden usar con versiones [Unicode](unicode.md) y orientadas a bytes de funciones de cadena que se pueden usar con caracteres de [juegos de caracteres de un solo byte](single-byte-character-sets.md) (SBCSs). El tipo de datos Unicode WCHAR es compatible con el tipo de datos WCHAR \_ t en ANSI C y permite el acceso a las funciones de cadena Unicode. Las versiones Unicode de las funciones comienzan con las letras "WCS" (o a veces " \_ WCS"). El tipo de datos CHAR utilizado para las páginas de códigos es compatible con el tipo de datos de caracteres char en ANSI C, para permitir el acceso a las funciones de cadena de caracteres. Las versiones de caracteres de las funciones comienzan con las letras "STR". También hay versiones especiales de [juegos de caracteres de doble byte](double-byte-character-sets.md) (DBCS) que comienzan con las letras " \_ MBS".

Las bibliotecas en tiempo de ejecución estándar de C incluyen funciones genéricas para todas las funciones de cadena estándar de C. Comienzan con " \_ TCS" y se enumeran en el archivo de encabezado TCHAR. h. Estas funciones usan el tipo de datos TCHAR genérico.

Una aplicación debe agregar las siguientes líneas para usar las funciones genéricas y compilar para Unicode.


```C++
#define _UNICODE

#include <tchar.h>
#include <wchar.h>
```



Tenga en cuenta que los archivos TCHAR. h y WCHAR. h son obligatorios y que también se requiere el carácter de subrayado inicial en la \_ variable Unicode. Esta nomenclatura es específica de la biblioteca estándar de C. "Unicode" se representa sin el carácter de subrayado para Microsoft Windows en tiempo de ejecución.

Las funciones [wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) y [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) pueden convertir desde el juego de caracteres compatible con la biblioteca estándar de C a Unicode y viceversa, con algunas limitaciones. Para obtener más información sobre la traducción de cadenas a y desde Unicode, vea [traducción entre tipos de cadena](translation-between-string-types.md).

La función [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) definida en TCHAR. h admite las mismas especificaciones de formato que las funciones de impresión strsafe. h, por ejemplo [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa). Del mismo modo, TCHAR. h define una función [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) , en la que la propia cadena de formato es una cadena Unicode.

> [!Caution]  
> Un control deficiente del búfer es implicado en muchos problemas de seguridad que implican saturaciones del búfer. Consulte [referencia de strsafe. h](../menurc/strsafe-ovw.md). Las funciones definidas en strsafe. h proporcionan procesamiento adicional para el control de búfer adecuado en el código. Están diseñados para reemplazar sus homólogos de C/C++ integrados, así como implementaciones específicas de Microsoft Windows. Para obtener más información, vea [consideraciones de seguridad: características internacionales](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Unicode en la API de Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
