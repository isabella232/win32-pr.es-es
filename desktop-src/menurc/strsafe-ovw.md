---
title: Acerca de Strsafe.h
description: Un control de búfer deficiente se implica en muchos problemas de seguridad que implican saturaciones del búfer.
ms.assetid: a104a260-1edb-441a-acf8-e2bd3a7d8235
keywords:
- funciones de cadena
- Strsafe.h
- Funciones strsafe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5d50a6921e2775c64fd4db53393332c667aba975ffa366fb2eb49881b6beaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720595"
---
# <a name="about-strsafeh"></a>Acerca de Strsafe.h

Un control de búfer deficiente se implica en muchos problemas de seguridad que implican saturaciones del búfer. Las funciones definidas en Strsafe.h proporcionan procesamiento adicional para el control adecuado del búfer en el código. Por esta razón, están diseñados para reemplazar sus homólogos de C/C++ integrados, así como implementaciones de Windows específicas. Strsafe.h está disponible en el SDK de Windows a partir de Windows XP con Service Pack 2 (SP2).

Las ventajas de las funciones strsafe incluyen:

-   El tamaño del búfer de destino siempre se proporciona a la función para asegurarse de que la función no escribe más allá del final del búfer.

-   Se garantiza que los búferes terminan en NULL, incluso si la operación trunca el resultado previsto.

-   Todas las funciones devuelven **un valor HRESULT,** con solo un código de éxito posible **(S \_ OK**).

-   Cada función está disponible en una versión correspondiente de recuento de caracteres ("cch") o recuento de bytes ("cb").

-   La mayoría de las funciones tienen una versión extendida ("Ex") disponible para funcionalidad avanzada.

Vea las secciones siguientes para obtener información.

