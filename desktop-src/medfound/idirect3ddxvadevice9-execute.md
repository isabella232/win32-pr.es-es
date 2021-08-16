---
description: Realiza una operación de decodificación de aceleración de vídeo de DirectX (DXVA).
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: Método IDirect3DDXVADevice9::Execute (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.Execute
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: ac00e5f78e4281523c006216f3173745ba26bc6429ddfdd9d74c9abbe616b89a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465965"
---
# <a name="idirect3ddxvadevice9execute-method"></a>IDirect3DDXVADevice9::Execute (Método)

Realiza una operación de decodificación de aceleración de vídeo de DirectX (DXVA).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Execute(
   DWORD          FunctionNum,
   VOID           *pInputData,
   DWORD          InputSize,
   VOID           *OutputData,
   DWORD          OutputSize,
   DWORD          NumBuffers,
   DXVABufferInfo *pBufferInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FunctionNum* 
</dt> <dd>

DWORD **que** contiene uno o varios números de función DXVA. Para más información, consulte la [especificación DXVA 1.0](/windows-hardware/drivers/display/directx-video-acceleration).

</dd> <dt>

*pInputData* 
</dt> <dd>

Puntero a un búfer que contiene datos de entrada para la operación decoding. El significado de estos datos depende del tipo de superficie y del número de función.

</dd> <dt>

*InputSize* 
</dt> <dd>

Tamaño de los datos de entrada, en bytes.

</dd> <dt>

*OutputData* 
</dt> <dd>

Puntero a un búfer donde el acelerador de vídeo escribe los datos de salida.

</dd> <dt>

*OutputSize* 
</dt> <dd>

Tamaño del búfer *OutputData,* en bytes.

</dd> <dt>

*NumBuffers* 
</dt> <dd>

Número de elementos de la matriz *pBufferInfo.*

</dd> <dt>

*pBufferInfo* 
</dt> <dd>

Puntero a una matriz de [**estructuras DXVABufferInfo.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                              |
| Header<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 
