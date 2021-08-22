---
description: La función ModifyFrame modifica un marco existente con nuevos datos.
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: Función ModifyFrame (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ModifyFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 04bc22af11d83078ecf98d0386b061b520fbf9a8dcab6f6beb360c45b1c6fe96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555825"
---
# <a name="modifyframe-function"></a>Función ModifyFrame

La **función ModifyFrame** modifica un marco existente con nuevos datos.

## <a name="syntax"></a>Sintaxis


```C++
HFRAME WINAPI ModifyFrame(
  _In_  HCAPTURE hCapture,
  _In_  DWORD    FrameNumber,
  _In_  LPBYTE   FrameData,
  _In_  DWORD    FrameLength,
  _Out_ __int64  TimeStamp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hCapture* \[ En\]
</dt> <dd>

Identificador de la captura. Para obtener información sobre cómo obtener el identificador de captura, vea la sección Comentarios de este **tema ModifyFrame.**

</dd> <dt>

*FrameNumber* \[ En\]
</dt> <dd>

Número de índice de fotogramas.

</dd> <dt>

*FrameData* \[ En\]
</dt> <dd>

Puntero a una matriz de bytes que contienen los nuevos datos de marco.

</dd> <dt>

*FrameLength* \[ En\]
</dt> <dd>

Longitud de los nuevos datos, en bytes.

</dd> <dt>

*TimeStamp* \[ out\]
</dt> <dd>

Marca de tiempo que indica cuándo se modificó el marco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un identificador para un nuevo marco.

Si la función no se realiza correctamente, el valor devuelto es **NULL.**

## <a name="remarks"></a>Comentarios

Si la llamada se realiza correctamente, **la función ModifyFrame** destruye el fotograma original.

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función ModifyFrame.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




