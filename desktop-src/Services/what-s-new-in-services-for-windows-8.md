---
description: Windows 8 y Windows Server 2012 incluyen las siguientes nuevas funcionalidades para los servicios.
ms.assetid: 42BC7325-4FAC-493E-95AC-AEF660F499C0
title: Novedades de los servicios para Windows 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc5b3b97bda816a2c8676d55d670deecea3222482776a01e8dccf314326a608a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888137"
---
# <a name="whats-new-in-services-for-windows-8"></a>Novedades de los servicios para Windows 8

Windows 8 y Windows Server 2012 incluyen las siguientes nuevas funcionalidades para los servicios.

## <a name="new-service-functions"></a>Nuevas funciones de servicio



| Función                                                                            | Descripción                                                                    |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)<br/> | Recupera información dinámica relacionada con el inicio del servicio actual.<br/> |



 

## <a name="updated-api-elements"></a>Elementos de API actualizados



| Elemento de API                                                                                     | Descripción                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)<br/>                                                       | Se ha agregado **CONTROL \_ DE SERVICIO \_ USERMODEREBOOT.**<br/>                                                                                                        |
| [**ESTADO DEL \_ SERVICIO**](/windows/desktop/api/Winsvc/ns-winsvc-service_status)<br/>                                        | Se ha **agregado SERVICE \_ ACCEPT \_ USERMODEREBOOT**.<br/>                                                                                                         |
| [**ELEMENTO DE \_ DATOS ESPECÍFICO DEL DESENCADENADOR DE \_ \_ \_ SERVICIO**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_specific_data_item)<br/> | Se ha agregado **SERVICE TRIGGER DATA TYPE \_ \_ \_ \_ LEVEL**, **SERVICE TRIGGER DATA TYPE KEYWORD \_ \_ \_ \_ \_ ANY** y **SERVICE TRIGGER DATA TYPE KEYWORD \_ \_ \_ \_ \_ ALL**.<br/> |



 

 

 




