---
title: Estructura de WINBIO_BDB_ANSI_381_HEADER (Winbio \_ Types. h)
description: Especifica información acerca de una serie de muestras de huellas digitales o Palm.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- Plataforma de biometría de Windows API de WINBIO_BDB_ANSI_381_HEADER Structure
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685985"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a>\_Estructura del encabezado WINBIO BDB \_ ANSI \_ 381 \_

La estructura de **\_ encabezado WINBIO BDB \_ ANSI \_ 381 \_** especifica información sobre una serie de muestras de huellas digitales o Palm.

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



## <a name="members"></a>Miembros

<dl> <dt>

**RecordLength**
</dt> <dd>

Tamaño, en bytes, de esta estructura más el tamaño de todas las estructuras de [**\_ registro WINBIO BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-record.md) para la huella digital o los ejemplos de Palm capturados por un usuario final. Solo los seis bytes inferiores son válidos.

</dd> <dt>

**FormatIdentifier**
</dt> <dd>

Especifica el formato. Actualmente, debe ser 0x46495200.

</dd> <dt>

**NúmeroDeVersión**
</dt> <dd>

Especifica el número de versión. Actualmente, este debe ser 0x30313000, que corresponde internamente a 0.1.0.0.

</dd> <dt>

**ProductId**
</dt> <dd>

Estructura [**de \_ \_ formato registrada en WINBIO**](winbio-registered-format.md) que contiene el formato de datos registrado como par de propietario/tipo.

</dd> <dt>

**CaptureDeviceId**
</dt> <dd>

Contiene el identificador de unidad del dispositivo usado para capturar el ejemplo.

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

Especifica la resolución horizontal de la huella digital capturada o la imagen de Palm.

</dd> <dt>

**VerticalImageResolution**
</dt> <dd>

Especifica la resolución vertical de la huella digital capturada o la imagen de Palm.

</dd> <dt>

**ElementCount**
</dt> <dd>

Número de registros de dedo o Palm en esta estructura.

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

Especifica el algoritmo utilizado para comprimir el dedo o la imagen de Palm.

</dd> <dt>

**Reserved**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> </dl>

 

 





