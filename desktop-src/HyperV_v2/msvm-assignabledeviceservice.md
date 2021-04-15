---
description: Administra los dispositivos asignables en un sistema de equipo host.
ms.assetid: d958e978-682e-49eb-bd10-d31d9563fdbf
title: Msvm_AssignableDeviceService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8aff620e9227000b2c4a03069f8a5f900a5fc82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688727"
---
# <a name="msvm_assignabledeviceservice-class"></a>MSVM \_ AssignableDeviceService (clase)

Administra los dispositivos asignables en un sistema de equipo host.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AssignableDeviceService : CIM_Service
{
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ AssignableDeviceService** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **MSVM \_ AssignableDeviceService** tiene estos métodos.



| Método                                                                                    | Descripción                                                                                    |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**DismountAssignableDevice**](msvm-assignabledeviceservice-dismountassignabledevice.md) | Desmonta el dispositivo PCI especificado para que se pueda asignar.<br/>                      |
| [**MountAssignableDevice**](msvm-assignabledeviceservice-mountassignabledevice.md)       | Monta el dispositivo PCI especificado para que lo pueda usar el sistema del equipo host.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Servicio CIM**](cim-service.md)
</dt> </dl>

 

 




