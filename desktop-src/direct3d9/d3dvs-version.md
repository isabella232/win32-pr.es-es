---
description: Cree un token de número de versión del sombreador de vértices.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: D3DVS_VERSION macro (D3d9types.h)
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
ms.openlocfilehash: 861295c9068bee9e40174d877a78628aa405b9cfa5d46414190fbb7b37904e89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527261"
---
# <a name="d3dvs_version-macro"></a>Macro D3DVS \_ VERSION

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

*\_Principal* 
</dt> <dd>

La versión principal del sombreador de vértices. Consulte los comentarios para obtener los valores adecuados.

</dd> <dt>

*\_Minor* 
</dt> <dd>

Versión del sombreador de vértices secundaria. Consulte los comentarios para obtener los valores adecuados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor DWORD que es una versión del sombreador de vértices.

## <a name="remarks"></a>Comentarios

Números de versión

El número de versión es una combinación de la versión principal y los números de versión del sombreador de vértices menores. Los números válidos se muestran en la tabla.



| Principal | Minor | Ejemplo             |
|-------|-------|---------------------|
| 1     | 1     | D3DVS \_ VERSION(1,1) |
| 2     | 0     | D3DVS \_ VERSION(2,0) |
| 3     | 0     | D3DVS \_ VERSIÓN(3,0) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




