---
description: Objeto de carga de datos utilizado por la interfaz ID3DX10ThreadPump para cargar datos de forma asincrónica.
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: Interfaz ID3DX10DataLoader (D3DX10. h)
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
ms.openlocfilehash: b0e45d24d663f0ba9a8978bc251a4adf0c7868fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003830"
---
# <a name="id3dx10dataloader-interface"></a>Interfaz ID3DX10DataLoader

Objeto de carga de datos utilizado por la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md) para cargar datos de forma asincrónica.

## <a name="members"></a>Miembros

La interfaz **ID3DX10DataLoader** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10DataLoader** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX10DataLoader** tiene estos métodos.



| Método                                             | Descripción                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Descomprimir**](id3dx10dataloader-decompress.md) | Se usa para descomprimir datos codificados. Normalmente, esto se utilizaría para cargar recursos desde sistemas de archivos, como archivos ZIP. Al cargar desde un recurso sin comprimir, la fase de descompresión no tiene que realizar ningún trabajo.<br/> |
| [**Borrar**](id3dx10dataloader-destroy.md)       | Lo usa una [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md) para destruir el cargador una vez completado un elemento de trabajo.<br/>                                                                                                   |
| [**Cargar**](id3dx10dataloader-load.md)             | Lo usa una [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md) para cargar datos de un disco.<br/>                                                                                                                            |



 

## <a name="remarks"></a>Observaciones

Este objeto se puede heredar y sus miembros se pueden redefinir. Esto le permitirá personalizar la API para cargar y descomprimir sus propios formatos de archivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
