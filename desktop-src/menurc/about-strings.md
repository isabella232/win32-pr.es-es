---
title: Acerca de las cadenas
description: En este tema se de abordan las funciones de cadena.
ms.assetid: f1799fbf-4619-4b19-998e-b1d2f4c19a35
keywords:
- resources,strings
- cadenas
- funciones de cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff9fa6c9d93ba2f5c089b52b56816cad74bb61c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268575"
---
# <a name="about-strings"></a>Acerca de las cadenas

Las funciones de cadena dan a las aplicaciones los medios para copiar, comparar, ordenar, dar formato y convertir cadenas de caracteres, así como los medios para determinar el tipo de carácter de cada carácter de una cadena. Todas las funciones de cadena admiten los juegos de caracteres Unicode, de un solo byte y de doble byte si estos juegos de caracteres son compatibles con el sistema operativo en el que se ejecuta la aplicación.

**Advertencia de seguridad:** El uso incorrecto de funciones de cadena puede causar problemas de seguridad para la aplicación. Normalmente, esto implica una saturación del búfer que puede permitir un ataque por denegación de servicio contra la aplicación o la inyección de código ejecutable de un atacante. Las funciones strsafe permiten un control más seguro de las cadenas y se recomiendan para mejorar la seguridad de la aplicación. Para obtener más información sobre estas funciones, vea [Uso de las funciones strsafe.h](strsafe-ovw.md).

En esta sección se tratan los temas siguientes.

-   [Comparación con las funciones de cadena Run-Time C](#comparison-with-c-run-time-string-functions)
-   [Recursos de cadena](#string-resources)

## <a name="comparison-with-c-run-time-string-functions"></a>Comparación con las funciones de cadena Run-Time C

Muchas funciones de cadena duplican o mejoran funciones de cadena conocidas de la biblioteca estándar en tiempo de ejecución de C (CRT). Muchas de las mejoras permiten que las funciones de cadena funcionen con juegos de caracteres Unicode o extendidos. En la tabla siguiente se muestran las funciones de CRT, Windows funciones (que admiten Unicode, a diferencia de las funciones de CRT) y las funciones StrSafe.



| Crt String (Función)                                       | Windows String (Función)    | StrSafe (Función)                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [strcat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019) | [**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata) | <dl> <dt>[**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt>[**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> <dt>[**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt>[**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>         |
| [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp?view=vs-2019) | [**lstrcmp**](/windows/desktop/api/Winbase/nf-winbase-lstrcmpa) | (sin función equivalente)                                                                                                                                                                                                                                                                                                                                                                                  |
| [strcpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019) | [**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya) | <dl> <dt>[**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt>[**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> <dt>[**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt>[**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl> |
| [strlen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019) | [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) | <dl> <dt>[**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> <dt> [ **StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                                                                                                       |



 

Por ejemplo, la función **strlen** siempre devuelve el número de bytes de una cadena, pero la función [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) devuelve el número de valores **TCHAR,** que hace referencia a bytes para versiones ANSI de la función o valores **WCHAR** para versiones Unicode.

Las siguientes funciones de cadena difieren de las funciones estándar de C, como **tolower** y **toupper,** en que funcionan con cualquier carácter de un juego de caracteres. Por ejemplo, mediante la [**función CharLower,**](/windows/desktop/api/Winuser/nf-winuser-charlowera) una aplicación puede convertir una U mayúscula con un umlaut (Ü) a minúsculas (ü). Para obtener más información sobre los juegos de caracteres, vea [Juegos de caracteres de un solo byte.](/windows/desktop/Intl/single-byte-character-sets)



| Función                               | Descripción                                   |
|----------------------------------------|-----------------------------------------------|
| [**CharLower**](/windows/desktop/api/Winuser/nf-winuser-charlowera)         | Convierte un carácter o una cadena en minúsculas.  |
| [**CharLowerBuff**](/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa) | Convierte una cadena de caracteres en minúsculas.     |
| [**CharNext**](/windows/desktop/api/Winuser/nf-winuser-charnexta)           | Se desplaza al siguiente carácter de una cadena.      |
| [**CharPrev**](/windows/desktop/api/Winuser/nf-winuser-charpreva)           | Se desplaza al carácter anterior de una cadena. |
| [**CharUpper**](/windows/desktop/api/Winuser/nf-winuser-charuppera)         | Convierte un carácter o una cadena en mayúsculas.  |
| [**CharUpperBuff**](/windows/desktop/api/Winuser/nf-winuser-charupperbuffa) | Convierte una cadena a mayúsculas.               |



 

Las siguientes funciones de cadena hacen determinaciones sobre un carácter en función de la semántica del idioma seleccionado por el usuario. Estas funciones están habilitadas para Unicode.



| Función                                         | Descripción                                     |
|--------------------------------------------------|-------------------------------------------------|
| [**IsCharAlpha**](/windows/desktop/api/Winuser/nf-winuser-ischaralphaa)               | Determina si un carácter es alfabético.   |
| [**IsCharAlphaNumeric**](/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica) | Determina si un carácter es alfanumérico. |
| [**IsCharLower**](/windows/desktop/api/Winuser/nf-winuser-ischarlowera)               | Determina si un carácter está en minúsculas.    |
| [**IsCharUpper**](/windows/desktop/api/Winuser/nf-winuser-ischaruppera)               | Determina si un carácter está en mayúsculas.    |



 

En la tabla siguiente se muestran las extensiones Unicode a las funciones estándar en tiempo de ejecución de C (CRT). Como se mencionó anteriormente, las funciones de StrSafe permiten un control más seguro de las cadenas y se recomiendan para mejorar la seguridad de la aplicación.



| Función CRT estándar                                       | String (Función)                | StrSafe (Función)                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [sprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)  | [**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)   | <dl> <dt>[**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt>[**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> <dt>[**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt>[**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>         |
| [vsprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019) | [**wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa) | <dl> <dt>[**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt>[**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> <dt>[**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt>[**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> |



 

## <a name="string-resources"></a>Recursos de cadena

Una aplicación que mantiene cadenas de caracteres en recursos se puede traducir a nuevos idiomas con el mínimo esfuerzo. En lugar de buscar cadenas en los módulos de origen, puede traducir simplemente las cadenas en el archivo de recursos y volver a vincular la aplicación. Además, el uso de recursos de cadena simplifica la creación de versiones Unicode y no Unicode de la aplicación a partir de los mismos archivos de origen.

La [**función LoadString**](/windows/desktop/api/Winuser/nf-winuser-loadstringa) carga un recurso de cadena desde el archivo ejecutable de una aplicación. La [**función FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) carga un recurso de cadena e interpreta las opciones de formato que se pueden incrustar en la cadena.

Los recursos en formato binario se almacenan en formato Unicode. Al cargar recursos, las aplicaciones pueden usar la versión Unicode de las funciones de recursos [**(LoadStringW,**](/windows/desktop/api/Winuser/nf-winuser-loadstringa)por ejemplo) para obtener recursos como datos Unicode.

Para los recursos de cadena de 16 bits, la longitud máxima es de 255 caracteres. Para los recursos de cadena de 32 bits, 65535 caracteres es la longitud máxima.

 

 