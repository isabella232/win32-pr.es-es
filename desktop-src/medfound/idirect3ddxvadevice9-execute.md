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
ms.openlocfilehash: d624146c32b5f7eaeb4e680cf03878e8d065ee5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580448"
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



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 
