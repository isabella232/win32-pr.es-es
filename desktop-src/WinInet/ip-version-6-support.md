---
title: Compatibilidad con IP versión 6
description: A partir de IE7 y versiones posteriores, WinINet admite los literales IPv6 en el nombre de host y el componente de autoridad del URI.
ms.assetid: cbbb9f93-15b0-4017-ac39-8a396203532e
keywords:
- Compatibilidad con IP versión 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed0857d9a0968bcd3e6c18e54623fb0c7d86cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421219"
---
# <a name="ip-version-6-support"></a>Compatibilidad con IP versión 6

A partir de IE7 y versiones posteriores, WinINet admite los literales IPv6 en el nombre de host y el componente de autoridad del URI. WinINet también admite el uso de literales de IPv6 en partes relevantes del protocolo HTTP, como en el encabezado de ubicación.

## <a name="hostname-ipv6-literals-and-uri-components"></a>Nombres de host y literales IPv6

WinINet implementa los literales de IPv6 según las especificaciones de RFC 3513. Tal y como se especifica en esta RFC, los literales IPv6 de un URI deben ir entre corchetes. Por ejemplo, https:// \[ :: 1 \] /es un URI de IPv6 válido; el formulario sin corchetes ( https://::1/) no es válido. Sin embargo, no es necesario incluir en los corchetes los literales de nombre de host IPv6 que no forman parte del URI; cualquier formulario es aceptable para WinINet. Por ejemplo, ":: 1" y " \[ :: 1 \] " son formas aceptables de los literales de nombre de host de IPv6. Otras API, como la API de WinSock, también aceptarán ambos formularios. Por lo tanto, las aplicaciones deben estar preparadas para controlar ambos tipos de literales de nombre de host de IPv6.

## <a name="scope-id"></a>El identificador de ámbito

La dirección literal IPv6 en el URI puede incluir un identificador de ámbito. Un identificador de ámbito puede ser un identificador de interfaz como \[ fe80:: 1% 1 \] . La norma del URI, documentada en RFC 3986, no define la sintaxis del identificador de ámbito y el URI se considera no uniforme cuando el identificador de ámbito está presente. Sin embargo, WinINet acepta un identificador de ámbito en el componente de autoridad del URI y en el literal IPv6 del nombre de host.

El carácter de porcentaje (%) en, la dirección del literal IPv6 debe ser el porcentaje de escape cuando esté presente en el URI. Por ejemplo, el ID. de ámbito FE80:: 2% 3, debe aparecer en el URI como "https:// \[ fe80:: 2% 253 \] /", donde %25 es el carácter de porcentaje codificado hexadecimal (%). Si la aplicación recupera el URI de una API de Unicode, como Winsock [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) API, la aplicación debe agregar la versión con escape del carácter de porcentaje (%). en el nombre de host del URI. Para crear la versión con escape del URI, las aplicaciones llaman a [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) con el parámetro *dwFlags* establecido en la **\_ \_ autoridad de escape ICU** y el nombre de host IPv6 especificado en la estructura de componentes URL especificada en el parámetro *lpUrlComponents* .

Para todas las operaciones de sockets, WinINet usa el identificador de ámbito. Sin embargo, dado que el identificador de ámbito solo tiene significado de host local, no se envía como parte de los encabezados de protocolo HTTP en la solicitud. Por ejemplo, se llama a la llamada a [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) con la siguiente dirección URL en el parámetro *lpszUrl* .

``` syntax
https://[fec0::2%251]:80/path.htm
```

WinINet quita la parte del identificador de ámbito de la dirección URL cuando se envía la solicitud HTTP para esta dirección URL. La solicitud contiene los encabezados siguientes:

``` syntax
GET path.htm HTTP/1.1
Host: [fec0::2]
```

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 