---
description: Administra la configuración de grupos de recursos mediante trabajos.
ms.assetid: cc0f0236-2335-4dd9-9132-51b3e6b9fcf4
title: CIM_ResourcePoolConfigurationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6a289c21f4a741778bb88a154f5923cf844f0c78390c50b558d40a5bcc32aff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647670"
---
# <a name="cim_resourcepoolconfigurationservice-class"></a>Clase \_ ResourcePoolConfigurationService de CIM

Administra la configuración de grupos de recursos mediante trabajos.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationService : CIM_Service
{
};
```

## <a name="members"></a>Miembros

La **clase \_ ResourcePoolConfigurationService** de CIM tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **clase \_ ResourcePoolConfigurationService** de CIM tiene estos métodos.



| Método                                                                                                          | Descripción                                                                   |
|:----------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**AddResourcesToResourcePool**](cim-resourcepoolconfigurationservice-addresourcestoresourcepool.md)           | Inicia un trabajo para agregar recursos a un grupo de recursos.<br/>                  |
| [**ChangeParentResourcePool**](cim-resourcepoolconfigurationservice-changeparentresourcepool.md)               | Inicie un trabajo para cambiar el grupo de recursos primario de un grupo de recursos.<br/> |
| [**CreateChildResourcePool**](cim-resourcepoolconfigurationservice-createchildresourcepool.md)                 | Inicie un trabajo para crear un grupo de recursos a partir de un grupo de recursos primario.<br/> |
| [**CreateResourcePool**](cim-resourcepoolconfigurationservice-createresourcepool.md)                           | Inicia un trabajo para crear un grupo de recursos raíz.<br/>                       |
| [**DeleteResourcePool**](cim-resourcepoolconfigurationservice-deleteresourcepool.md)                           | Inicie un trabajo para eliminar un grupo de recursos.<br/>                             |
| [**RemoveResourcesFromResourcePool**](cim-resourcepoolconfigurationservice-removeresourcesfromresourcepool.md) | Inicia un trabajo para quitar recursos de un grupo de recursos.<br/>             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Servicio \_ CIM**](cim-service.md)
</dt> </dl>

 

 




