---
description: Finaliza el procesamiento para crear una imagen descodificada.
ms.assetid: 4b47cd53-6ce0-47b0-83ed-84926e92430f
title: Método IDirect3DDXVADevice9::EndFrame (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.EndFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: a6a737fe6c4c3020b7ebfe7fee98281e6c83f168
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581064"
---
# <a name="idirect3ddxvadevice9endframe-method"></a>IDirect3DDXVADevice9::EndFrame (método)

Finaliza el procesamiento para crear una imagen descodificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndFrame(
   DWORD SizeMiscData,
   VOID  *pMiscData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SizeMiscData* 
</dt> <dd>

Tamaño del búfer especificado por *pMiscData*, en bytes. El valor debe ser 2.

</dd> <dt>

*pMiscData* 
</dt> <dd>

Puntero a un búfer que contiene datos para el acelerador de vídeo. Este búfer debe contener el mismo índice de marco que se pasó al método [**IDirect3DDXVADevice9::BeginFrame**](idirect3ddxvadevice9-beginframe.md) en el *parámetro pInputData.*

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

 

 




