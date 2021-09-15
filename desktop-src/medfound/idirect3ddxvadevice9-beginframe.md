---
description: Comienza el procesamiento para crear una imagen descodificada.
ms.assetid: 80471cc6-c66d-49d9-8593-780e41ac39b9
title: Método IDirect3DDXVADevice9::BeginFrame (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.BeginFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3090d7868316d08fa91f36dffcc938eb31e06a7d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581065"
---
# <a name="idirect3ddxvadevice9beginframe-method"></a>IDirect3DDXVADevice9::BeginFrame (método)

Comienza el procesamiento para crear una imagen descodificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BeginFrame(
   IDirect3DSurface9 *pDstSurface,
   DWORD             SizeInputData,
   VOID              *pInputData,
   DWORD             *pSizeOutputData,
   VOID              *pOutputData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDstSurface* 
</dt> <dd>

Puntero a la **interfaz IDirect3DSurface9 de** la superficie de destino sin comprimir.

</dd> <dt>

*SizeInputData* 
</dt> <dd>

Tamaño del búfer especificado por *pInputData*, en bytes. El valor debe ser 2.

</dd> <dt>

*pInputData* 
</dt> <dd>

Puntero a un búfer que contiene datos para el acelerador de vídeo. Este búfer debe contener el índice de marco de base cero, especificado como un **valor WORD.**

</dd> <dt>

*pSizeOutputData* 
</dt> <dd>

Tamaño del búfer especificado por *pOutputData*, en bytes. El valor debe ser cero.

</dd> <dt>

*pOutputData* 
</dt> <dd>

Puntero a un búfer en el que el acelerador de vídeo puede escribir. Establezca este parámetro en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Para cada llamada a **BeginFrame**, el descodificador debe realizar una llamada correspondiente a [**IDirect3DDXVADevice9::EndFrame**](idirect3ddxvadevice9-endframe.md).

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

 

 




