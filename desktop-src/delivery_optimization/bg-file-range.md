---
title: BG_FILE_RANGE estructura (Deliveryoptimization. h)
description: La estructura BG_FILE_RANGE identifica un intervalo de bytes que se van a descargar de un archivo.
ms.assetid: 58993C51-E42E-4E44-9E8A-15E982B25413
keywords:
- Estructura de BG_FILE_RANGE
topic_type:
- apiref
api_name:
- BG_FILE_RANGE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cedabfb066a5905adb2ed8eac9996fd77c0e12be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422530"
---
# <a name="bg_file_range-structure"></a>Estructura de BG_FILE_RANGE

La estructura **BG_FILE_RANGE** identifica un intervalo de bytes que se van a descargar de un archivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  UINT64 InitialOffset;
  UINT64 Length;
} BG_FILE_RANGE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**InitialOffset**
</dt> <dd>

Desplazamiento de base cero al principio del intervalo de bytes que se va a descargar de un archivo.

</dd> <dt>

**Duración**
</dt> <dd>

Longitud del intervalo, en bytes. No especifique una longitud de cero bytes. Para indicar que el intervalo se extiende hasta el final del archivo, especifique **BG_LENGTH_TO_EOF**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El intervalo debe existir en el archivo o generar un error de **DO_E_INVALID_RANGE** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyFile2::GetFileRanges**](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 





