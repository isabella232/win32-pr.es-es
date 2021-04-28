---
description: 'IWICStream_InitializeFromMemory_Proxy función: función proxy para el método InitializeFromMemory.'
ms.assetid: 737526ac-fe79-4d53-83c5-33102f5ac67b
title: IWICStream_InitializeFromMemory_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: be3cec08f2ad3970d8860803cfb70970cf7b765b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097133"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a>Función IWICStream \_ InitializeFromMemory \_ Proxy

Función de proxy para [**el método InitializeFromMemory.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***

Puntero a este [**objeto IWICStream.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)

</dd> <dt>

*pbBuffer* \[ En\]
</dt> <dd>

Tipo: **\* BYTE**

Puntero al búfer utilizado para inicializar la secuencia.

</dd> <dt>

*cbBufferSize* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Tamaño del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




