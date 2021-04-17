---
description: En la tabla siguiente se \_ describen \_ las opciones de socket de tipo de tráfico de DSCP IP \_ .
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
ms.openlocfilehash: 80cbe41e58cf36cd366015d83af380f5952630ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653649"
---
# <a name="ip_dscp_traffic_type"></a>\_tipo de \_ tráfico IP DSCP \_

En la tabla siguiente se \_ describen \_ las opciones de socket de tipo de tráfico de DSCP IP \_ .

<dl> <dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**\_tipo de \_ tráfico IP DSCP \_**</dt> <dd> <dl> <dt> 

| Opción              | Obtener | Set | Tipo Optval | Descripción                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_tipo de tráfico de DSCP \_ | Sí | Sí | DWORD       | Al establecer este valor en los valores definidos en el **\_ \_ tipo de tráfico de DSCP**, una aplicación podrá solicitar que los paquetes de red se traten según el tipo de servicio que se solicita. De forma similar, se pueden utilizar llamadas a [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para obtener la configuración actual del tipo de tráfico solicitado en el socket dado. |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|--------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows 10<br/>                                                          |
| Fin de compatibilidad de servidor<br/> | Windows Server 2016<br/>                                                 |
| Encabezado<br/>                | <dl> <dt>N/D</dt> </dl> |



 

 




