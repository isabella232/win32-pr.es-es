---
title: Función D3D12CalcSubresource (D3dx12.h)
description: Calcula un índice de subrecurso para una textura.
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- Función D3D12CalcSubresource
topic_type:
- apiref
api_name:
- D3D12CalcSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c704be7087d95d739685bc2823ec1c31a027b4406a3110986220927fdbbffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751725"
---
# <a name="d3d12calcsubresource-function"></a>Función D3D12CalcSubresource

Calcula un índice de subrecurso para una textura.

## <a name="syntax"></a>Sintaxis


```C++
UINT inline D3D12CalcSubresource(
   UINT MipSlice,
   UINT ArraySlice,
   UINT PlaneSlice,
   UINT MipLevels,
   UINT ArraySize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MipSlice* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Índice de base cero para el nivel de mapa mip que se debe direccionar; 0 indica el primer nivel de asignación mipmap más detallado.

</dd> <dt>

*ArraySlice* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Índice de base cero para el nivel de matriz que se debe abordar; use siempre 0 para las texturas de volumen (3D).

</dd> <dt>

*PlaneSlice* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Índice de base cero para el nivel de plano que se debe abordar.

</dd> <dt>

*MipLevels* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Número de niveles de mapa mip en el recurso.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Número de elementos de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Índice que es igual a MipSlice + (ArraySlice \* MipLevels).

## <a name="remarks"></a>Comentarios

Un búfer es un recurso no estructurado y, por tanto, se define como que contiene un único subrecurso. Las API que toman búferes no necesitan un índice de subrecurso. Por otro lado, una textura está muy estructurada. Cada objeto de textura puede contener uno o varios subrecursos según el tamaño de la matriz y el número de niveles de mapa mip.

En el caso de las texturas de volumen (3D), todos los segmentos de un nivel de asignación mipmap determinado son un único índice de subrecurso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Subrecursos](subresources.md)
</dt> </dl>

 

