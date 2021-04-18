---
description: Obtiene un IMemoryBuffer como una matriz de bytes.
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
title: 'IMemoryBufferByteAccess:: GetBuffer (método)'
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
ms.openlocfilehash: f31d1506822f21977e2d60492248c2d70a51829c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715153"
---
# <a name="imemorybufferbyteaccessgetbuffer-method"></a>IMemoryBufferByteAccess:: GetBuffer (método)

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

*valor* \[ de enuncia\]
</dt> <dd>

Puntero a una matriz de bytes que contiene los datos del búfer.

</dd> <dt>

*capacidad* \[ de enuncia\]
</dt> <dd>

Número de bytes de la matriz devuelta

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Cuando se llama a [**MemoryBuffer:: Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) , el código que usa este búfer debe establecer el puntero de *valor* en NULL.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))
</dt> </dl>

 

 
