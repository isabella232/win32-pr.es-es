---
title: Tipos de datos del servicio de acceso remoto (Ras.h)
description: La API del servicio de acceso remoto usa los siguientes tipos de datos.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26df8b8336b9b96ec338a79ed846519fb8a0ca019e6dd5996b9ac17087faa371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028255"
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

Un [**complemento \_ de que**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) contiene una dirección IPv4.

> [!Note]  
> Compatible con Windows Vista o versiones posteriores de Windows.

 

</dd> <dt>

**RASIPV6ADDR**
</dt> <dd>

Un [**complemento in6 \_ que**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) contiene una dirección IPv6.

> [!Note]  
> Compatible con Windows Vista o versiones posteriores de Windows.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Ras.h</dt> </dl> |



 

