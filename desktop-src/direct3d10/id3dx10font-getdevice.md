---
description: Recupere el dispositivo Direct3D asociado al objeto de fuente.
ms.assetid: aad2406e-9461-4a84-9875-74b53d68ef40
title: Método ID3DX10Font::GetDevice (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0abed8fcb2e5c85b64c58f66f7584d1c6af5f5b6b4ed9e2efd7266ea38a5a8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118100410"
---
# <a name="id3dx10fontgetdevice-method"></a>Método ID3DX10Font::GetDevice

Recupere el dispositivo Direct3D asociado al objeto de fuente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDevice* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Dirección de un puntero a una interfaz ID3D10Device, que representa el objeto de dispositivo Direct3D asociado al objeto de fuente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Llamar a este método aumentará el número de referencias internas en la interfaz ID3D10Device. Asegúrese de llamar a IUnknown cuando haya terminado de usar esta interfaz ID3D10Device o tendrá una pérdida de memoria.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




