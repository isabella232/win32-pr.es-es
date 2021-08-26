---
description: 'Función D3DX10CheckVersion: compruebe que la versión de D3DX con la que ha compilado es la versión que está ejecutando.'
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: Función D3DX10CheckVersion (D3DX10Core.h)
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
ms.openlocfilehash: 69592957c6bcd429c61eab51f968570c7ddec51fb1c0f24e522e9fee73a51cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989215"
---
# <a name="d3dx10checkversion-function"></a>Función D3DX10CheckVersion

Compruebe que la versión de D3DX con la que ha compilado es la versión que está ejecutando.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*D3DSdkVersion* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Use D3D10 \_ SDK \_ VERSION. Vea Notas.

</dd> <dt>

*D3DX10SdkVersion* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Use D3DX10 \_ SDK \_ VERSION. Vea Notas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la versión no coincide, la función devolverá FALSE (un número menor o igual que 0, el propio número no tiene ningún significado).

## <a name="remarks"></a>Comentarios

Use esta función durante la inicialización de la aplicación.


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
