---
description: Objeto de carga de datos usado por la interfaz ID3DX10ThreadPump para cargar datos de forma asincrónica.
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: Interfaz ID3DX10DataLoader (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 86da40dd581c10d9f567f6011cd3987710a9aa36e41f360dc4ffc2662f909c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128373"
---
# <a name="id3dx10dataloader-interface"></a>Interfaz ID3DX10DataLoader

Objeto de carga de datos utilizado [**por la interfaz ID3DX10ThreadPump**](id3dx10threadpump.md) para cargar datos de forma asincrónica.

## <a name="members"></a>Miembros

La **interfaz ID3DX10DataLoader** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10DataLoader** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX10DataLoader** tiene estos métodos.



| Método                                             | Descripción                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Descomprimir**](id3dx10dataloader-decompress.md) | Se usa para descomprimir los datos codificados. Normalmente, esto se usaría para cargar recursos desde sistemas de archivos, como archivos ZIP. Al cargar desde un recurso sin comprimir, la fase de descompresión no tiene que realizar ningún trabajo.<br/> |
| [**Destruir**](id3dx10dataloader-destroy.md)       | Lo usa una [**interfaz ID3DX10ThreadPump para**](id3dx10threadpump.md) destruir el cargador una vez completado un elemento de trabajo.<br/>                                                                                                   |
| [**Cargar**](id3dx10dataloader-load.md)             | Usado por una [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md) para cargar datos desde un disco.<br/>                                                                                                                            |



 

## <a name="remarks"></a>Comentarios

Este objeto se puede heredar y sus miembros se pueden volver a definir. Esto le permitiría personalizar la API para cargar y descomprimir sus propios formatos de archivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
