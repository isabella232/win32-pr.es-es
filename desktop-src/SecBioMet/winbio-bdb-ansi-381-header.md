---
title: WINBIO_BDB_ANSI_381_HEADER estructura (Winbio \_ types.h)
description: Especifica información sobre una serie de muestras de huellas digitales o de ramas.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- WINBIO_BDB_ANSI_381_HEADER estructura Windows API de Marco biométrico
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da04643bbdff273a2594394011ba46c16bfa29d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160790"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a>Estructura DE \_ ENCABEZADO \_ ANSI \_ 381 \_ de WINBIO BDB

La **estructura WINBIO \_ BDB ANSI \_ \_ 381 \_ HEADER** especifica información sobre una serie de muestras de huellas digitales o de hojas de árbol.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_BDB_ANSI_381_HEADER {
  ULONG64                  RecordLength;
  ULONG                    FormatIdentifier;
  ULONG                    VersionNumber;
  WINBIO_REGISTERED_FORMAT ProductId;
  USHORT                   CaptureDeviceId;
  USHORT                   ImageAcquisitionLevel;
  USHORT                   HorizontalScanResolution;
  USHORT                   VerticalScanResolution;
  USHORT                   HorizontalImageResolution;
  USHORT                   VerticalImageResolution;
  UCHAR                    ElementCount;
  UCHAR                    ScaleUnits;
  UCHAR                    PixelDepth;
  UCHAR                    ImageCompressionAlg;
  USHORT                   Reserved;
} WINBIO_BDB_ANSI_381_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**RecordLength**
</dt> <dd>

El tamaño, en bytes, de esta estructura más el tamaño de todas las estructuras [**\_ DE REGISTRO ANSI \_ \_ \_ 381 DE WINBIO BDB**](winbio-bdb-ansi-381-record.md) para las muestras de huella digital o de ramas capturadas de un usuario final. Solo los seis bytes bajos son válidos.

</dd> <dt>

**FormatIdentifier**
</dt> <dd>

Especifica el formato. Actualmente, debe ser 0x46495200.

</dd> <dt>

**VersionNumber**
</dt> <dd>

Especifica el número de versión. Actualmente, debe ser 0x30313000 que se corresponda internamente con 0.1.0.0.

</dd> <dt>

**ProductId**
</dt> <dd>

Estructura [**DE FORMATO REGISTRADO \_ \_ DE WINBIO**](winbio-registered-format.md) que contiene el formato de datos registrado como un par propietario/tipo.

</dd> <dt>

**CaptureDeviceId**
</dt> <dd>

Contiene el identificador de unidad del dispositivo utilizado para capturar el ejemplo.

</dd> <dt>

**ImageAcquisitionLevel**
</dt> <dd>

Especifica el nivel de resolución en el que se captura el ejemplo.

</dd> <dt>

**HorizontalScanResolution**
</dt> <dd>

Especifica la resolución horizontal del examen.

</dd> <dt>

**VerticalScanResolution**
</dt> <dd>

Especifica la resolución vertical del examen.

</dd> <dt>

**HorizontalImageResolution**
</dt> <dd>

Especifica la resolución horizontal de la huella digital capturada o la imagen de la mano.

</dd> <dt>

**VerticalImageResolution**
</dt> <dd>

Especifica la resolución vertical de la huella digital capturada o la imagen de la mano.

</dd> <dt>

**ElementCount**
</dt> <dd>

Número de registros de dedo o de mano en esta estructura.

</dd> <dt>

**Unidades de escalado**
</dt> <dd>

Contiene la unidad de medida, 1 para pulgadas y 2 para centímetros.

</dd> <dt>

**PixelDepth**
</dt> <dd>

Especifica el número de bits de un píxel. Puede ser de 1 a 16 bits por píxel para el color.

</dd> <dt>

**ImageCompressionAlg**
</dt> <dd>

Especifica el algoritmo utilizado para comprimir la imagen de dedo o de mano.

</dd> <dt>

**Reserved**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> </dl>

 

 





