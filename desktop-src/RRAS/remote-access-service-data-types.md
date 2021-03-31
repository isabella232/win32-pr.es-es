---
title: Tipos de datos del servicio de acceso remoto (RAS. h)
description: La API del servicio de acceso remoto usa los siguientes tipos de datos.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8aa2fdae531c5aae0986d3289802565c6914fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996358"
---
# <a name="remote-access-service-data-types"></a>Tipos de datos del servicio de acceso remoto

La API del servicio de acceso remoto usa los siguientes tipos de datos.


```C++
typedef in_addr RASIPV4ADDR;
typedef in6_addr RASIPV6ADDR;
```



<dl> <dt>

**RASIPV4ADDR**
</dt> <dd>

[**En \_ addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) que contiene una dirección IPv4.

> [!Note]  
> Compatible con Windows Vista o versiones posteriores de Windows.

 

</dd> <dt>

**RASIPV6ADDR**
</dt> <dd>

Una [**dirección \_ IN6**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) que contiene una dirección IPv6.

> [!Note]  
> Compatible con Windows Vista o versiones posteriores de Windows.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Ras. h</dt> </dl> |



 

