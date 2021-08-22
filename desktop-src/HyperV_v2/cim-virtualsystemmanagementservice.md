---
description: Representa un servicio que administra sistemas virtuales.
ms.assetid: b2645546-3c04-4d3f-8d53-019a6db08e24
title: CIM_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 903b751b405c103313c0f83c38687e08ee7bb36a33ae803bd175b6ad91c559cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068625"
---
# <a name="cim_virtualsystemmanagementservice-class"></a>Cim \_ VirtualSystemManagementService (clase)

Representa un servicio que administra sistemas virtuales.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementService : CIM_Service
{
};
```

## <a name="members"></a>Miembros

La **clase CIM \_ VirtualSystemManagementService** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **clase CIM \_ VirtualSystemManagementService** tiene estos métodos.



| Método                                                                                      | Descripción                                                                           |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**AddResourceSettings**](cim-virtualsystemmanagementservice-addresourcesettings.md)       | Agrega recursos a una configuración del sistema virtual.<br/>                          |
| [**DefineSystem**](cim-virtualsystemmanagementservice-definesystem.md)                     | Define un sistema virtual.<br/>                                                  |
| [**DestroySystem**](cim-virtualsystemmanagementservice-destroysystem.md)                   | Elimina un sistema virtual.<br/>                                                  |
| [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) | Modifica la configuración de recursos virtuales para una configuración del sistema virtual.<br/> |
| [**ModifySystemSettings**](cim-virtualsystemmanagementservice-modifysystemsettings.md)     | Modifica la configuración del sistema virtual.<br/>                                          |
| [**RemoveResourceSettings**](cim-virtualsystemmanagementservice-removeresourcesettings.md) | Quita la configuración de recursos virtuales de una configuración del sistema virtual.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 




