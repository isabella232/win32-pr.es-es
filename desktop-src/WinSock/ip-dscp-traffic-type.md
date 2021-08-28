---
description: En la tabla siguiente se describen las opciones \_ de socket de TIPO DE TRÁFICO \_ DSCP de \_ IP.
ms.assetid: 0042B53F-B84E-453A-8E18-87052280DAD5
title: IP_DSCP_TRAFFIC_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IP_DSCP_TRAFFIC_TYPE
api_type:
- HeaderDef
api_location:
- N/A
ms.openlocfilehash: 87915dc214b0ba306b4f38dbd833b27199277564fa8c2815b9147e0d82253589
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097855"
---
# <a name="ip_dscp_traffic_type"></a>TIPO \_ DE TRÁFICO DSCP DE \_ \_ IP

En la tabla siguiente se describen las opciones \_ de socket de TIPO DE TRÁFICO \_ DSCP de \_ IP.

<dl> <dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**TIPO \_ DE TRÁFICO DSCP DE \_ \_ IP**</dt> <dd> <dl> <dt> 

| Opción              | Obtener | Set | Tipo optval | Descripción                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TIPO DE TRÁFICO \_ \_ DSCP | Sí | Sí | DWORD       | Al establecer este valor en valores definidos en **DSCP \_ TRAFFIC \_ TYPE**, una aplicación podrá pedir a sus paquetes de red que se traten según el tipo de servicio que se solicita. De forma similar, se pueden usar llamadas a [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para obtener la configuración actual del tipo de tráfico solicitado en el socket especificado. |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|--------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows 10<br/>                                                          |
| Fin de compatibilidad de servidor<br/> | Windows Server 2016<br/>                                                 |
| Header<br/>                | <dl> <dt>N/D</dt> </dl> |



 

 




