---
title: Método de descompresión ID3DX11DataLoader (D3DX11core.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Descomprime los datos codificados.
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- Método de descompresión Direct3D 11
- Método de descompresión Direct3D 11, interfaz ID3DX11DataLoader
- ID3DX11DataLoader interface Direct3D 11 , Decompress method
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Decompress
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4f2424d46748b33918c8b6870c07dbaf4486217f8f3ba7a0a64f881792b81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633035"
---
# <a name="id3dx11dataloaderdecompress-method"></a>Método ID3DX11DataLoader::D ecompress

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Descomprime los datos codificados.

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

Tipo: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)\***

Tamaño de los datos a los que apunta ppData.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Use este método para cargar recursos desde sistemas de archivos, como archivos ZIP. Al cargar desde un recurso sin comprimir, la fase de descompresión no tiene que realizar ningún trabajo.

[**La interfaz ID3DX11DataLoader se**](id3dx11dataloader.md) puede heredar y sus miembros se pueden volver a definir para admitir formatos de archivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11DataLoader](id3dx11dataloader.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

