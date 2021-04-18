---
description: Compruebe que la versión de D3DX que compiló con es la versión que está ejecutando.
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: Función D3DX10CheckVersion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CheckVersion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3b41996f16cb97d91dc59f8d368f13b905992388
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721511"
---
# <a name="d3dx10checkversion-function"></a>D3DX10CheckVersion función)

Compruebe que la versión de D3DX que compiló con es la versión que está ejecutando.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*D3DSdkVersion* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Use la \_ versión del SDK de D3D10 \_ . Vea Notas.

</dd> <dt>

*D3DX10SdkVersion* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Use la \_ versión del SDK de D3DX10 \_ . Vea Notas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la versión no coincide, la función devolverá FALSE (un número menor o igual que 0, el propio número no tiene ningún significado).

## <a name="remarks"></a>Observaciones

Use esta función durante la inicialización de la aplicación.


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
