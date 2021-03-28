---
title: Método de proceso ID3DX11DataProcessor (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Procesa los datos.
ms.assetid: be20b231-9c2e-4b4a-bdb1-cdc75552bf9d
keywords:
- Método de proceso Direct3D 11
- Método Process Direct3D 11, interfaz ID3DX11DataProcessor
- Interfaz ID3DX11DataProcessor Direct3D 11, método Process
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Process
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6127d62398d212c94669fadaaa2ecb09819d0171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547958"
---
# <a name="id3dx11dataprocessorprocess-method"></a>ID3DX11DataProcessor::P método rador

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

Procesa los datos.

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

Tipo: **[ **tamaño \_ T**](/windows/desktop/WinProg/windows-data-types)**

Tamaño de los datos que se van a procesar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Este método lo usa una [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11DataProcessor](id3dx11dataprocessor.md)
</dt> <dt>

[Interfaces de D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

