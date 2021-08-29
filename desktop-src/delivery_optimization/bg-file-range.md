---
title: BG_FILE_RANGE estructura (Deliveryoptimization.h)
description: La BG_FILE_RANGE estructura identifica un intervalo de bytes para descargar desde un archivo.
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
ms.openlocfilehash: 048cef74eb5c375bf7c68a6c37184741a63140230e3d0ac36ac73c32ffd848ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755905"
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

## <a name="remarks"></a>Comentarios

El intervalo debe existir en el archivo o do genera un **error DO_E_INVALID_RANGE** error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyFile2::GetFileRanges**](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 





