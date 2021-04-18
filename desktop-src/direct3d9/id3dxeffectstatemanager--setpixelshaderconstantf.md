---
description: Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de punto flotante del sombreador de vértices.
ms.assetid: db87ca8c-2539-4d80-854c-25b114a7e7e0
title: 'ID3DXEffectStateManager:: SetPixelShaderConstantF (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 19e8654fbc851460fea932a8c858240c5e4631de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718305"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstantf-method"></a>ID3DXEffectStateManager:: SetPixelShaderConstantF (método)

Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de punto flotante del sombreador de vértices.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPixelShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartRegister* \[ enuncia\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de base cero del primer registro constante.

</dd> <dt>

*pConstantData* \[ enuncia\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Matriz de constantes de punto flotante.

</dd> <dt>

*RegisterCount* \[ enuncia\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

El número de registros en pConstantData.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ correcto. Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:

-   Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetPixelShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