-   [Funciones de recuento de caracteres](#character-count-functions)
-   [Funciones de recuento de bytes](#byte-count-functions)
-   [Uso de Strsafe.h](#using-strsafeh)
-   [Temas relacionados](#related-topics)

## <a name="character-count-functions"></a>Funciones de recuento de caracteres

Las funciones siguientes usan un recuento de caracteres en lugar de un recuento de bytes.



| Función                                                                                                                                                                                                                      | Reemplaza                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>[**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt> [ **StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> </dl>                 | <dl> <dt>[strcat, wcscat, \_ tcsat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019)</dt> <dt>[**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata)</dt> <dt>[**StrCat**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatw)</dt> <dt>[**StrCatBuff**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatbuffa)</dt> </dl>                                                                             |
| <dl> <dt>[**StringCchCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)</dt> <dt> [ **StringCchCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)</dt> </dl>             | <dl> <dt>[strncat](/cpp/c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l?view=vs-2019)</dt> <dt> [ **StrNCat**](/windows/desktop/api/shlwapi/nf-shlwapi-strncata)</dt> </dl>                                                                                                                                                                                                                                                                   |
| <dl> <dt>[**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt> [ **StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> </dl>             | <dl> <dt>[strcpy, wcscpy, \_ tcscpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019)</dt> <dt>[**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)</dt> <dt>[**StrCpy**](/windows/desktop/api/shlwapi/nf-shlwapi-strcpyw)</dt> </dl>                                                                                                                                                                    |
| <dl> <dt>[**StringCchCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)</dt> <dt> [ **StringCchCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)</dt> </dl>         | <dl> <dt>[strncpy, wcsncpy, \_ tcsncpy](/cpp/c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>[**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)</dt> <dt> [ **StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)</dt> </dl>             | <dl> <dt>[gets, \_ getws, \_ getts](/cpp/c-runtime-library/gets-getws?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>[**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt> [ **StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> </dl>     | <dl> <dt>[sprintf, swprintf, \_ stprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)</dt> <dt>[**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)</dt> <dt>[**wnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wnsprintfa)</dt> <dt>[ \_ snprintf, \_ snwprintf, \_ sntprintf](/cpp/c-runtime-library/reference/snprintf-snprintf-snprintf-l-snwprintf-snwprintf-l?view=vs-2019)</dt> </dl>          |
| <dl> <dt>[**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt> [ **StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> </dl> | <dl> <dt>[vsprintf, vswprintf, \_ vstprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019)</dt> <dt>[vsnprintf, \_ vsnwprintf, \_ vsntprintf](/cpp/c-runtime-library/reference/vsnprintf-vsnprintf-vsnprintf-l-vsnwprintf-vsnwprintf-l?view=vs-2019)</dt> <dt>[**wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)</dt> <dt>[**wvnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wvnsprintfa)</dt> </dl>, |
| <dl> <dt>[**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> </dl>                                                                                                         | <dl> <dt>[strlen, wcslen, \_ tcslen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="byte-count-functions"></a>Funciones de recuento de bytes

Las funciones siguientes usan un recuento de bytes en lugar de un recuento de caracteres.



| Función                                                                                                                                                                                                                  | Reemplaza                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>[**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt> [ **StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>                 | <dl> <dt>[strcat, wcscat, \_ tcsat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019)</dt> <dt>[**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata)</dt> <dt>[**StrCat**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatw)</dt> <dt>[**StrCatBuff**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatbuffa)</dt> </dl>                                                                            |
| <dl> <dt>[**StringCbCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)</dt> <dt> [ **StringCbCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)</dt> </dl>             | <dl> <dt>[strncat](/cpp/c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l?view=vs-2019)</dt> <dt> [ **StrNCat**](/windows/desktop/api/shlwapi/nf-shlwapi-strncata)</dt> </dl>                                                                                                                                                                                                                                                                  |
| <dl> <dt>[**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt> [ **StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl>             | <dl> <dt>[strcpy, wcscpy, \_ tcscpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019)</dt> <dt>[**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)</dt> <dt>[**StrCpy**](/windows/desktop/api/shlwapi/nf-shlwapi-strcpyw)</dt> </dl>                                                                                                                                                                   |
| <dl> <dt>[**StringCbCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)</dt> <dt> [ **StringCbCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)</dt> </dl>         | <dl> <dt>[strncpy, wcsncpy, \_ tcsncpy](/cpp/c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>[**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)</dt> <dt> [ **StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)</dt> </dl>             | <dl> <dt>[gets, \_ getws, \_ getts](/cpp/c-runtime-library/gets-getws?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>[**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt> [ **StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>     | <dl> <dt>[sprintf, swprintf, \_ stprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)</dt> <dt>[**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)</dt> <dt>[**wnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wnsprintfa)</dt> <dt>[ \_ snprintf, \_ snwprintf, \_ sntprintf](/cpp/c-runtime-library/reference/snprintf-snprintf-snprintf-l-snwprintf-snwprintf-l?view=vs-2019)</dt> </dl>         |
| <dl> <dt>[**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt> [ **StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> | <dl> <dt>[vsprintf, vswprintf, \_ vstprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019)</dt> <dt>[vsnprintf, \_ vsnwprintf, \_ vsntprintf](/cpp/c-runtime-library/reference/vsnprintf-vsnprintf-vsnprintf-l-vsnwprintf-vsnwprintf-l?view=vs-2019)</dt> <dt>[**wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)</dt> <dt>[**wvnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wvnsprintfa)</dt> </dl> |
| <dl> <dt>[**StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                       | <dl> <dt>[strlen, wcslen, \_ tcslen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="using-strsafeh"></a>Uso de Strsafe.h

-   Para usar las funciones strsafe insertadas, incluya el archivo de encabezado como se muestra aquí, siguiendo las instrucciones **\# include** para todos los demás archivos de encabezado.

    `#include <strsafe.h>`

-   Para usar las funciones en formato de biblioteca, incluya la siguiente instrucción antes de incluir Strsafe.h. Sin embargo, se recomienda usar las funciones insertadas.

    `#define STRSAFE_LIB`

    > [!Note]  
    > : las siguientes funciones deben usarse como funciones insertadas: [**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa), [**StringCbGetsEx,**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa) [**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)y [**StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa).

     

-   Al incluir Strsafe.h en el archivo, las funciones anteriores reemplazadas por las funciones strsafe.h estarán en desuso. Los intentos de usar estas funciones anteriores producirán un error del compilador que le dice que use las funciones más recientes. Si desea invalidar este comportamiento, incluya la siguiente instrucción antes de incluir Strsafe.h.

    `#define STRSAFE_NO_DEPRECATE`

-   Para permitir solo funciones de recuento de caracteres, incluya la siguiente instrucción antes de incluir Strsafe.h.

    `#define STRSAFE_NO_CB_FUNCTIONS`

-   Para permitir solo funciones de recuento de bytes, incluya la siguiente instrucción antes de incluir Strsafe.h.

    `#define STRSAFE_NO_CCH_FUNCTIONS`

    > [!Note]  
    > Puede definir **STRSAFE \_ NO CB \_ FUNCTIONS \_ o** **STRSAFE NO \_ \_ CCH \_ FUNCTIONS**, pero no ambos.

     

-   Algunas funciones strsafe tienen versiones que tienen en cuenta la configuración regional. De forma predeterminada, el encabezado no declara estas funciones. Para habilitar estas declaraciones, incluya la siguiente instrucción de macro antes de incluir Strsafe.h.

    `#define STRSAFE_LOCALE_FUNCTIONS`

-   La longitud máxima de cadena admitida es de 2 147 483 647 caracteres **(STRSAFE \_ MAX \_ CCH),** ya sea ANSI o Unicode.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones strsafe](string-overviews.md)
</dt> </dl>

 

 