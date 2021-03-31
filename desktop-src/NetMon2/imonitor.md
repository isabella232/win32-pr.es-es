---
description: La interfaz IMonitor proporciona métodos que controlan la operación de supervisión. El servicio de control de supervisión (MCSVC) llama a estos métodos.
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: Interfaz IMonitor (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 1b6ba91860905010fd14a46cd4608eaee3da80fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908301"
---
# <a name="imonitor-interface"></a>Interfaz IMonitor

La interfaz **IMonitor** proporciona métodos que controlan la operación de supervisión. El [*servicio de control de supervisión*](m.md) (MCSVC) llama a estos métodos.

## <a name="members"></a>Miembros

La interfaz **IMonitor** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMonitor** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IMonitor** tiene estos métodos.



| Método                                        | Descripción                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**Configurar**](imonitor-doconfigure.md)   | Actualiza la configuración del monitor.<br/>                                                                           |
| [**Inicializar**](imonitor-doinitialize.md) | Inicializa un monitor.<br/>                                                                                   |
| [**Marcos**](imonitor-onframes.md)         | Indica el estado de un evento de marco.<br/>                                                                   |
| [**OnStart**](imonitor-onstart.md)           | Indica que el monitor se ha configurado correctamente y que la captura de datos está a punto de comenzar.<br/> |
| [**OnStatus**](imonitor-onstatus.md)         | Indica un evento de estado NPP.<br/>                                                                           |
| [**OnStop**](imonitor-onstop.md)             | Indica la finalización de la captura de datos.<br/>                                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

