---
description: La función ModifyFrame modifica un marco existente con nuevos datos.
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: Función ModifyFrame (Netmon. h)
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
ms.openlocfilehash: af3ef6c2c5ccae2b6410ac8fc81c815f790b17a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666543"
---
# <a name="modifyframe-function"></a>ModifyFrame función)

La función **ModifyFrame** modifica un marco existente con nuevos datos.

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

*hCapture* \[ de\]
</dt> <dd>

Identificador de la captura. Para obtener información acerca de cómo obtener el identificador de captura, vea la sección Comentarios de este tema **ModifyFrame** .

</dd> <dt>

*Númeromarco* \[ de\]
</dt> <dd>

Número de índice del marco.

</dd> <dt>

*FrameData* \[ de\]
</dt> <dd>

Puntero a una matriz de bytes que contiene los nuevos datos de marco.

</dd> <dt>

*FrameLength* \[ de\]
</dt> <dd>

Longitud de los datos nuevos, en bytes.

</dd> <dt>

*Marca* \[ de tiempo enuncia\]
</dt> <dd>

Marca de tiempo que indica cuándo se modificó el marco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es un identificador de un nuevo marco.

Si la función no se realiza correctamente, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

Si la llamada se realiza correctamente, la función **ModifyFrame** destruye el marco original.

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **ModifyFrame** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




