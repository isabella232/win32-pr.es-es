---
title: D3DX11_ERR enumeración (D3DX11.h)
description: 'Nota: La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Los errores se representan mediante valores negativos y no se pueden combinar.'
ms.assetid: d042621d-a20b-4945-b6aa-714a451aa88a
keywords:
- D3DX11_ERR enumeración Direct3D 11
- LPD3DX11_ERR puntero de enumeración Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_ERR
api_location:
- D3DX11.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d80b906b5b95693458eeea353f40fe446a22e8e33a6011b7851cf6d9663b3ed4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729325"
---
# <a name="d3dx11_err-enumeration"></a>Enumeración ERR D3DX11 \_

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Los errores se representan mediante valores negativos y no se pueden combinar. A continuación se muestra una lista de valores que pueden devolver los métodos incluidos con la biblioteca de utilidades D3DX. Consulte las descripciones de métodos individuales para obtener listas de los valores que cada uno puede devolver. Estas listas no son necesariamente completas.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX11_ERR { 
  D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX11_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX11_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX11_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX11_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX11_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX11_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX11_ERR, *LPD3DX11_ERR;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**ERROR D3DX11 \_ NO SE PUEDE MODIFICAR EL BÚFER DE \_ \_ \_ \_ ÍNDICE**
</dt> <dd>

No se puede modificar el búfer de índice.

</dd> <dt>

<span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11 \_ ERR \_ INVALID \_ MESH**
</dt> <dd>

La malla no es válida.

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**ERROR D3DX11 \_ NO SE PUEDE ORDENAR \_ \_ ATTR \_**
</dt> <dd>

La ordenación de atributos (D3DXMESHOPT \_ ATTRSORT) no se admite como técnica de optimización.

</dd> <dt>

<span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**D3DX11 \_ ERR \_ SKINNING \_ NOT \_ SUPPORTED**
</dt> <dd>

No se admite el desnasado.

</dd> <dt>

<span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11 \_ ERR \_ TOO \_ MANY \_ INFLUENCES**
</dt> <dd>

Demasiadas influencias especificadas.

</dd> <dt>

<span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11 \_ ERR DATOS NO \_ \_ VÁLIDOS**
</dt> <dd>

Los datos no son válidos.

</dd> <dt>

<span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**LA MALLA CARGADA DE ERRORES D3DX11 \_ \_ NO TIENE \_ \_ \_ \_ DATOS**
</dt> <dd>

La malla no tiene datos.

</dd> <dt>

<span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**FRAGMENTO CON NOMBRE DUPLICADO DE ERROR D3DX11 \_ \_ \_ \_**
</dt> <dd>

Ya existe un fragmento con ese nombre.

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**ERROR D3DX11 \_ NO SE PUEDE QUITAR EL ÚLTIMO \_ \_ \_ \_ ELEMENTO**
</dt> <dd>

No se puede eliminar el último elemento.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El código de la \_ instalación FACDD se usa para generar códigos de error, como en las macros siguientes.


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX11.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





