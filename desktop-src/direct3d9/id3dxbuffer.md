---
description: La interfaz ID3DXBuffer se usa como un búfer de datos, que almacena información de vértices, de adyacencias y de material durante las operaciones de carga y optimización de malla.
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: Interfaz ID3DXBuffer (D3DX9Mesh. h)
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
ms.openlocfilehash: 5fff273d2e38daeb003fb360f099e7a7b4985504
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678803"
---
# <a name="id3dxbuffer-interface"></a>Interfaz ID3DXBuffer

La interfaz ID3DXBuffer se usa como un búfer de datos, que almacena información de vértices, de adyacencias y de material durante las operaciones de carga y optimización de malla. El objeto de búfer se usa para devolver datos de longitud arbitraria. Además, los objetos de búfer se usan para devolver código objeto y mensajes de error en métodos que ensamblan sombreadores de píxeles y vértices.

## <a name="members"></a>Miembros

La interfaz **ID3DXBuffer** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXBuffer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXBuffer** tiene estos métodos.



| Método                                                    | Descripción                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [**GetBufferPointer**](id3dxbuffer--getbufferpointer.md) | Recupera un puntero a los datos del búfer.<br/>      |
| [**GetBufferSize**](id3dxbuffer--getbuffersize.md)       | Recupera el tamaño total de los datos en el búfer.<br/> |



 

## <a name="remarks"></a>Observaciones

La interfaz **ID3DXBuffer** se obtiene mediante una llamada a la función [**D3DXCreateBuffer**](d3dxcreatebuffer.md) .

El tipo LPD3DXBUFFER se define como un puntero a la interfaz **ID3DXBuffer** .


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
