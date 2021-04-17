---
description: PNRP usa la estructura WSAQUERYSET junto con varias funciones para facilitar la resolución de nombres y la enumeración de nombres y nubes.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP y WSAQUERYSET (P2P. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d09d135d57af0922feb5a143c41696d85dac083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667928"
---
# <a name="pnrp-and-wsaqueryset"></a>PNRP y WSAQUERYSET

PNRP usa la estructura [**WSAQUERYSET**](winsock-nsp-reference-links.md) junto con varias funciones para facilitar la resolución de nombres y la enumeración de nombres y nubes.

Para obtener definiciones completas de las funciones de [**WSAQUERYSET**](winsock-nsp-reference-links.md) o Windows Sockets, consulte sus correspondientes definiciones en la documentación de la API de Windows Sockets 2 en el SDK de la plataforma.

## <a name="wsaqueryset-and-wsasetservice"></a>WSAQUERYSET y WSASetService

La función [**WSASetService**](winsock-nsp-reference-links.md) utiliza la estructura **WSAQUERYSET** para registrar o quitar nombres de mismo nivel. En la página [PNRP y WSASetService](pnrp-and-wsasetservice.md) se describe el uso de la estructura **WSAQUERYSET** con esta función.

## <a name="wsaqueryset-and-wsalookupservicebegin"></a>WSAQUERYSET y WSALookupServiceBegin

La estructura [**WSAQUERYSET**](winsock-nsp-reference-links.md) se usa en gran medida con las funciones **WSALookupServiceBegin**, **WSALookupServiceNext** y **WSALookupServiceEnd** . Los detalles sobre cómo estas funciones usan la estructura **WSAQUERYSET** se detallan en las páginas de referencia siguientes:

-   [PNRP y WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
-   [PNRP y WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
-   [PNRP y WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                             |
| Versión<br/>                  | Windows XP con SP1 con Advanced Networking Pack para Windows XP<br/>  |
| Encabezado<br/>                   | <dl> <dt>P2P. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[PNRP y BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP y WSASetService](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




