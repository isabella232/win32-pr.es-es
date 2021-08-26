---
description: Se usa para descomprimir los datos codificados. Normalmente, esto se usaría para cargar recursos desde sistemas de archivos, como archivos ZIP. Al cargar desde un recurso sin comprimir, la fase de descompresión no tiene que realizar ningún trabajo.
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: Método ID3DX10DataLoader::D ecompress (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader.Decompress
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c9e532bae8cb121fc93f3fdf2a5a1ee23e597c66599277b73b3b36b15ebbb963
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989125"
---
# <a name="id3dx10dataloaderdecompress-method"></a>Método ID3DX10DataLoader::D ecompress

Se usa para descomprimir los datos codificados. Normalmente, esto se usaría para cargar recursos desde sistemas de archivos, como archivos ZIP. Al cargar desde un recurso sin comprimir, la fase de descompresión no tiene que realizar ningún trabajo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppData* \[ out\]
</dt> <dd>

Tipo: **\* \* void**

Puntero a los datos sin procesar que se descomprimen.

</dd> <dt>

*pcBytes* \[ En\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

Tamaño de los datos a los que apunta ppData.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

[**La interfaz ID3DX10DataLoader**](id3dx10dataloader.md) se puede heredar y sus miembros se pueden volver a definir. La descompresión se podría volver a definir para admitir sus propios formatos de archivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10DataLoader](id3dx10dataloader.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
