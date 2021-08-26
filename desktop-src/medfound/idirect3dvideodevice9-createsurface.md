---
description: Crea una superficie comprimida para lacodización de aceleración de vídeo de DirectX (DXVA).
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: Método IDirect3DVideoDevice9::CreateSurface (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateSurface
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: b5bc624527c7ef3ea2a8bb9c878f1d97e865a54341ae5902449fb8a015374f3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887875"
---
# <a name="idirect3dvideodevice9createsurface-method"></a>IDirect3DVideoDevice9::CreateSurface (Método)

Crea una superficie comprimida para lacodización de aceleración de vídeo de DirectX (DXVA).

Para obtener los requisitos de superficie, llame a [**IDirect3DVideoDevice9::GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) y examine las estructuras [**DXVACompBufferInfo devueltas.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateSurface(
   UINT              Width,
   UINT              Height,
   UINT              BackBuffers,
   D3DFORMAT         Format,
   D3DPOOL           Pool,
   DWORD             Usage,
   IDirect3DSurface9 **ppSurface,
   HANDLE            *pSharedHandle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Width* 
</dt> <dd>

Ancho de la superficie, en píxeles. Establezca este parámetro en **DXVACompBufferInfo.WidthToCreate.**

</dd> <dt>

*Height* 
</dt> <dd>

Alto de la superficie, en píxeles. Establezca este parámetro en **DXVACompBufferInfo.HeightToCreate**.

</dd> <dt>

*BackBuffers* 
</dt> <dd>

Número de búferes de reserva. Este parámetro puede ser cero.

</dd> <dt>

*Format* 
</dt> <dd>

Formato de píxel, especificado como valor **D3DFORMAT.** Establezca este parámetro en **DXVACompBufferInfo.Format.**

</dd> <dt>

*Grupo* 
</dt> <dd>

Grupo de memoria en el que se va a crear la superficie, especificado como **un valor D3DPOOL.** Establezca este parámetro en **DXVACompBufferInfo.Pool.**

</dd> <dt>

*Uso* 
</dt> <dd>

OR bit a **bit** de una o varias **constantes D3DUSAGE.** Establezca este parámetro en **DXVACompBufferInfo.Usage.**

</dd> <dt>

*ppSurface* 
</dt> <dd>

Recibe un puntero a la **interfaz IDirect3DSurface9.** El autor de la llamada debe liberar la interfaz .

</dd> <dt>

*pSharedHandle* 
</dt> <dd>

Reservado. Se establece en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                              |
| Header<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




