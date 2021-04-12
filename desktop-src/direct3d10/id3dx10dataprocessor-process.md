---
description: Procesa algunos datos.
ms.assetid: c64f6a2d-4512-4028-8ed9-bfc5e9e86758
title: ID3DX10DataProcessor::P método rador (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.Process
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2ddad2f6350f48f65bc82e094eccb92b1b8bf390
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280531"
---
# <a name="id3dx10dataprocessorprocess-method"></a>ID3DX10DataProcessor::P método rador

Procesa algunos datos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdata* \[ de\]
</dt> <dd>

Tipo: **void \***

Puntero a los datos que se van a procesar.

</dd> <dt>

*cBytes* \[ de\]
</dt> <dd>

Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**

Tamaño de los datos que se van a procesar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10DataProcessor](id3dx10dataprocessor.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
