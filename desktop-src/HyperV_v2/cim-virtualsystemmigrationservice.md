---
description: Representa un servicio que controla la migración de sistemas virtuales entre sistemas host. Esta clase también comprueba si es probable que una migración pendiente sea correcta.
ms.assetid: 28948a36-3b92-4d52-9a48-aaa155e7fad5
title: CIM_VirtualSystemMigrationService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6343cec0573a97656368d66426ec9b46c7255e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909190"
---
# <a name="cim_virtualsystemmigrationservice-class"></a>\_Clase VirtualSystemMigrationService de CIM

Representa un servicio que controla la migración de sistemas virtuales entre sistemas host. Esta clase también comprueba si es probable que una migración pendiente sea correcta.

## <a name="syntax"></a>Sintaxis

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationService : CIM_Service
{
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ VirtualSystemMigrationService** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **CIM \_ VirtualSystemMigrationService** tiene estos métodos.



| Método                                                                                                                     | Descripción                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)     | Comprueba si es probable que se realice correctamente una migración de sistema virtual pendiente a un host.<br/>   |
| [**CheckVirtualSystemIsMigratableToSystem**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletosystem.md) | Comprueba si es probable que se realice correctamente una migración de sistema virtual pendiente a un sistema.<br/> |
| [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)                         | Migra un sistema virtual a un host de destino.<br/>                                           |
| [**MigrateVirtualSystemToSystem**](cim-virtualsystemmigrationservice-migratevirtualsystemtosystem.md)                     | Migra un sistema virtual a un sistema de destino.<br/>                                           |



 

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

 

 




