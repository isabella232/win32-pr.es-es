---
description: Exporta el punto de referencia del sistema virtual.
ms.assetid: e4d80404-6b1b-4153-9ab2-aebab18c331a
title: Método ExportReferencePoint de la Msvm_VirtualSystemReferencePointService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3273c4781858b02e60b632ae491b1694068a32f5feaddea885576dade6876989
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147958"
---
# <a name="exportreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Método ExportReferencePoint de la clase Msvm \_ VirtualSystemReferencePointService

Exporta el punto de referencia del sistema virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ExportReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF ReferencePoint,
  [in]  string                               ExportDirectory,
  [in]  string                               ExportSettingData,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ReferencePoint* \[ En\]
</dt> <dd>

Referencia a la instancia [**de Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que representa el punto de referencia que se va a exportar.

</dd> <dt>

*ExportDirectory* \[ En\]
</dt> <dd>

Ruta de acceso completa del directorio al que se va a exportar el punto de referencia.

</dd> <dt>

*ExportSettingData* \[ En\]
</dt> <dd>

Instancia de [**Msvm \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) que representa la configuración de la operación de exportación.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Parámetro opcional para supervisar el progreso de la operación, que se usa si el método no se pudo ejecutar sincrónicamente. Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve 0 (Completado sin error) o 4096 (trabajo iniciado); de lo contrario, devuelva un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método activados: trabajo iniciado** (4096)
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

**El sistema no está** disponible (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

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

[**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




