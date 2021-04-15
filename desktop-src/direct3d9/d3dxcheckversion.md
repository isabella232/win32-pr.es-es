---
description: Compruebe que la versión de D3DX que compiló con es la versión que está ejecutando.
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: Función D3DXCheckVersion (D3dx9core. h)
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
ms.openlocfilehash: 7b392d706e54780924115471906096f6b63d1a80
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649424"
---
# <a name="d3dxcheckversion-function"></a>D3DXCheckVersion función)

Compruebe que la versión de D3DX que compiló con es la versión que está ejecutando.

## <a name="syntax"></a>Sintaxis


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*D3DSDKVersion* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Use la \_ versión del SDK de D3D \_ . Vea Notas.

</dd> <dt>

*D3DXSDKVersion* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Use la \_ versión del SDK de D3DX \_ . Vea Notas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Devuelve **true** si la versión de D3DX que compiló es la versión con la que se está ejecutando; de lo contrario, se devuelve **false** .

## <a name="remarks"></a>Observaciones

Use esta función durante la inicialización de la aplicación de la siguiente manera:


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



Use [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) para comprobar que está instalado el tiempo de ejecución correcto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
