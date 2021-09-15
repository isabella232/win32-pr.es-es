---
description: Implementado por el explorador. Expone métodos que administran qué monitor contiene la Windows de tareas en un sistema de supervisión múltiple.
title: IMultiMonitorDockingSite (interfaz)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite
api_type:
- COM
api_location: ''
ms.assetid: af9a7a9e-bd7c-4b17-9cb6-008df5c820d8
ms.openlocfilehash: 5ea3461d00c16f7384d7396e2f03946d517c460f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574549"
---
# <a name="imultimonitordockingsite-interface"></a>IMultiMonitorDockingSite (interfaz)

Implementado por el explorador. Expone métodos que administran qué monitor contiene la Windows de tareas en un sistema de supervisión múltiple.

## <a name="members"></a>Members

La **interfaz IMultiMonitorDockingSite** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IMultiMonitorDockingSite** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMultiMonitorDockingSite** tiene estos métodos.



| Método                                                            | Descripción                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**GetMonitor**](imultimonitordockingsite-getmonitor.md)         | Obtiene el monitor predeterminado actual.<br/>                                               |
| [**RequestMonitor**](imultimonitordockingsite-requestmonitor.md) | Comprueba que el monitor está activo y disponible.<br/>                              |
| [**SetMonitor**](imultimonitordockingsite-setmonitor.md)         | Cambios que se usan para las barras de herramientas acopladas en un sistema de varios monitores.<br/> |



 

## <a name="remarks"></a>Observaciones

Normalmente no se implementa la **interfaz IMultiMonitorDockingSite.** El explorador shell implementa esta interfaz para admitir varios monitores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones \[ de escritorio XP\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                   |



 

 
