---
description: Crea una superficie comprimida para la descodificación de DirectX video Acceleration (DXVA).
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: 'IDirect3DVideoDevice9:: CreateSurface (método) (DXVA. h)'
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
ms.openlocfilehash: d9e87c9767619241fd6228bb6b0a531249dd2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156173"
---
# <a name="idirect3dvideodevice9createsurface-method"></a>IDirect3DVideoDevice9:: CreateSurface (método)

Crea una superficie comprimida para la descodificación de DirectX video Acceleration (DXVA).

Para obtener los requisitos de la superficie, llame a [**IDirect3DVideoDevice9:: GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) y examine las estructuras [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) devueltas.

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

Ancho de la superficie, en píxeles. Establezca este parámetro en **DXVACompBufferInfo. WidthToCreate**.

</dd> <dt>

*Height* 
</dt> <dd>

Alto de la superficie, en píxeles. Establezca este parámetro en **DXVACompBufferInfo. HeightToCreate**.

</dd> <dt>

*Búferes de reserva* 
</dt> <dd>

Número de búferes de reserva. Este parámetro puede ser cero.

</dd> <dt>

*Format* 
</dt> <dd>

Formato de píxel, especificado como un valor de **D3DFORMAT** . Establezca este parámetro en **DXVACompBufferInfo. Format**.

</dd> <dt>

*Grupo* 
</dt> <dd>

El bloque de memoria en el que se va a crear la superficie, especificado como un valor de **D3DPOOL** . Establezca este parámetro en **DXVACompBufferInfo. Pool**.

</dd> <dt>

*Uso* 
</dt> <dd>

**Operación OR bit a bit** de una o varias constantes **D3DUSAGE** . Establezca este parámetro en **DXVACompBufferInfo. Usage**.

</dd> <dt>

*ppSurface* 
</dt> <dd>

Recibe un puntero a la interfaz **IDirect3DSurface9** . El llamador debe liberar la interfaz.

</dd> <dt>

*pSharedHandle* 
</dt> <dd>

Reservado. Se establece en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




