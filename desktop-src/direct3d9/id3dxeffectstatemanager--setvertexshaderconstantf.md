---
description: Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de punto flotante del sombreador de vértices.
ms.assetid: 3a13040d-5d5a-4454-bf11-cda9653585c0
title: 'ID3DXEffectStateManager:: SetVertexShaderConstantF (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 378af983e0ed7ca1709ae8bb6cfe8615a481b3f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698322"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantf-method"></a>ID3DXEffectStateManager:: SetVertexShaderConstantF (método)

Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de punto flotante del sombreador de vértices.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetVertexShaderConstantF(
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
-   Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
