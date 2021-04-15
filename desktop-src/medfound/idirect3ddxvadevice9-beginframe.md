---
description: Comienza el procesamiento para crear una imagen descodificada.
ms.assetid: 80471cc6-c66d-49d9-8593-780e41ac39b9
title: 'IDirect3DDXVADevice9:: BeginFrame (método) (DXVA. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715888"
---
# <a name="idirect3ddxvadevice9beginframe-method"></a>IDirect3DDXVADevice9:: BeginFrame (método)

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

Puntero a la interfaz **IDirect3DSurface9** de la superficie de destino sin comprimir.

</dd> <dt>

*SizeInputData* 
</dt> <dd>

Tamaño del búfer especificado por *pInputData*, en bytes. El valor debe ser 2.

</dd> <dt>

*pInputData* 
</dt> <dd>

Puntero a un búfer que contiene datos para el acelerador de vídeo. Este búfer debe contener el índice de marco basado en cero, especificado como un valor de **palabra** .

</dd> <dt>

*pSizeOutputData* 
</dt> <dd>

Tamaño del búfer especificado por *pOutputData*, en bytes. El valor debe ser cero.

</dd> <dt>

*pOutputData* 
</dt> <dd>

Puntero a un búfer en el que puede escribir el acelerador de vídeo. Establezca este parámetro en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Para cada llamada a **BeginFrame**, el descodificador debe hacer una llamada correspondiente a [**IDirect3DDXVADevice9:: EndFrame**](idirect3ddxvadevice9-endframe.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




