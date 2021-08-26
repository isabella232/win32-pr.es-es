---
description: Las bibliotecas en tiempo de ejecución estándar de C contienen versiones UTF-16 Unicode (caracteres anchos) de funciones de cadena que se pueden usar con versiones Unicode y orientadas a bytes de funciones de cadena que se pueden usar con caracteres de juegos de caracteres de un solo byte (SBCS). El tipo de datos Unicode WCHAR es compatible con el tipo de datos wchar t en ANSI C y permite el acceso a \_ las funciones de cadena Unicode. Las versiones Unicode de las funciones comienzan con las letras \# &0034;wcs&\# 0034; (o a veces &\# 0034; \_ wcs&\# 0034;). El tipo de datos CHAR utilizado para las páginas de códigos es compatible con el tipo de datos de caracteres char en ANSI C, para permitir el acceso a las funciones de cadena de caracteres. Las versiones de caracteres de las funciones comienzan con las letras \# &0034;str&\# 0034;. También hay versiones especiales para juegos de caracteres de doble byte (DBCS) que comienzan con las letras &\# 0034; \_ mbs&\# 0034;.
ms.assetid: a86626c1-7f90-4924-bfdd-384729bd0cc5
title: Funciones estándar de C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0e576dd8ad506d3d0f3379c161526dd7b9330542ca1cc575c95e3eda8e7dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130165"
---
# <a name="standard-c-functions"></a>Funciones estándar de C

Las bibliotecas en tiempo de ejecución estándar de C contienen versiones UTF-16 Unicode (caracteres anchos) de funciones de cadena que se pueden usar con [versiones Unicode](unicode.md) y orientadas a bytes de funciones de cadena que se pueden usar con caracteres de juegos de caracteres de un solo [byte](single-byte-character-sets.md) (SBCS). El tipo de datos Unicode WCHAR es compatible con el tipo de datos wchar t en ANSI C y permite el acceso a \_ las funciones de cadena Unicode. Las versiones Unicode de las funciones comienzan con las letras "wcs" (o, a veces, \_ "wcs"). El tipo de datos CHAR utilizado para las páginas de códigos es compatible con el tipo de datos de caracteres char en ANSI C, para permitir el acceso a las funciones de cadena de caracteres. Las versiones de caracteres de las funciones comienzan con las letras "str". También hay versiones especiales para juegos de caracteres de doble [byte](double-byte-character-sets.md) (DBCS) que comienzan con las letras \_ "mbs".

Las bibliotecas en tiempo de ejecución estándar de C incluyen funciones genéricas para todas las funciones de cadena de C estándar. Comienzan con \_ "tcs" y aparecen en el archivo de encabezado Tchar.h. Estas funciones usan el tipo de datos TCHAR genérico.

Una aplicación debe agregar las siguientes líneas para usar las funciones genéricas y compilar para Unicode.


```C++
#define _UNICODE

#include <tchar.h>
#include <wchar.h>
```



Tenga en cuenta que los archivos Tchar.h y Wchar.h son necesarios y que también se requiere el carácter de subrayado \_ inicial en la variable UNICODE. Esta nomenclatura es específica de la biblioteca estándar de C. "UNICODE" representado sin el carácter de subrayado es para los entornos de ejecución Windows Microsoft.

Las [funciones wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) y [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) pueden convertir del juego de caracteres admitido por la biblioteca estándar de C a Unicode y back, con algunas limitaciones. Para obtener más información sobre cómo traducir cadenas a y desde Unicode, vea [Traducción entre tipos de cadena.](translation-between-string-types.md)

La [función printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) definida en Tchar.h admite las mismas especificaciones de formato que las funciones de impresión Strsafe.h, por ejemplo [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa). De forma similar, Tchar.h define una [función wprintf,](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) en la que la propia cadena de formato es una cadena Unicode.

> [!Caution]  
> El control deficiente del búfer se implica en muchos problemas de seguridad que implican saturaciones de búfer. Vea [Referencia de Strsafe.h.](../menurc/strsafe-ovw.md) Las funciones definidas en Strsafe.h proporcionan procesamiento adicional para el control adecuado del búfer en el código. Están diseñados para reemplazar sus homólogos integrados de C/C++, así como implementaciones específicas Windows Microsoft. Para obtener más información, vea [Security Considerations: International Features](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Unicode en la API de Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
