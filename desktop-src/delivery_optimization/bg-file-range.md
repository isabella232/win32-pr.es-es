---
title: BG_FILE_RANGE estructura (Deliveryoptimization.h)
description: La BG_FILE_RANGE identifica un intervalo de bytes que se van a descargar de un archivo.
ms.assetid: 58993C51-E42E-4E44-9E8A-15E982B25413
keywords:
- BG_FILE_RANGE estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126884857"
---
# <a name="bg_file_range-structure"></a>BG_FILE_RANGE estructura

La **BG_FILE_RANGE** estructura identifica un intervalo de bytes que se van a descargar de un archivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  UINT64 InitialOffset;
  UINT64 Length;
} BG_FILE_RANGE;
```



## <a name="members"></a>Members

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

El intervalo debe existir en el archivo o do genera un **error DO_E_INVALID_RANGE** error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBackgroundCopyFile2::GetFileRanges**](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 





