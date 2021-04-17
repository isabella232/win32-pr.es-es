---
description: Notifica el estado de mantenimiento de una aplicación que se ejecuta en una máquina virtual a los componentes de integración de Hyper-V que se ejecutan en la misma máquina virtual.
ms.assetid: C463391B-669C-4CBA-9EC7-7E0ABC5A63A1
title: Interfaz IVmApplicationHealthMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: ac9f6574dd8261a120e434cc0351fd07985c71a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687194"
---
# <a name="ivmapplicationhealthmonitor-interface"></a>Interfaz IVmApplicationHealthMonitor

Notifica el estado de mantenimiento de una aplicación que se ejecuta en una máquina virtual a los componentes de integración de Hyper-V que se ejecutan en la misma máquina virtual. El estado de las aplicaciones que se ejecutan en la máquina virtual se refleja en el \[ valor de la propiedad OperationalStatus 1 \] de la clase [**MSVM \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) . Esta interfaz también proporciona una manera de restablecer todo el estado de la aplicación acumulado en Hyper-V.

Esta interfaz la implementan los componentes de integración de Hyper-V de Windows 8. Una instancia de esta interfaz se obtiene creando una instancia del CLSID **397a2e5f-348c-482d-b9a3-57d383b483cd** .

## <a name="members"></a>Miembros

La interfaz **IVmApplicationHealthMonitor** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVmApplicationHealthMonitor** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IVmApplicationHealthMonitor** tiene estos métodos.



| Método                                                                                   | Descripción                                                                              |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ResetAllApplicationState**](ivmapplicationhealthmonitor-resetallapplicationstate.md) | Restablece el estado de mantenimiento de todas las aplicaciones de una máquina virtual.<br/>            |
| [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md)           | Establece el estado de mantenimiento de una aplicación que se ejecuta en una máquina virtual.<br/> |



 

## <a name="remarks"></a>Observaciones

Para usar este elemento de programación, los componentes de integración de Windows 8 deben estar instalados en la máquina virtual en la que se ejecuta la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                                                                                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                                                                                           |
| Versión<br/>                  | Componentes de integración para Windows 8<br/>                                                                                                                                |
| IDL<br/>                      | <dl> <dt>VmApplicationHealthMonitor. idl</dt> </dl>                                                                      |
| IID<br/>                      | IID \_ IVmApplicationHealthMonitor se define como 267a0284-848f-447e-a096-5e10a1a76bca<br/> El identificador de objeto se define como 397a2e5f-348c-482d-b9a3-57d383b483cd<br/> |



 

