---
description: Representa un servicio que puede crear, aplicar y eliminar instantáneas de sistemas virtuales.
ms.assetid: 8d5d54a2-08f1-4f24-bca3-601dc698d018
title: CIM_VirtualSystemSnapshotService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ae74f85d1af9867b7a95c23aeda670b8f06f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913901"
---
# <a name="cim_virtualsystemsnapshotservice-class"></a>\_Clase VirtualSystemSnapshotService de CIM

Representa un servicio que puede crear, aplicar y eliminar instantáneas de sistemas virtuales.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemSnapshotService : CIM_Service
{
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ VirtualSystemSnapshotService** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **CIM \_ VirtualSystemSnapshotService** tiene estos métodos.



| Método                                                                      | Descripción                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**ApplySnapshot**](cim-virtualsystemsnapshotservice-applysnapshot.md)     | Aplica una instantánea del sistema virtual al sistema virtual de origen.<br/> |
| [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md)   | Crea una instantánea de un sistema virtual.<br/>                                               |
| [**DestroySnapshot**](cim-virtualsystemsnapshotservice-destroysnapshot.md) | Elimina una instantánea del sistema virtual.<br/>                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Servicio CIM**](cim-service.md)
</dt> </dl>

 

 




