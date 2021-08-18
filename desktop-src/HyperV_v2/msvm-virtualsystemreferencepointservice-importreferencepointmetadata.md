---
description: Importa metadatos de punto de referencia del sistema virtual.
ms.assetid: 8e32fded-cd84-4586-83c4-c23200d4698e
title: Método ImportReferencePointMetadata de la Msvm_VirtualSystemReferencePointService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ImportReferencePointMetadata
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2757464e8b101819dc46a778df142e4e8ed37d93b774a87a037a7d272812f883
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147938"
---
# <a name="importreferencepointmetadata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Método ImportReferencePointMetadata de la clase Msvm \_ VirtualSystemReferencePointService

Importa metadatos de punto de referencia del sistema virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ImportReferencePointMetadata(
  [in]  Msvm_ComputerSystem REF AffectedSystem,
  [in]  string                  ConfigFilePath,
  [in]  string                  RuntimeStateFilePath,
  [out] CIM_ConcreteJob     REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedSystem* \[ En\]
</dt> <dd>

Referencia a un [**sistema de equipos de Msvm \_**](msvm-computersystem.md) que describe el sistema afectado.

</dd> <dt>

*ConfigFilePath* \[ En\]
</dt> <dd>

Ruta de acceso completa del archivo de configuración desde donde se importarán los metadatos del punto de referencia.

</dd> <dt>

*RuntimeStateFilePath* \[ En\]
</dt> <dd>

Ruta de acceso completa del archivo de estado en tiempo de ejecución desde donde se importarán los metadatos del punto de referencia.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Parámetro opcional para supervisar el progreso de la operación, que se usa si el método no se pudo ejecutar sincrónicamente. Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 (sin error) o uno de los siguientes mensajes de error:

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**El sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1703 \[ solo aplicaciones de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




