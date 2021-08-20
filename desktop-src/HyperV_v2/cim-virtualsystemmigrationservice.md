---
description: Representa un servicio que controla la migración de sistemas virtuales entre sistemas host. Esta clase también comprueba si es probable que una migración pendiente se pueda realizar correctamente.
ms.assetid: 28948a36-3b92-4d52-9a48-aaa155e7fad5
title: CIM_VirtualSystemMigrationService clase
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
ms.openlocfilehash: 44b034c5b91eb024bdbcde0b0d835ba12f0367bedc6dbd9c5c2d52dca1029f87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068545"
---
# <a name="cim_virtualsystemmigrationservice-class"></a>Cim \_ VirtualSystemMigrationService (clase)

Representa un servicio que controla la migración de sistemas virtuales entre sistemas host. Esta clase también comprueba si es probable que una migración pendiente se pueda realizar correctamente.

## <a name="syntax"></a>Sintaxis

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationService : CIM_Service
{
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM VirtualSystemMigrationService** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **clase CIM \_ VirtualSystemMigrationService** tiene estos métodos.



| Método                                                                                                                     | Descripción                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)     | Comprueba si es probable que una migración del sistema virtual pendiente a un host se realiza correctamente.<br/>   |
| [**CheckVirtualSystemIsMigratableToSystem**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletosystem.md) | Comprueba si es probable que una migración del sistema virtual pendiente a un sistema se realiza correctamente.<br/> |
| [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)                         | Migra un sistema virtual a un host de destino.<br/>                                           |
| [**MigrateVirtualSystemToSystem**](cim-virtualsystemmigrationservice-migratevirtualsystemtosystem.md)                     | Migra un sistema virtual al sistema de destino.<br/>                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Servicio \_ CIM**](cim-service.md)
</dt> </dl>

 

 




