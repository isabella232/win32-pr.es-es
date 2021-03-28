---
title: Enumeración D3DX11_ERR (D3DX11. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Los errores se representan con valores negativos y no se pueden combinar.
ms.assetid: d042621d-a20b-4945-b6aa-714a451aa88a
keywords:
- Enumeración de D3DX11_ERR Direct3D 11
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
ms.openlocfilehash: 0607bd495bad4bdeacf66ae593670dbe3ad0d2e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998689"
---
# <a name="d3dx11_err-enumeration"></a>\_Enumeración de D3DX11 Err

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

Los errores se representan con valores negativos y no se pueden combinar. A continuación se muestra una lista de los valores que pueden ser devueltos por los métodos incluidos en la biblioteca de utilidades de D3DX. Vea las descripciones individuales de cada método para ver las listas de los valores que puede devolver. Estas listas no son necesariamente completas.

## <a name="syntax"></a>Sintaxis


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

<span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11 \_ Err \_ no puede \_ modificar el \_ búfer de índice \_**
</dt> <dd>

No se puede modificar el búfer de índice.

</dd> <dt>

<span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11 \_ Err \_ no válida \_ Mesh**
</dt> <dd>

La malla no es válida.

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11 \_ Err \_ no se puede \_ ordenar el atributo \_**
</dt> <dd>

La ordenación de atributos (D3DXMESHOPT \_ ATTRSORT) no se admite como técnica de optimización.

</dd> <dt>

<span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**\_No se \_ \_ \_ admiten los aspectos de D3DX11 Err**
</dt> <dd>

No se admite la recubrimiento.

</dd> <dt>

<span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11 \_ Err \_ demasiadas \_ \_ influencias**
</dt> <dd>

Se han especificado demasiadas influencias.

</dd> <dt>

<span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11 \_ Err \_ invalid \_ Data**
</dt> <dd>

Los datos no son válidos.

</dd> <dt>

<span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**D3DX11 el error de la \_ \_ \_ malla cargada \_ \_ no tiene \_ datos**
</dt> <dd>

La malla no tiene datos.

</dd> <dt>

<span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**D3DX11 \_ Err \_ Duplicate \_ nombre \_ FRAGMENT**
</dt> <dd>

Ya existe un fragmento con ese nombre.

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11 \_ Err \_ no puede \_ quitar el \_ último \_ elemento**
</dt> <dd>

No se puede eliminar el último elemento.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El código de instalación \_ FACDD se utiliza para generar códigos de error, como en las siguientes macros.


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
| Encabezado<br/> | <dl> <dt>D3DX11. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





