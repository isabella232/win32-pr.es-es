---
description: La interfaz IMonitorEventer proporciona métodos para enviar eventos y asignar y liberar recursos de supervisión.
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: Interfaz IMonitorEventer (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 7d4ca58b5a0787638eee54b7733b4e1a8fbf7ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907871"
---
# <a name="imonitoreventer-interface"></a>Interfaz IMonitorEventer

La interfaz **IMonitorEventer** proporciona métodos para enviar eventos y asignar y liberar recursos de supervisión.

## <a name="members"></a>Miembros

La interfaz **IMonitorEventer** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMonitorEventer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IMonitorEventer** tiene estos métodos.



| Método                                                 | Descripción                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [**FreeEventData**](imonitoreventer-freeeventdata.md) | Libera el espacio asignado para los datos del monitor.<br/> |
| [**GetEventData**](imonitoreventer-geteventdata.md)   | Asigna espacio para supervisar los datos.<br/>       |
| [**SendNMEvent**](imonitoreventer-sendnmevent.md)     | Envía eventos a WMI.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

