---
description: Describe un servicio de punto de referencia del sistema virtual.
ms.assetid: 888ecd21-4b59-46a9-b2e1-538e30dd2d1c
title: Msvm_VirtualSystemReferencePointService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0614349ed6f6358316826bbfc2cd10ac55cba953
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670063"
---
# <a name="msvm_virtualsystemreferencepointservice-class"></a>MSVM \_ VirtualSystemReferencePointService (clase)

Describe un servicio de punto de referencia del sistema virtual.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointService : CIM_Service
{
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ VirtualSystemReferencePointService** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **MSVM \_ VirtualSystemReferencePointService** tiene estos métodos.



| Método                                                                                                       | Descripción                                                          |
|:-------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md)                 | Crea un punto de referencia de un sistema virtual.<br/>            |
| [**DestroyReferencePoint**](msvm-virtualsystemreferencepointservice-destroyreferencepoint.md)               | Elimina el punto de referencia especificado.<br/>                    |
| [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md)                 | Exporta el punto de referencia del sistema virtual.<br/>        |
| [**ImportReferencePointMetadata**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md) | Importa los metadatos del punto de referencia del sistema virtual.<br/>   |
| [**RemoveAssociatedData**](msvm-virtualsystemreferencepointservice-removeassociateddata.md)                 | Quita el registro de datos asociado al punto de referencia.<br/> |



 

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

 

 




