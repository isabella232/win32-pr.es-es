---
title: Interfaz IRDVTaskPlugin
description: La interfaz IRDVTaskPlugin se implementa mediante un agente de tareas de actualización de la máquina virtual para permitir que el agente de tareas Administre las actualizaciones del sistema de una máquina virtual.
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IRDVTaskPlugin
- Servicios de Escritorio remoto de la interfaz IRDVTaskPlugin, descrito
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59e90e899e8084f7fbc6b0b6f11067061eaa807b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997077"
---
# <a name="irdvtaskplugin-interface"></a>Interfaz IRDVTaskPlugin

La interfaz **IRDVTaskPlugin** se implementa mediante un *agente de tareas* de actualización de la máquina virtual para permitir que el agente de tareas Administre las actualizaciones del sistema de una máquina virtual. Esta interfaz la usa el *agente de desencadenador*, que se implementa mediante el sistema host.

## <a name="members"></a>Miembros

La interfaz **IRDVTaskPlugin** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IRDVTaskPlugin** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IRDVTaskPlugin** tiene estos métodos.



| Método                                          | Descripción                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [**Inicialización**](irdvtaskplugin-initialize.md) | Se llama para inicializar el agente de tareas.<br/>                    |
| [**StartTask**](irdvtaskplugin-starttask.md)   | Se llama para iniciar la tarea de actualización en la máquina virtual.<br/> |
| [**Terminate**](irdvtaskplugin-terminate.md)   | Se llama cuando se está cerrando el agente de tareas.<br/>          |



 

### <a name="properties"></a>Propiedades

La interfaz **IRDVTaskPlugin** tiene estas propiedades.



| Propiedad                                                   | Tipo de acceso          | Descripción                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [**PluginName**](irdvtaskplugin-pluginname.md)<br/> | Solo lectura<br/> | Contiene el nombre para mostrar del agente de tareas.<br/> |



 

## <a name="remarks"></a>Observaciones

El agente de tareas se ejecuta en la máquina virtual cuando la máquina virtual está programada para una actualización del sistema. El agente de tareas actualiza la máquina virtual cuando se llama al método [**StartTask**](irdvtaskplugin-starttask.md) .

Para registrar el agente de tareas, agregue la siguiente clave al registro de la máquina virtual:

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Terminal Server** \\  \\ **Complementos** de tareas \\ **TaskAgentName**

En esta clave del registro, agregue los siguientes valores:



| Nombre                     | Tipo                      | Descripción                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| **CLSID**<br/>     | **Registro \_ SZ**<br/>    | Cadena que representa el **CLSID** del agente de tareas.<br/>          |
| **IsEnabled**<br/> | **\_valor DWORD reg**<br/> | 0 si el agente de tareas está deshabilitado o 1 si está habilitado el agente de tareas.<br/> |



 

> [!Note]  
> Se puede registrar más de un agente de tareas, pero solo se usará un agente de tareas. Si hay más de un agente de tareas habilitado, solo se usará el primero que se encuentre.

 

Aunque esta interfaz es compatible con los sistemas operativos identificados en los requisitos siguientes, solo se usará si la máquina virtual está hospedada en Windows Server 2012.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



 

