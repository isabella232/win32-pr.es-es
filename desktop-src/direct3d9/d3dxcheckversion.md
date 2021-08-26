---
description: 'Función D3DXCheckVersion: compruebe que la versión de D3DX con la que ha compilado es la versión que está ejecutando.'
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: Función D3DXCheckVersion (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 26831f3a1a5f08494a7382cd412c30dcd24c1482c01dca684962a580068d380d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894125"
---
# <a name="d3dxcheckversion-function"></a>Función D3DXCheckVersion

Compruebe que la versión de D3DX con la que ha compilado es la versión que está ejecutando.

## <a name="syntax"></a>Sintaxis


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*D3DSDKVersion* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Use D3D \_ SDK \_ VERSION. Vea Notas.

</dd> <dt>

*D3DXSDKVersion* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Use D3DX \_ SDK \_ VERSION. Vea Notas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Devuelve **TRUE** si la versión de D3DX con la que se compiló es la versión con la que se está ejecutando; De lo contrario, se devuelve **FALSE.**

## <a name="remarks"></a>Comentarios

Use esta función durante la inicialización de la aplicación de esta forma:


```
HRESULT CD3DXMyApplication::Initialize(HINSTANCE hInstance, 
  LPCSTR szWindowName, LPCSTR szClassName, UINT uWidth, UINT uHeight)
{
    HRESULT hr;
    
    if (!D3DXCheckVersion(D3D_SDK_VERSION, D3DX_SDK_VERSION))
        return E_FAIL;
    
    ...
}
```



Use [**Direct3DCreate9 para**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) comprobar que está instalado el tiempo de ejecución correcto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general Functions](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
