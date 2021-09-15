---
description: 'D3DX10_ERR enumeración: los errores se representan mediante valores negativos y no se pueden combinar.'
ms.assetid: 4149ce6d-e87a-4003-b123-5555c6b3b086
title: D3DX10_ERR enumeración (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ERR
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 520abae0409dd4214106363d7ffde0cfb5c81ff1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566748"
---
# <a name="d3dx10_err-enumeration"></a>Enumeración ERR D3DX10 \_

Los errores se representan mediante valores negativos y no se pueden combinar. A continuación se muestra una lista de valores que pueden devolver los métodos incluidos con la biblioteca de utilidades D3DX. Consulte las descripciones de métodos individuales para obtener listas de los valores que cada uno puede devolver. Estas listas no son necesariamente completas.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DX10_ERR { 
  D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX10_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX10_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX10_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX10_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX10_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX10_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX10_ERR, *LPD3DX10_ERR;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10 \_ ERR NO PUEDE MODIFICAR EL BÚFER DE \_ \_ \_ \_ ÍNDICE**
</dt> <dd>

No se puede modificar el búfer de índice.

</dd> <dt>

<span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**MALLA NO VÁLIDA DE ERROR D3DX10 \_ \_ \_**
</dt> <dd>

La malla no es válida.

</dd> <dt>

<span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**ERROR D3DX10 \_ NO SE PUEDE ORDENAR \_ \_ ATTR \_**
</dt> <dd>

La ordenación de atributos (D3DXMESHOPT \_ ATTRSORT) no se admite como técnica de optimización.

</dd> <dt>

<span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**D3DX10 \_ ERR \_ SKINNING \_ NOT \_ SUPPORTED**
</dt> <dd>

No se admite el desnasado.

</dd> <dt>

<span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10 \_ ERR \_ TOO \_ MANY \_ INFLUENCES**
</dt> <dd>

Demasiadas influencias especificadas.

</dd> <dt>

<span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3DX10 \_ ERR DATOS NO \_ \_ VÁLIDOS**
</dt> <dd>

Los datos no son válidos.

</dd> <dt>

<span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**LA MALLA CARGADA DE ERRORES D3DX10 \_ \_ NO TIENE \_ \_ \_ \_ DATOS**
</dt> <dd>

La malla no tiene datos.

</dd> <dt>

<span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**FRAGMENTO CON NOMBRE DUPLICADO DE ERROR D3DX10 \_ \_ \_ \_**
</dt> <dd>

Ya existe un fragmento con ese nombre.

</dd> <dt>

<span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10 \_ ERR NO PUEDE QUITAR EL ÚLTIMO \_ \_ \_ \_ ELEMENTO**
</dt> <dd>

No se puede eliminar el último elemento.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El código de instalación \_ FACDD se usa para generar códigos de error, como en las macros siguientes.


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
| Encabezado<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




