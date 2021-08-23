---
title: Derecho extendido permitido para autenticar
description: El derecho de acceso de control controla quién puede autenticarse en un determinado equipo o servicio.
ms.assetid: 265e6240-0fb5-4037-8c66-05fadc646100
ms.tgt_platform: multiple
keywords:
- Esquema de AD derecho extendido permitido para autenticar
topic_type:
- apiref
api_name:
- Allowed-To-Authenticate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446a63d63751105500986c27c7a851d60146a72281ee8415bc01c5ec8c5dfa3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548835"
---
# <a name="allowed-to-authenticate-extended-right"></a>Derecho extendido permitido para autenticar

El derecho de acceso de control controla quién puede autenticarse en un determinado equipo o servicio. Básicamente reside en objetos de equipo, usuario e InetOrgPerson. También es aplicable en el objeto de dominio si se permite el acceso para todo el dominio. Se puede aplicar a las us para permitir que los usuarios puedan establecer ACE heredables en os que contengan un conjunto de objetos de usuario o equipo.



| Entrada | Valor |
|--------------|--------------------------------------|
| CN           | Permitido para autenticarse              |
| Display-Name | Se permite autenticarse              |
| Rights-GUID  | 68b1d179-0d15-4d4f-ab71-46152e79a7bc |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**Usuario**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Localization-Display-ID | 65                                                                                                                              |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**Usuario**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Localization-Display-ID | 65                                                                                                                              |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**Usuario**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Localization-Display-ID | 65                                                                                                                              |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-Service-Account**](c-msds-managedserviceaccount.md)<br/> [**Usuario**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Localization-Display-ID | 65                                                                                                                                                                                                               |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-Service-Account**](c-msds-managedserviceaccount.md)<br/> [**Usuario**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Localization-Display-ID | 65                                                                                                                                                                                                               |



 

 





