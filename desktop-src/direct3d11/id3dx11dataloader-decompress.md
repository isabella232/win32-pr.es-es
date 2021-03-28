---
title: Método Descomprimie ID3DX11DataLoader (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Descomprime los datos codificados.
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- Descomprimir método Direct3D 11
- Método descomprimite Direct3D 11, interfaz ID3DX11DataLoader
- Interfaz ID3DX11DataLoader Direct3D 11, método Descomprimite
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
ms.openlocfilehash: b515eb38fb70fc31f0bbd0d02e20dcfb9f66ea5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003974"
---
# <a name="id3dx11dataloaderdecompress-method"></a>ID3DX11DataLoader::D método ecompress

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

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

*ppData* \[ enuncia\]
</dt> <dd>

Tipo: **void \* \***

Puntero a los datos sin procesar que se van a descomprimir.

</dd> <dt>

*pcBytes* \[ de\]
</dt> <dd>

Tipo: **[ **tamaño \_ T**](/windows/desktop/WinProg/windows-data-types)\***

Tamaño de los datos a los que apunta ppData.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Utilice este método para cargar recursos desde sistemas de archivos, como archivos ZIP. Al cargar desde un recurso sin comprimir, la fase de descompresión no tiene que realizar ningún trabajo.

La [**interfaz ID3DX11DataLoader**](id3dx11dataloader.md) se puede heredar y sus miembros se pueden redefinir para admitir formatos de archivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11DataLoader](id3dx11dataloader.md)
</dt> <dt>

[Interfaces de D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

