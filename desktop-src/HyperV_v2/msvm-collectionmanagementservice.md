---
description: Administra las colecciones en el host de Hyper-V.
ms.assetid: e895217e-352d-4d77-8f1d-7070012e6f60
title: Msvm_CollectionManagementService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89d63d9a210f8c1074296620f430117d6203e295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819019"
---
# <a name="msvm_collectionmanagementservice-class"></a>MSVM \_ CollectionManagementService (clase)

Administra las colecciones en el host de Hyper-V.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionManagementService : CIM_Service
{
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ CollectionManagementService** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **MSVM \_ CollectionManagementService** tiene estos métodos.



| Método                                                                          | Descripción                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddMember**](msvm-collectionmanagementservice-addmember.md)                 | Agrega el elemento ManagedElement especificado como miembro del objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) determinado.<br/>                                                                                           |
| [**DefineCollection**](msvm-collectionmanagementservice-definecollection.md)   | Crea un nuevo objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) .<br/>                                                                                                                                        |
| [**DestroyCollection**](msvm-collectionmanagementservice-destroycollection.md) | Elimina el objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) determinado.<br/>                                                                                                                                    |
| [**RemoveMember**](msvm-collectionmanagementservice-removemember.md)           | Quita el elemento ManagedElement especificado como miembro del objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) determinado.<br/>                                                                                        |
| [**RemoveMemberById**](msvm-collectionmanagementservice-removememberbyid.md)   | Quita el elemento ManagedElement especificado como miembro de [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) con el identificador especificado. Esto se realizará correctamente incluso si el objeto con ese identificador no está presente.<br/> |
| [**RenameCollection**](msvm-collectionmanagementservice-renamecollection.md)   | Actualiza ElementName el objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) determinado.<br/>                                                                                                                    |
| [**StartService**](msvm-collectionmanagementservice-startservice.md)           | inicia el servicio.<br/>                                                                                                                                                                                                |
| [**StopService**](msvm-collectionmanagementservice-stopservice.md)             | detiene el servicio.<br/>                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Servicio CIM**](cim-service.md)
</dt> </dl>

 

 




