---
description: La interfaz IMonitorEventer proporciona métodos para enviar eventos y asignar y liberar recursos de supervisión.
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: Interfaz IMonitorEventer (Netmon.h)
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
ms.openlocfilehash: 2af49529a74c23e0f4d4e77e0d2608cd44d12028d93022750fbbd3af891e2e77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365493"
---
# <a name="imonitoreventer-interface"></a>Interfaz IMonitorEventer

La **interfaz IMonitorEventer proporciona** métodos para enviar eventos y asignar y liberar recursos de supervisión.

## <a name="members"></a>Miembros

La **interfaz IMonitorEventer** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMonitorEventer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMonitorEventer** tiene estos métodos.



| Método                                                 | Descripción                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [**FreeEventData**](imonitoreventer-freeeventdata.md) | Libera espacio asignado para los datos de supervisión.<br/> |
| [**GetEventData**](imonitoreventer-geteventdata.md)   | Asigna espacio para los datos de supervisión.<br/>       |
| [**SendNMEvent**](imonitoreventer-sendnmevent.md)     | Envía eventos a WMI.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

