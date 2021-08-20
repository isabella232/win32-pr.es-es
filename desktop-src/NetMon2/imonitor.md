---
description: La interfaz IMonitor proporciona métodos que controlan el funcionamiento del monitor. El Servicio de control de supervisión (MCSVC) llama a estos métodos.
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: Interfaz IMonitor (Netmon.h)
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
ms.openlocfilehash: 16199568473315fb61e53428d01c72032f3efff6ea0591bfd72ca2475f854fb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133106"
---
# <a name="imonitor-interface"></a>Interfaz IMonitor

La **interfaz IMonitor** proporciona métodos que controlan la operación de supervisión. El Servicio de [*control de supervisión*](m.md) (MCSVC) llama a estos métodos.

## <a name="members"></a>Miembros

La **interfaz IMonitor** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMonitor** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMonitor** tiene estos métodos.



| Método                                        | Descripción                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**DoConfigure**](imonitor-doconfigure.md)   | Actualiza la configuración del monitor.<br/>                                                                           |
| [**DoInitialize**](imonitor-doinitialize.md) | Inicializa un monitor.<br/>                                                                                   |
| [**OnFrames**](imonitor-onframes.md)         | Indica el estado de un evento de marco.<br/>                                                                   |
| [**OnStart**](imonitor-onstart.md)           | Indica que el monitor se ha configurado correctamente y que la captura de datos está a punto de comenzar.<br/> |
| [**OnStatus**](imonitor-onstatus.md)         | Indica un evento de estado de NPP.<br/>                                                                           |
| [**OnStop**](imonitor-onstop.md)             | Indica la finalización de la captura de datos.<br/>                                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

