---
description: Prepara un dispositivo para dibujar líneas.
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: 'ID3DXLine:: Begin (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ee241b39f2d0c1939cf2cb0cc09e079abd3430a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698379"
---
# <a name="id3dxlinebegin-method"></a>ID3DXLine:: Begin (método)

Prepara un dispositivo para dibujar líneas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Begin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

La llamada a **ID3DXLine:: Begin** es opcional. Si se llama fuera de una secuencia ID3DXLine:: Begin/ID3DXLine:: end, las funciones Draw llamarán internamente a ID3DXLine:: Begin y ID3DXLine:: end. Para evitar una sobrecarga adicional, este método se debe usar si se llama a más de una función Draw sucesivamente.

Se debe llamar a este método desde una secuencia [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) y [**IDirect3DDevice9:: EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .

ID3DXLine:: Begin no se puede usar como sustituto de [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) o [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
