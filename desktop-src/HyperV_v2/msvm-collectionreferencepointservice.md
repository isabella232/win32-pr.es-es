---
description: Servicio para crear, destruir y exportar puntos de referencia.
ms.assetid: 88a76319-b5a7-44a3-8a31-83ade999b255
title: Msvm_CollectionReferencePointService clase
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
ms.openlocfilehash: 3ab0a3cb41ac32751b896988a05d8b4404fc37813781fe72382bc67a03a110f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426925"
---
# <a name="msvm_collectionreferencepointservice-class"></a>Clase \_ CollectionReferencePointService de Msvm

Servicio para crear, destruir y exportar puntos de referencia

de colecciones de sistema virtual.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointService : CIM_Service
{
};
```

## <a name="members"></a>Miembros

La **clase \_ CollectionReferencePointService de Msvm** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **clase \_ CollectionReferencePointService de Msvm** tiene estos métodos.



| Método                                                                                      | Descripción                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md)   | Crea un punto de referencia de una colección de sistema virtual.<br/>                                                                                                                                            |
| [**DestroyReferencePoint**](msvm-collectionreferencepointservice-destroyreferencepoint.md) | Destruye una colección de puntos de referencia existente. Este método puede destruir como efecto secundario otros puntos de referencia que dependen de la colección de puntos de referencia afectada.<br/>                      |
| [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md)   | Exporta una colección de puntos de referencia a un archivo. La colección de puntos de referencia, sus opciones de configuración asociadas y sus valores de recursos asociados se conservarán en el archivo resultante.<br/> |
| [**RemoveAssociatedData**](msvm-collectionreferencepointservice-removeassociateddata.md)   | Quita el registro de datos asociado al punto de referencia.<br/>                                                                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Servicio \_ CIM**](cim-service.md)
</dt> </dl>

 

 




