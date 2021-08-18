---
description: Implementado por el explorador. Expone métodos que administran qué monitor contiene la Windows de tareas en un sistema de varios monitores.
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
ms.openlocfilehash: a5a17e8206af8f0821833f4b2ea250606de29b6fbe74b7a29ced6c5b5dc13ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458225"
---
# <a name="imultimonitordockingsite-interface"></a>IMultiMonitorDockingSite (interfaz)

Implementado por el explorador. Expone métodos que administran qué monitor contiene la Windows de tareas en un sistema de varios monitores.

## <a name="members"></a>Miembros

La **interfaz IMultiMonitorDockingSite** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IMultiMonitorDockingSite** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMultiMonitorDockingSite** tiene estos métodos.



| Método                                                            | Descripción                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**GetMonitor**](imultimonitordockingsite-getmonitor.md)         | Obtiene el monitor predeterminado actual.<br/>                                               |
| [**RequestMonitor**](imultimonitordockingsite-requestmonitor.md) | Comprueba que el monitor está activo y disponible.<br/>                              |
| [**SetMonitor**](imultimonitordockingsite-setmonitor.md)         | Cambios que se usan para las barras de herramientas acopladas en un sistema de varios monitores.<br/> |



 

## <a name="remarks"></a>Comentarios

Normalmente no se implementa la **interfaz IMultiMonitorDockingSite.** El explorador shell implementa esta interfaz para admitir varios monitores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                   |



 

 
