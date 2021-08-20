---
title: Compatibilidad con ip versión 6
description: A partir de IE7 y posteriores, WinINet admite literales IPv6 en el nombre de host y el componente de autoridad del URI.
ms.assetid: cbbb9f93-15b0-4017-ac39-8a396203532e
keywords:
- Compatibilidad con ip versión 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a024c792995780769a078c84b0493b7abba8647189fa2cee835d93dcb83770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113635"
---
# <a name="ip-version-6-support"></a>Compatibilidad con ip versión 6

A partir de IE7 y posteriores, WinINet admite literales IPv6 en el nombre de host y el componente de autoridad del URI. WinINet también admite el uso de literales IPv6 en partes pertinentes del protocolo HTTP, como en el encabezado Location.

## <a name="hostname-ipv6-literals-and-uri-components"></a>Literales IPv6 de nombre de host y componentes uri

WinINet implementa literales IPv6 según las especificaciones de RFC 3513. Como se especifica en esta RFC, los literales IPv6 de un URI deben ir entre corchetes. Por ejemplo, https:// ::1 / es un URI IPv6 válido; el formulario sin \[ \] corchetes ( https://::1/) no es válido. Sin embargo, no es necesario incluir los literales IPv6 de nombre de host que no forman parte del URI entre corchetes. Cualquier forma es aceptable para WinINet. Por ejemplo, "::1" y \[ "::1" son formas aceptables de literales de nombre de \] host IPv6. Otras API, como WinSock API, también aceptarán ambos formularios. Por lo tanto, las aplicaciones deben estar preparadas para controlar ambas formas de literales de nombre de host IPv6.

## <a name="scope-id"></a>El identificador de ámbito

La dirección literal IPv6 en el URI puede incluir un identificador de ámbito. Un identificador de ámbito puede ser un identificador de interfaz como \[ FE80::1%1. \] El estándar uri, documentado en RFC 3986, no define la sintaxis del identificador de ámbito y el URI se considera no uniforme cuando el identificador de ámbito está presente. Sin embargo, WinINet acepta un identificador de ámbito en el componente de autoridad del URI y en el literal IPv6 del nombre de host.

El carácter de porcentaje (%) de la dirección literal IPv6 debe ser de escape por porcentaje cuando esté presente en el URI. Por ejemplo, el identificador de ámbito FE80::2%3 debe aparecer en el URI como "https:// \[ FE80::2%253 /", donde %25 es el carácter de porcentaje codificado hexadecimal \] (%). Si la aplicación recupera el URI de una API Unicode, como winsock [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) API, la aplicación debe agregar la versión con escape del carácter de porcentaje (%) en el nombre de host del URI. Para crear la versión con escape del URI, las aplicaciones llaman a [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) con el parámetro *dwFlags* establecido en **ICU \_ ESCAPE \_ AUTHORITY** y el nombre de host IPv6 especificado en la estructura de componentes de dirección URL especificada en el parámetro *lpUrlComponents.*

Para todas las operaciones de sockets, WinINet usa el identificador de ámbito. Sin embargo, dado que el identificador de ámbito solo tiene importancia de host local, no se envía como parte de los encabezados del protocolo HTTP en la solicitud. Por ejemplo, se llama a [**la llamada a InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) con la siguiente dirección URL en el *parámetro lpszUrl.*

``` syntax
https://[fec0::2%251]:80/path.htm
```

WinINet quita la parte del identificador de ámbito de la dirección URL cuando se envía la solicitud HTTP para esta dirección URL. La solicitud contiene los encabezados siguientes:

``` syntax
GET path.htm HTTP/1.1
Host: [fec0::2]
```

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 