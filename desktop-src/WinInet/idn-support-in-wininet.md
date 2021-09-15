---
title: Compatibilidad con IDN en WinINet
description: A partir de Windows Server 2008 y Windows Vista, la parte del host de la dirección URL Unicode se convierte al nombre de dominio internacionalizado (IDN).
ms.assetid: 7c56908e-f6d0-48dc-9ac1-73f888fb7b6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510b1bc8d2ab77534d7f5dac587f287d5e7095af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473293"
---
# <a name="idn-support-in-wininet"></a>Compatibilidad con IDN en WinINet

A partir de Windows Server 2008 y Windows Vista, la parte del host de la dirección URL Unicode se convierte al nombre de dominio internacionalizado (IDN). Las configuraciones establecidas por la aplicación también pueden modificar partes independientes de la codificación de direcciones URL Unicode. Las versiones ANSI de la API de WinINet siguen envíando la dirección URL a través de la conexión especificada por la aplicación, pero las versiones Unicode de WinINet de la API ahora se ajustan al estándar IDN (RFC3490) para las codificaciones de direcciones URL.

De forma predeterminada, cuando se especifica una dirección URL como parámetro Unicode, la parte del host, tanto para las conexiones de proxy como para las conexiones directas, se convierte al formato IDN. La aplicación tiene la opción de deshabilitar el formato de host IDN estableciendo la opción **INTERNET \_ OPTION \_ IDN.** La conversión de host IDN solo se puede habilitar en las conexiones directas o de proxy mediante las marcas INTERNET **\_ FLAG \_ IDN \_ DIRECT** o **INTERNET FLAG \_ \_ IDN \_ PROXY** con **INTERNET OPTION \_ \_ IDN**.

En el ejemplo de código siguiente se muestra cómo deshabilitar la conversión de host IDN para el proxy y las conexiones directas.

``` syntax
DWORD IDN = 0; 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_IDN,
                   &IDN, 
                   sizeof(DWORD) ); 
```

Si el formato de host IDN está deshabilitado, la aplicación tiene la opción de especificar la página de códigos deseada **mediante INTERNET \_ OPTION \_ CODEPAGE**.

En el ejemplo de código siguiente se muestra cómo especificar la página de códigos japonés.

``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS, 
                   Sizeof(DWORD) ); 
```

La parte de la ruta de acceso de la dirección URL está codificada en UTF8 de forma predeterminada y los segmentos restantes de la dirección URL, la consulta o el fragmento, se convierten a la página de códigos del sistema predeterminada (CP \_ ACP).

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
| PÁGINA \_ DE CÓDIGOS DE OPCIÓN DE \_ INTERNET        | Esta opción se establece en la solicitud, o identificador de conexión, para especificar un esquema de codificación de página de códigos para la parte host de la dirección URL. Esta opción se omite si IDN está habilitado.                                                      |
| RUTA DE \_ ACCESO DE PÁGINA DE CÓDIGOS DE OPCIÓN DE \_ \_ INTERNET  | Esta opción se establece en la solicitud o el identificador de conexión habilita el esquema de codificación especificado para la parte de la ruta de acceso de la dirección URL. De forma predeterminada, la parte de la ruta de acceso de la dirección URL está codificada en UTF8.                                         |
| OPCIÓN DE INTERNET \_ \_ CODEPAGE \_ EXTRA | Al establecer esta opción en la solicitud o el identificador de conexión, se habilita el esquema de codificación especificado para la parte adicional de la dirección URL. De forma predeterminada, la parte adicional de la dirección URL se codifica en la página de códigos del sistema predeterminada (CP \_ ACP). |
| IDN \_ DE \_ OPCIÓN DE INTERNET             | Esta opción se puede usar en la solicitud o en el identificador de conexión para habilitar o deshabilitar la conversión de host IDN. Cuando IDN está deshabilitado, WinINet usa la página de códigos del sistema predeterminada para codificar la parte del host o la autoridad de la dirección URL.       |



 

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para implementaciones de servidor o servicios, use [Microsoft Windows servicios HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 