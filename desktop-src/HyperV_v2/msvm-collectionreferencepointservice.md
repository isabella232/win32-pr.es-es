---
description: Servicio para crear, destruir y exportar puntos de referencia.
ms.assetid: 88a76319-b5a7-44a3-8a31-83ade999b255
title: Msvm_CollectionReferencePointService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6ba56fcb75a177521b8f3ea3ae0675cfdd8a8dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687029"
---
# <a name="msvm_collectionreferencepointservice-class"></a>MSVM \_ CollectionReferencePointService (clase)

Servicio para crear, destruir y exportar puntos de referencia

de colecciones del sistema virtual.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointService : CIM_Service
{
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ CollectionReferencePointService** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **MSVM \_ CollectionReferencePointService** tiene estos métodos.



| Método                                                                                      | Descripción                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md)   | Crea un punto de referencia de una colección de sistemas virtuales.<br/>                                                                                                                                            |
| [**DestroyReferencePoint**](msvm-collectionreferencepointservice-destroyreferencepoint.md) | Destruye una colección de puntos de referencia existente. Este método puede ser un efecto secundario de la destrucción de otros puntos de referencia que dependen de la colección de puntos de referencia afectados.<br/>                      |
| [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md)   | Exporta una colección de puntos de referencia a un archivo. La colección de puntos de referencia, sus valores de configuración asociados y su configuración de recursos asociada se conservarán en el archivo resultante.<br/> |
| [**RemoveAssociatedData**](msvm-collectionreferencepointservice-removeassociateddata.md)   | Quita el registro de datos asociado al punto de referencia.<br/>                                                                                                                                            |



 

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

 

 




