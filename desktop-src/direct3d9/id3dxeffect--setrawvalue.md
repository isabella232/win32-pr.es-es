---
description: Establezca un intervalo contiguo de constantes de sombreador con una copia de memoria.
ms.assetid: 8a3b5141-c67a-45b9-91c2-1877642164e3
title: 'ID3DXEffect:: SetRawValue (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetRawValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cc3ce5eb547032ced5d0d79c533cefd1d2daab3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707793"
---
# <a name="id3dxeffectsetrawvalue-method"></a>ID3DXEffect:: SetRawValue (método)

Establezca un intervalo contiguo de constantes de sombreador con una copia de memoria.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetRawValue(
  [in] D3DXHANDLE Handle,
  [in] void       *pData,
  [in] DWORD      OffsetInBytes,
  [in] DWORD      Bytes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Identificador* \[ de de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador del valor que se va a establecer o nombre del valor que se pasa como una cadena. Pasar un identificador es más eficaz. Vea [identificadores (Direct3D 9)](handles.md).

</dd> <dt>

*pdata* \[ de\]
</dt> <dd>

Tipo: **void \***

Puntero a un búfer que contiene los datos que se van a establecer. SetRawValue comprueba la memoria válida, pero no realiza ninguna comprobación de datos válidos.

</dd> <dt>

*OffsetInBytes* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de bytes entre el principio de los datos del efecto y el comienzo de las constantes del efecto que se van a establecer.

</dd> <dt>

*Bytes* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Tamaño del búfer que se va a establecer, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: E \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

SetRawValue es una manera muy rápida de establecer constantes de efecto, ya que realiza una copia de memoria sin realizar la validación ni ninguna conversión de datos (como la conversión de una matriz de filas principales en una matriz de columnas principal). Use SetRawValue para establecer una serie de constantes de efectos contiguos. Por ejemplo, puede establecer una matriz de veinte matrices con 20 llamadas a [**ID3DXBaseEffect:: SetMatrix**](id3dxbaseeffect--setmatrix.md) o mediante un solo SetRawValue.

Se espera que todos los valores sean matrix4x4s o float4s y se espera que todas las matrices estén en orden de columna principal. Los valores int o float se convierten en una FLOAT4; por lo tanto, se recomienda encarecidamente que use SetRawValue solo con datos FLOAT4 o matrix4x4.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
