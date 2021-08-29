---
description: Establezca un intervalo contiguo de constantes de sombreador con una copia de memoria.
ms.assetid: 8a3b5141-c67a-45b9-91c2-1877642164e3
title: Método ID3DXEffect::SetRawValue (D3DX9Effect.h)
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
ms.openlocfilehash: 10ba7dd5729d67fdd34180d737e835e0a22dc10de2126df3c8b07c2176a78fe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494055"
---
# <a name="id3dxeffectsetrawvalue-method"></a>Método ID3DXEffect::SetRawValue

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

*Identificador* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Controle el valor que se establecerá o el nombre del valor pasado como una cadena. Pasar un identificador es más eficaz. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Tipo: **\* void**

Puntero a un búfer que contiene los datos que se establecerán. SetRawValue comprueba si hay memoria válida, pero no realiza ninguna comprobación de los datos válidos.

</dd> <dt>

*OffsetInBytes* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de bytes entre el principio de los datos del efecto y el principio de las constantes de efecto que se van a establecer.

</dd> <dt>

*Bytes* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Tamaño del búfer que se va a establecer, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: E \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

SetRawValue es una manera muy rápida de establecer constantes de efecto, ya que realiza una copia de memoria sin realizar la validación ni ninguna conversión de datos (como convertir una matriz de filas principales en una matriz principal de columna). Use SetRawValue para establecer una serie de constantes de efecto contiguas. Por ejemplo, podría establecer una matriz de veinte matrices con 20 llamadas a [**ID3DXBaseEffect::SetMatrix**](id3dxbaseeffect--setmatrix.md) o mediante un único valor SetRawValue.

Se espera que todos los valores sean matrix4x4s o float4s y se espera que todas las matrices estén en orden de columna principal. Los valores int o float se convierten en float4; Por lo tanto, se recomienda encarecidamente usar SetRawValue solo con datos float4 o matrix4x4.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
