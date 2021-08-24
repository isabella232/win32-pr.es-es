---
description: La interfaz ID3DXBuffer se usa como búfer de datos, almacenando información de vértices, adyacencias e materiales durante las operaciones de optimización y carga de malla.
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: Interfaz ID3DXBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cc69262949b9cc700f0a7c477bcfacb7dacd1fc51eb836ad76dfaa2fecb7358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121683"
---
# <a name="id3dxbuffer-interface"></a>Interfaz ID3DXBuffer

La interfaz ID3DXBuffer se usa como búfer de datos, almacenando información de vértices, adyacencias e materiales durante las operaciones de optimización y carga de malla. El objeto de búfer se usa para devolver datos de longitud arbitraria. Además, los objetos de búfer se usan para devolver código de objeto y mensajes de error en métodos que ensamblan sombreadores de vértices y píxeles.

## <a name="members"></a>Miembros

La **interfaz ID3DXBuffer** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXBuffer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXBuffer** tiene estos métodos.



| Método                                                    | Descripción                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [**GetBufferPointer**](id3dxbuffer--getbufferpointer.md) | Recupera un puntero a los datos del búfer.<br/>      |
| [**GetBufferSize**](id3dxbuffer--getbuffersize.md)       | Recupera el tamaño total de los datos del búfer.<br/> |



 

## <a name="remarks"></a>Comentarios

La **interfaz ID3DXBuffer** se obtiene llamando a la función [**D3DXCreateBuffer.**](d3dxcreatebuffer.md)

El tipo LPD3DXBUFFER se define como un puntero a la **interfaz ID3DXBuffer.**


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
