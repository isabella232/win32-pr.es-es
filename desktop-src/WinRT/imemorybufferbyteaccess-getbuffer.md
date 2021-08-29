---
description: Obtiene un IMemoryBuffer como una matriz de bytes.
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
title: IMemoryBufferByteAccess::GetBuffer (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMemoryBufferByteAccess.GetBuffer
api_type:
- COM
api_location: ''
ms.openlocfilehash: df4e7897999dabd3ef7faff7d1e6f6b73c66f721256630e3ef91b154f4833b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758675"
---
# <a name="imemorybufferbyteaccessgetbuffer-method"></a>IMemoryBufferByteAccess::GetBuffer (método)

Obtiene un [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) como una matriz de bytes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBuffer(
  [out] BYTE   **value,
  [out] UINT32 *capacity
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Puntero a una matriz de bytes que contiene los datos del búfer.

</dd> <dt>

*capacidad* \[ out\]
</dt> <dd>

Número de bytes de la matriz devuelta

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Cuando [**se llama a MemoryBuffer::Close,**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) el código que usa este búfer debe establecer el puntero *de* valor en null.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))
</dt> </dl>

 

 
