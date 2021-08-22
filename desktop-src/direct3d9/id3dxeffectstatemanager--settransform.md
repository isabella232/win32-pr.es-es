---
description: Función de devolución de llamada que debe implementar un usuario para establecer una transformación.
ms.assetid: 5d886554-ddb6-4b8a-a7fd-453e94b9516f
title: Método ID3DXEffectStateManager::SetTransform (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTransform
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 48b9bb16bdcb145b94e94de61ed011bb9931982511ddfb8ac9076d047c01ad0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121471"
---
# <a name="id3dxeffectstatemanagersettransform-method"></a>Método ID3DXEffectStateManager::SetTransform

Función de devolución de llamada que debe implementar un usuario para establecer una transformación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTransform(
  [in]       D3DTRANSFORMSTATETYPE State,
  [in] const D3DMATRIX             *pMatrix
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Estado* \[ En\]
</dt> <dd>

Tipo: **[ **D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**

Tipo de transformación al que se aplicará la matriz. Vea [**D3DTRANSFORMSTATETYPE.**](./d3dtransformstatetype.md)

</dd> <dt>

*pMatrix* \[ En\]
</dt> <dd>

Tipo: **const [**D3DMATRIX**](d3dmatrix.md) \***

Matriz de transformación. Vea [**D3DMATRIX.**](d3dmatrix.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ OK. Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:

-   Se producirá un error en el efecto [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   Se producirá un error en la llamada de estado de efecto dinámico (por [**ejemplo, IDirect3DDevice9::SetTransform).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
