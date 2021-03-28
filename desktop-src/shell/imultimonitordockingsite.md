---
description: Implementado por el explorador. Expone métodos que administran el monitor que contiene la barra de tareas de Windows en un sistema de varios monitores.
title: Interfaz IMultiMonitorDockingSite
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
ms.openlocfilehash: 3aa1ccb1c25fd2896ce9e18ba52ea3f46b1882af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997965"
---
# <a name="imultimonitordockingsite-interface"></a>Interfaz IMultiMonitorDockingSite

Implementado por el explorador. Expone métodos que administran el monitor que contiene la barra de tareas de Windows en un sistema de varios monitores.

## <a name="members"></a>Miembros

La interfaz **IMultiMonitorDockingSite** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMultiMonitorDockingSite** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IMultiMonitorDockingSite** tiene estos métodos.



| Método                                                            | Descripción                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**GetMonitor**](imultimonitordockingsite-getmonitor.md)         | Obtiene el monitor predeterminado actual.<br/>                                               |
| [**RequestMonitor**](imultimonitordockingsite-requestmonitor.md) | Comprueba que el monitor está activo y disponible.<br/>                              |
| [**SetMonitor**](imultimonitordockingsite-setmonitor.md)         | Cambia el monitor que se usa para las barras de herramientas acopladas en un sistema de varios monitores.<br/> |



 

## <a name="remarks"></a>Observaciones

Normalmente no se implementa la interfaz **IMultiMonitorDockingSite** . El explorador de Shell implementa esta interfaz para admitir varios monitores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                   |



 

 
