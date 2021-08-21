---
title: Función D3D12DecomposeSubresource (D3dx12.h)
description: Genera el segmento mip, el segmento de matriz y el segmento de plano que corresponden al índice de subrecurso especificado.
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- Función D3D12DecomposeSubresource
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
ms.openlocfilehash: 1c27089fb09c2408917be06b2f74e6d32f3e2f5aa9b96924de1ab92de190efb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045643"
---
# <a name="d3d12decomposesubresource-function"></a>Función D3D12DecomposeSubresource

Genera el segmento mip, el segmento de matriz y el segmento de plano que corresponden al índice de subrecurso especificado.

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

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Índice del subrecurso.

</dd> <dt>

*MipLevels* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Número máximo de niveles de mapa mip en el subrecurso.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Número de elementos de la matriz.

</dd> <dt>

*MipSlice* \[ out, ref\]
</dt> <dd>

Tipo: **T**

Genera el segmento mip que corresponde al índice de subrecursos especificado.

</dd> <dt>

*ArraySlice* \[ out, ref\]
</dt> <dd>

Tipo: **U**

Genera el segmento de matriz que corresponde al índice de subrecurso especificado.

</dd> <dt>

*PlaneSlice* \[ out, ref\]
</dt> <dd>

Tipo: **V**

Genera el segmento de plano que corresponde al índice de subrecursos especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta función determina qué segmento mip, segmento de matriz y segmento de plano corresponden a un índice de subrecurso determinado. Se trata de una utilidad útil, aunque es específica de C++.

Esta función se declara de la siguiente manera, con parámetros con plantillas de C++ para los tipos **T,** **U** y **V**:


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
| Encabezado<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)

[Subrecursos](subresources.md)
