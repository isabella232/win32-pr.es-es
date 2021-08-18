---
description: PNRP usa la estructura WSAQUERYSET junto con varias funciones para facilitar la resolución de nombres y la enumeración de nombres y nubes.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP y WSAQUERYSET (P2P.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bbc635b0c1ca19cfaeeeb7f8b013aefad1e49e2141dd9715a36c0238e7be6f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061363"
---
# <a name="pnrp-and-wsaqueryset"></a>PNRP y WSAQUERYSET

PNRP usa la [**estructura WSAQUERYSET**](winsock-nsp-reference-links.md) junto con varias funciones para facilitar la resolución de nombres y la enumeración de nombres y nubes.

Para obtener definiciones completas de las funciones [**WSAQUERYSET**](winsock-nsp-reference-links.md) o Windows Sockets, consulte sus respectivas definiciones en la documentación de la API de Windows Sockets 2 en el SDK de plataforma.

## <a name="wsaqueryset-and-wsasetservice"></a>WSAQUERYSET y WSASetService

La [**función WSASetService**](winsock-nsp-reference-links.md) usa la **estructura WSAQUERYSET** para registrar o quitar nombres del mismo nivel. En [la página PNRP y WSASetService](pnrp-and-wsasetservice.md) se describe cómo usar la **estructura WSAQUERYSET** con esta función.

## <a name="wsaqueryset-and-wsalookupservicebegin"></a>WSAQUERYSET y WSALookupServiceBegin

La [**estructura WSAQUERYSET**](winsock-nsp-reference-links.md) se usa ampliamente con las funciones **WSALookupServiceBegin,** **WSALookupServiceNext** y **WSALookupServiceEnd.** Los detalles sobre cómo estas funciones usan **la estructura WSAQUERYSET** se detallan en las siguientes páginas de referencia:

-   [PNRP y WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
-   [PNRP y WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
-   [PNRP y WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                             |
| Versión<br/>                  | Windows XP con SP1 con advanced networking pack for Windows XP<br/>  |
| Header<br/>                   | <dl> <dt>P2P.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[PNRP y BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP y WSASetService](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




