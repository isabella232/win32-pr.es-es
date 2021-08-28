---
title: Compatibilidad con IDN en WinINet
description: A partir de Windows Server 2008 y Windows Vista, la parte del host de la dirección URL Unicode se convierte en el nombre de dominio internacionalizado (IDN).
ms.assetid: 7c56908e-f6d0-48dc-9ac1-73f888fb7b6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 998005ff6d46a768403c9c3a18ac14457139ee871fe135fb1306ad677e9e029a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071685"
---
# <a name="idn-support-in-wininet"></a>Compatibilidad con IDN en WinINet

A partir de Windows Server 2008 y Windows Vista, la parte del host de la dirección URL Unicode se convierte en el nombre de dominio internacionalizado (IDN). Las configuraciones establecidas por la aplicación también pueden modificar partes independientes de la codificación de direcciones URL Unicode. Las versiones ANSI de la API de WinINet siguen envíando la dirección URL a través de la conexión especificada por la aplicación; sin embargo, las versiones Unicode de WinINet de la API ahora se ajustan al estándar IDN (RFC3490) para codificaciones de direcciones URL.

De forma predeterminada, cuando se especifica una dirección URL como un parámetro Unicode, la parte del host, tanto para conexiones directas como proxy, se convierte al formato IDN. La aplicación tiene la opción de deshabilitar el formato de host IDN estableciendo la opción **INTERNET \_ OPTION \_ IDN.** La conversión de host IDN solo se puede habilitar en las conexiones directas o proxy mediante las marcas DE PROXY DE **\_ \_ IDN DIRECT \_** o INTERNET FLAG **\_ \_ IDN \_** con INTERNET OPTION **\_ \_ IDN**.

En el ejemplo de código siguiente se muestra cómo deshabilitar la conversión de host IDN tanto para el proxy como para las conexiones directas.

``` syntax
DWORD IDN = 0; 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_IDN,
                   &IDN, 
                   sizeof(DWORD) ); 
```

Si el formato de host IDN está deshabilitado, la aplicación tiene la opción de especificar la página de códigos deseada **mediante INTERNET \_ OPTION \_ CODEPAGE**.

En el ejemplo de código siguiente se muestra cómo especificar la página de códigos japonesa.

``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS, 
                   Sizeof(DWORD) ); 
```

La parte de la ruta de acceso de la dirección URL está codificada en UTF8 de forma predeterminada y los segmentos restantes de la dirección URL, la consulta o el fragmento, se convierten en la página de códigos del sistema predeterminada \_ (CP ACP).

En el ejemplo siguiente se muestra cómo especificar la página de códigos del idioma coreano para la parte de la ruta de acceso de la dirección URL.

``` syntax
DWORD CP_KOREAN = 949;   // ANSI/OEM Korean 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE_PATH,
                   &CP_KOREAN, 
                   sizeof(DWORD) );
```

En la tabla siguiente se definen las opciones que admiten IDN. Para obtener más información, vea el [tema Marcas de](option-flags.md) opción.



| Opción                            | Descripción                                                                                                                                                                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PÁGINA \_ DE CÓDIGOS DE OPCIÓN DE \_ INTERNET        | Esta opción se establece en la solicitud, o identificador de conexión, para especificar un esquema de codificación de página de códigos para la parte host de la dirección URL. Esta opción se omite si idn está habilitado.                                                      |
| RUTA DE \_ ACCESO DE PÁGINA DE CÓDIGOS DE OPCIÓN DE \_ \_ INTERNET  | Esta opción se establece en la solicitud o el identificador de conexión habilita el esquema de codificación especificado para la parte de la ruta de acceso de la dirección URL. De forma predeterminada, la parte de la ruta de acceso de la dirección URL está codificada en UTF8.                                         |
| OPCIÓN DE INTERNET \_ \_ CODEPAGE \_ EXTRA | Al establecer esta opción en la solicitud o el identificador de conexión, se habilita el esquema de codificación especificado para la parte adicional de la dirección URL. De forma predeterminada, la parte adicional de la dirección URL se codifica en la página de códigos del sistema predeterminada (CP \_ ACP). |
| IDN \_ DE OPCIÓN \_ DE INTERNET             | Esta opción se puede usar en la solicitud o en el identificador de conexión para habilitar o deshabilitar la conversión de host IDN. Cuando IDN está deshabilitado, WinINet usa la página de códigos del sistema predeterminada para codificar la parte del host o la autoridad de la dirección URL.       |



 

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows HTTP Services (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 