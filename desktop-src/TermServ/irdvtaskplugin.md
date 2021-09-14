---
title: Interfaz IRDVTaskPlugin
description: La interfaz IRDVTaskPlugin se implementa mediante un agente de tareas de actualización de máquina virtual para permitir que el agente de tareas administre las actualizaciones del sistema de una máquina virtual.
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- Interfaz IRDVTaskPlugin Servicios de Escritorio remoto
- Interfaz IRDVTaskPlugin Servicios de Escritorio remoto , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168658"
---
# <a name="irdvtaskplugin-interface"></a>Interfaz IRDVTaskPlugin

La **interfaz IRDVTaskPlugin** se implementa mediante  un agente de tareas de actualización de máquina virtual para permitir que el agente de tareas administre las actualizaciones del sistema de una máquina virtual. El agente de desencadenador usa esta interfaz *,* que se implementa mediante el sistema host.

## <a name="members"></a>Members

La **interfaz IRDVTaskPlugin** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IRDVTaskPlugin** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IRDVTaskPlugin** tiene estos métodos.



| Método                                          | Descripción                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [**Inicialización**](irdvtaskplugin-initialize.md) | Se llama para inicializar el agente de tareas.<br/>                    |
| [**StartTask**](irdvtaskplugin-starttask.md)   | Se llama para iniciar la tarea de actualización en la máquina virtual.<br/> |
| [**Terminate**](irdvtaskplugin-terminate.md)   | Se llama cuando se está cerrando el agente de tareas.<br/>          |



 

### <a name="properties"></a>Propiedades

La **interfaz IRDVTaskPlugin** tiene estas propiedades.



| Propiedad                                                   | Tipo de acceso          | Descripción                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [**PluginName**](irdvtaskplugin-pluginname.md)<br/> | Solo lectura<br/> | Contiene el nombre para mostrar del agente de tareas.<br/> |



 

## <a name="remarks"></a>Observaciones

El agente de tareas se ejecuta en la máquina virtual cuando esa máquina virtual está programada para una actualización del sistema. El agente de tareas actualiza la máquina virtual cuando se [**llama al método StartTask.**](irdvtaskplugin-starttask.md)

Para registrar el agente de tareas, agregue la siguiente clave al registro de la máquina virtual:

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft Windows** \\ **NT** \\ **CurrentVersion** Terminal \\ **Server** \\ **Task** \\ **Plugins** \\ **TaskAgentName**

En esta clave del Registro, agregue los valores siguientes:



| Nombre                     | Tipo                      | Descripción                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| **CLSID**<br/>     | **REG \_ SZ**<br/>    | Cadena que representa el **CLSID** del agente de tareas.<br/>          |
| **IsEnabled**<br/> | **REG \_ DWORD**<br/> | 0 si el agente de tareas está deshabilitado o 1 si el agente de tareas está habilitado.<br/> |



 

> [!Note]  
> Se puede registrar más de un agente de tareas, pero solo se usará un agente de tareas. Si hay más de un agente de tareas habilitado, solo se usará el primero encontrado.

 

Aunque esta interfaz se admite en los sistemas operativos identificados en los siguientes requisitos, solo se usará si la máquina virtual se hospeda en Windows Server 2012.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



 

