---
title: pack_matrix Directiva pragma
description: Directiva pragma que especifica la alineación de empaquetado para matrices.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix pragma Directive HLSL
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bb5474702a1caba3f772002c34677601715caff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076747"
---
# <a name="pack_matrix-pragma-directive"></a>\_instrucción pragma Matrix (Directiva)

Directiva pragma que especifica la alineación de empaquetado para matrices.



| \#matriz de pragma Pack \_ ( *alignment* ) |
|--------------------------------------|



 

## <a name="parameters"></a>Parámetros



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="alignment"></span><span id="ALIGNMENT"></span><em>ecuación</em><br/></td>
<td>Alineación que se va a establecer para las matrices. Este parámetro puede tomar uno de los valores enumerados en la tabla siguiente. <br/> 
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>column_major</td>
<td>Predeterminada. Establece la alineación de empaquetado de la matriz en la columna principal.</td>
</tr>
<tr class="even">
<td>row_major</td>
<td>Establece la alineación de empaquetado de matriz en la fila principal.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se establece la alineación de empaquetado de matriz en la fila principal.


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Directivas de preprocesador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#pragma (Directiva) (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





