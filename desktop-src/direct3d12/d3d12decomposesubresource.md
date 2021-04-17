---
title: Función D3D12DecomposeSubresource (D3dx12.h)
description: Genera el segmento MIP, el segmento de matriz y el segmento de plano que se corresponden con el índice del subrecurso especificado.
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- D3D12DecomposeSubresource función)
topic_type:
- apiref
api_name:
- D3D12DecomposeSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec147833ee94969880865f679d40a198e0b22852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717589"
---
# <a name="d3d12decomposesubresource-function"></a>D3D12DecomposeSubresource función)

Genera el segmento MIP, el segmento de matriz y el segmento de plano que se corresponden con el índice del subrecurso especificado.

## <a name="syntax"></a>Sintaxis


```C++
void inline D3D12DecomposeSubresource(
        UINT Subresource,
        UINT MipLevels,
        UINT ArraySize,
  _Out_ T    &MipSlice,
  _Out_ U    &ArraySlice,
  _Out_ V    &PlaneSlice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Subrecurso* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice del subrecurso.

</dd> <dt>

*MipLevels* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Número máximo de niveles de mipmap en el subrecurso.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Número de elementos de la matriz.

</dd> <dt>

*MipSlice* \[ out, Ref\]
</dt> <dd>

Tipo: **T**

Genera el segmento de MIP que corresponde al índice de subrecurso dado.

</dd> <dt>

*ArraySlice* \[ out, Ref\]
</dt> <dd>

Tipo: **U**

Genera el segmento de la matriz que corresponde al índice del subrecurso dado.

</dd> <dt>

*PlaneSlice* \[ out, Ref\]
</dt> <dd>

Tipo: **V**

Genera el segmento del plano que corresponde al índice del subrecurso dado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función determina qué segmento MIP, segmento de matriz y segmento de plano corresponden a un índice de subrecurso dado. Se trata de una utilidad útil, aunque es específica de C++.

Esta función se declara como sigue, con los parámetros hace plantilla de C++ para los tipos **T**, **U** y **V**:


```c++
template <typename T, typename U, typename V>
inline void D3D12DecomposeSubresource( UINT Subresource, UINT MipLevels, UINT ArraySize, _Out_ T& MipSlice, _Out_ U& ArraySlice, _Out_ V& PlaneSlice )
{
    MipSlice = static_cast<T>(Subresource % MipLevels);
    ArraySlice = static_cast<U>((Subresource / MipLevels) % ArraySize);
    PlaneSlice = static_cast<V>(Subresource / (MipLevels * ArraySize));
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)

[Subrecursos](subresources.md)
