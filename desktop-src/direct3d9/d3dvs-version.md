---
description: Cree un token de número de versión del sombreador de vértices.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: Macro D3DVS_VERSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 915d5b843287602c80572d739d8b369d8c301770
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718311"
---
# <a name="d3dvs_version-macro"></a>D3DVS \_ versión (macro)

Cree un token de número de versión del sombreador de vértices.

## <a name="syntax"></a>Sintaxis


```C++
DWORD D3DVS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*\_Principales* 
</dt> <dd>

Versión principal del sombreador de vértices. Vea la sección Comentarios para obtener los valores adecuados.

</dd> <dt>

*\_Minor* 
</dt> <dd>

Versión secundaria del sombreador de vértices. Vea la sección Comentarios para obtener los valores adecuados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor DWORD que es una versión del sombreador de vértices.

## <a name="remarks"></a>Observaciones

Números de versión

El número de versión es una combinación de la versión principal y los números de versión del sombreador de vértices secundarios. Los números válidos se muestran en la tabla.



| Principal | Minor | Ejemplo             |
|-------|-------|---------------------|
| 1     | 1     | \_Versión de D3DVS (1,1) |
| 2     | 0     | \_Versión de D3DVS (2,0) |
| 3     | 0     | \_Versión de D3DVS (3, 0) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




