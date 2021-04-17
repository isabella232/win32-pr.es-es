---
description: Servicio para crear, destruir y exportar la colección de instantáneas de sistemas virtuales.
ms.assetid: 55a6c7b4-5352-4766-b5b7-6699b1f40b78
title: Msvm_CollectionSnapshotService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f9e835ad54773d69fab19861c7a9c417ac7d8a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666837"
---
# <a name="msvm_collectionsnapshotservice-class"></a>MSVM \_ CollectionSnapshotService (clase)

Servicio para crear, destruir y exportar la colección de instantáneas de sistemas virtuales.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotService : CIM_Service
{
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ CollectionSnapshotService** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **MSVM \_ CollectionSnapshotService** tiene estos métodos.



| Método                                                                                    | Descripción                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplySnapshot**](msvm-collectionsnapshotservice-applysnapshot.md)                     | Aplica una colección de instantáneas a la colección de sistemas del equipo virtual.<br/>                                                                                                                                        |
| [**ConvertToReferencePoint**](msvm-collectionsnapshotservice-converttoreferencepoint.md) | Convertir una instantánea de colección existente en una colección de puntos de referencia. La colección de instantáneas se elimina como un efecto secundario. Solo las instantáneas de recuperación se pueden convertir en puntos de referencia.<br/>                      |
| [**CreateSnapshot**](msvm-collectionsnapshotservice-createsnapshot.md)                   | Crea una instantánea de una colección de sistemas virtuales.<br/>                                                                                                                                                                 |
| [**DestroySnapshot**](msvm-collectionsnapshotservice-destroysnapshot.md)                 | Destruya una instantánea existente de la colección de sistemas virtuales. Este método puede ser un efecto secundario de destruir otras instantáneas que dependen de la instantánea afectada.<br/>                                                   |
| [**ExportSnapshot**](msvm-collectionsnapshotservice-exportsnapshot.md)                   | Exporta una colección de instantáneas de sistemas de equipos virtuales a un archivo. La colección de instantáneas, sus valores de configuración asociados y su configuración de recursos asociada se conservarán en el archivo resultante.<br/> |



 

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

 

 




