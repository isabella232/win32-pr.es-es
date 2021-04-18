---
description: Recupera el dispositivo Direct3D asociado a la asignación de entorno.
ms.assetid: 15f342c5-7665-443a-b7b8-32cc67034c41
title: 'ID3DXRenderToEnvMap:: GetDevice (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b5adc045beeefa220a849a6da752a8d3efc82ff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707811"
---
# <a name="id3dxrendertoenvmapgetdevice-method"></a>ID3DXRenderToEnvMap:: GetDevice (método)

Recupera el dispositivo Direct3D asociado a la asignación de entorno.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDevice* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***

Dirección de un puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el objeto de dispositivo Direct3D asociado a la asignación de entorno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL. La llamada a este método aumenta el recuento de referencias internas en la interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) . Asegúrese de llamar a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) cuando haya terminado de usar esta interfaz **IDirect3DDevice9** o se producirá una fuga de memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
