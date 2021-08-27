---
title: Interfaz ID3DX11DataLoader (D3DX11core.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store. Objeto de carga de datos utilizado por la interfaz ID3DX11ThreadPump para cargar datos de forma asincrónica.
ms.assetid: 878929ea-0228-4650-9ca0-f83d60d9f915
keywords:
- Interfaz ID3DX11DataLoader Direct3D 11
- Interfaz ID3DX11DataLoader Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11DataLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b688fcbeff21edf23f6a3be1b39be5a9cf0000
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471651"
---
# <a name="id3dx11dataloader-interface"></a>Interfaz ID3DX11DataLoader

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Objeto de carga de datos utilizado [**por la interfaz ID3DX11ThreadPump**](id3dx11threadpump.md) para cargar datos de forma asincrónica.

## <a name="members"></a>Miembros

La **interfaz ID3DX11DataLoader** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11DataLoader** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11DataLoader** tiene estos métodos.




| Método | Descripción | 
|--------|-------------|
| <a href="id3dx11dataloader-decompress.md"><strong>Descomprimir</strong></a> | <blockquote>[!Note]<br />La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.</blockquote><br /> Descomprime los datos codificados.<br /> | 
| <a href="id3dx11dataloader-destroy.md"><strong>Destruir</strong></a> | <blockquote>[!Note]<br />La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.</blockquote><br /> Destruye el cargador una vez completado un elemento de trabajo.<br /> | 
| <a href="id3dx11dataloader-load.md"><strong>Cargar</strong></a> | <blockquote>[!Note]<br />La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.</blockquote><br /> Carga datos desde un disco.<br /> | 




 

## <a name="remarks"></a>Comentarios

Este objeto se puede heredar y sus miembros se pueden volver a definir. Esto le permitiría personalizar la API para cargar y descomprimir sus propios formatos de archivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>D3DX11core.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

