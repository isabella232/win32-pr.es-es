---
title: Función D3D12CalcSubresource (D3dx12. h)
description: Calcula un índice de subrecurso para una textura.
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- D3D12CalcSubresource función)
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
ms.openlocfilehash: e872d13ba5221ad50003d789b87f65fc64821dd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707758"
---
# <a name="d3d12calcsubresource-function"></a>D3D12CalcSubresource función)

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice de base cero del nivel de mipmap que se va a direccionar; 0 indica el primer nivel de mapa MIP más detallado.

</dd> <dt>

*ArraySlice* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice de base cero para el nivel de matriz que se va a direccionar; Use siempre 0 para las texturas de volumen (3D).

</dd> <dt>

*PlaneSlice* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice de base cero para el nivel de plano que se va a direccionar.

</dd> <dt>

*MipLevels* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

El número de niveles de mipmap en el recurso.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Número de elementos de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice que es igual a MipSlice + (ArraySlice \* MipLevels).

## <a name="remarks"></a>Observaciones

Un búfer es un recurso no estructurado y, por tanto, se define como si contuviera un único subrecurso. Las API que toman búferes no necesitan un índice de subrecurso. Una textura por otro lado está muy estructurada. Cada objeto de textura puede contener uno o más Subrecursos en función del tamaño de la matriz y el número de niveles de mipmap.

En el caso de las texturas de volumen (3D), todos los segmentos de un nivel de mipmap determinado son un índice de un solo recurso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Subrecursos](subresources.md)
</dt> </dl>

 

