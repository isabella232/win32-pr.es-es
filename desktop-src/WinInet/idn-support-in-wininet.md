---
title: Compatibilidad con IDN en WinINet
description: A partir de Windows Server 2008 y Windows Vista, la parte del host de la dirección URL de Unicode se convierte en el nombre de dominio internacionalizado (IDN).
ms.assetid: 7c56908e-f6d0-48dc-9ac1-73f888fb7b6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510b1bc8d2ab77534d7f5dac587f287d5e7095af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421277"
---
# <a name="idn-support-in-wininet"></a>Compatibilidad con IDN en WinINet

A partir de Windows Server 2008 y Windows Vista, la parte del host de la dirección URL de Unicode se convierte en el nombre de dominio internacionalizado (IDN). Las configuraciones establecidas por la aplicación también pueden modificar partes independientes de la codificación de la dirección URL de Unicode. Las versiones ANSI de la API WinINet continúan enviando la dirección URL a través de la conexión tal como la escribe la aplicación; sin embargo, las versiones de WinINet Unicode de la API ahora se ajustan al estándar IDN (RFC3490) para las codificaciones de direcciones URL.

De forma predeterminada, cuando se especifica una dirección URL como un parámetro Unicode, la parte del host, para conexiones proxy y directas, se convierte al formato IDN. La aplicación tiene la opción de deshabilitar el formato de host de IDN estableciendo la opción de **Internet \_ \_ IDN** . La conversión de host de IDN solo se puede habilitar en las conexiones directas o de proxy mediante las marcas de **Internet \_ marca \_ IDN \_ Direct** o de **\_ \_ \_ proxy IDN de marca** de Internet con la **opción de Internet \_ \_ IDN**.

En el ejemplo de código siguiente se muestra cómo deshabilitar la conversión de host IDN para conexiones proxy y directas.

``` syntax
DWORD IDN = 0; 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_IDN,
                   &IDN, 
                   sizeof(DWORD) ); 
```

Si el formato de host de IDN está deshabilitado, la aplicación tiene la opción de especificar la página de códigos deseada mediante la **\_ Página de \_ códigos** de la opción de Internet.

En el ejemplo de código siguiente se muestra cómo especificar la página de códigos japonesa.

``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS, 
                   Sizeof(DWORD) ); 
```

La parte de la ruta de acceso de la dirección URL está codificada de forma predeterminada y el resto de los segmentos de la dirección URL, la consulta o el fragmento, se convierten en la página de códigos predeterminada del sistema (CP \_ ACP).

En el ejemplo siguiente se muestra cómo especificar la página de códigos del idioma coreano para la parte de la ruta de acceso de la dirección URL.

``` syntax
DWORD CP_KOREAN = 949;   // ANSI/OEM Korean 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE_PATH,
                   &CP_KOREAN, 
                   sizeof(DWORD) );
```

En la tabla siguiente se definen las opciones que admiten IDN. Para obtener más información, vea el tema [Option Flags](option-flags.md) .



| Opción                            | Descripción                                                                                                                                                                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Página de códigos de la opción de INTERNET \_ \_        | Esta opción se establece en la solicitud o en el identificador de conexión para especificar un esquema de codificación de página de códigos para la parte del host de la dirección URL. Esta opción se omite si se habilita IDN.                                                      |
| \_ruta de \_ acceso de página de la opción de Internet \_  | Esta opción se establece en la solicitud, o el identificador de conexión habilita el esquema de codificación especificado para la parte de la ruta de acceso de la dirección URL. De forma predeterminada, la parte de la ruta de acceso de la dirección URL está codificada en UTF8.                                         |
| Página de códigos de opciones de INTERNET \_ \_ \_ extra | Al establecer esta opción en la solicitud o el identificador de conexión, se habilita el esquema de codificación especificado para la parte adicional de la dirección URL. De forma predeterminada, la parte adicional de la dirección URL se codifica en la página de códigos predeterminada del sistema (CP \_ ACP). |
| Opciones de INTERNET \_ \_ IDN             | Esta opción se puede usar en la solicitud o el identificador de conexión para habilitar o deshabilitar la conversión de host de IDN. Cuando se deshabilita IDN, WinINet utiliza la página de códigos predeterminada del sistema para codificar la parte de host o de autoridad de la dirección URL.       |



 

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 