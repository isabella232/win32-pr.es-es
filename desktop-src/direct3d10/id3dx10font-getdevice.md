---
description: Recupere el dispositivo Direct3D asociado al objeto Font.
ms.assetid: aad2406e-9461-4a84-9875-74b53d68ef40
title: 'ID3DX10Font:: GetDevice (método) (D3DX10. h)'
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
ms.openlocfilehash: 72719e07c62b681579162fda56000d2d6238bd52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707897"
---
# <a name="id3dx10fontgetdevice-method"></a>ID3DX10Font:: GetDevice (método)

Recupere el dispositivo Direct3D asociado al objeto Font.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDevice* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Dirección de un puntero a una interfaz ID3D10Device que representa el objeto de dispositivo de Direct3D asociado al objeto de fuente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Al llamar a este método, se aumentará el recuento de referencias interno en la interfaz ID3D10Device. Asegúrese de llamar a IUnknown cuando haya terminado de usar esta interfaz ID3D10Device o se producirá una fuga de memoria.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




