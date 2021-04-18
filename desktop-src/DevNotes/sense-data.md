---
description: Se usa para notificar el estado o la información de error en respuesta a un comando de detección de solicitud SCSI.
ms.assetid: 43B2FE98-1468-4457-AB7D-3038C16E20B6
title: Estructura de SENSE_DATA (SCSI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SENSE_DATA
api_type:
- HeaderDef
api_location:
- Scsi.h
ms.openlocfilehash: b5eacf9bee8c2cebf93b27c97a88c691852a3841
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105649339"
---
# <a name="sense_data-structure"></a>Estructura de datos de detección \_

Se usa para notificar el estado o la información de error en respuesta a un comando de **detección de solicitud** SCSI.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SENSE_DATA {
  UCHAR  ErrorCode  :7;
  UCHAR  Valid  :1;
  UCHAR  SegmentNumber;
  UCHAR  SenseKey  :4;
  UCHAR  Reserved  :1;
  UCHAR  IncorrectLength  :1;
  UCHAR  EndOfMedia  :1;
  UCHAR  FileMark  :1;
  UCHAR  Information[4];
  UCHAR  AdditionalSenseLength;
  UCHAR  CommandSpecificInformation[4];
  UCHAR  AdditionalSenseCode;
  UCHAR  AdditionalSenseCodeQualifier;
  UCHAR  FieldReplaceableUnitCode;
  UCHAR  SenseKeySpecific[3];
} SENSE_DATA, *PSENSE_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ErrorCode**
</dt> <dd>

El tipo de informe.



| Value                                                                           | Significado                     |
|---------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>0x70</dt> </dl> | Errores actuales.<br/>  |
| <dl> <dt>0x71</dt> </dl> | Errores diferidos.<br/> |



 

</dd> <dt>

**Válido**
</dt> <dd>

1 si el campo de **información** se define en un estándar; de lo contrario, el campo de **información** es específico del proveedor y no está definido por un estándar.

</dd> <dt>

**SegmentNumber**
</dt> <dd>

Obsoleto.

</dd> <dt>

**SenseKey**
</dt> <dd>

Indica la categoría de error.

<dl> <dt>

<span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**No tiene sentido** (0X0)
</dt> <dt>

<span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Error recuperado** (0x1)
</dt> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (0X2)
</dt> <dt>

<span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Error medio** (0X3)
</dt> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Error de hardware** (0x4)
</dt> <dt>

<span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Solicitud no válida** (0X5)
</dt> <dt>

<span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Atención** de la unidad (0x6)
</dt> <dt>

<span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Protección de datos** (0X7)
</dt> <dt>

<span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Error de firmware** (0x9)
</dt> <dt>

<span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Comando anulado** (0xB)
</dt> <dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Igual** (0xc)
</dt> <dt>

<span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Desbordamiento de volumen** (0xd)
</dt> <dt>

<span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>No **comparación** (0xE)
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**IncorrectLength**
</dt> <dd>

1 si la longitud del bloque lógico solicitado no coincide con la longitud de bloque lógico de los datos en el medio.

</dd> <dt>

**EndOfMedia**
</dt> <dd>

1 si un dispositivo de acceso secuencial ha alcanzado el final del medio, o si una impresora no tiene papel.

</dd> <dt>

**Detecta**
</dt> <dd>

1 si el comando actual ha alcanzado una marca de acceso o setmark. Solo es válido para dispositivos de acceso secuencial.

</dd> <dt>

**Información**
</dt> <dd>

Datos específicos del tipo de dispositivo o del comando.

</dd> <dt>

**AdditionalSenseLength**
</dt> <dd>

La longitud en bytes del resto de la estructura. La longitud total menos 7.

</dd> <dt>

**CommandSpecificInformation**
</dt> <dd>

Datos específicos del comando. Los valores se definen en el estándar de comandos adecuado.

</dd> <dt>

**AdditionalSenseCode**
</dt> <dd>

Código específico del dispositivo que describe el error incluido en el campo **SenseKey** .

</dd> <dt>

**AdditionalSenseCodeQualifier**
</dt> <dd>

Puede contener detalles adicionales sobre el campo **AdditionalSenseCode** .

</dd> <dt>

**FieldReplaceableUnitCode**
</dt> <dd>

Información específica del expendedor sobre el componente asociado a estos datos de detección.

</dd> <dt>

**SenseKeySpecific**
</dt> <dd>

El contenido y el formato de la información específica de la clave de detección viene determinado por el valor del campo **SenseKey** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para obtener más información sobre el formato de datos de detección, consulte [comando de sentido de solicitud SCSI](https://wikipedia.org/wiki/SCSI_command) ( https://wikipedia.org/wiki/SCSI_command) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>SCSI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Paso a través de destino iSCSI](/powershell/module/iscsi)
</dt> <dt>

[\_paso \_ a través \_ directo de SCSI](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 




