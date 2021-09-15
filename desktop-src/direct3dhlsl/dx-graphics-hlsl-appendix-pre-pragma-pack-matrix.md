---
title: pack_matrix directiva pragma
description: Directiva Pragma que especifica la alineación de empaquetado para matrices.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix directiva pragma HLSL
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 87658a9ffcf2d8715e2caa581c7127301784980c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568384"
---
# <a name="pack_matrix-pragma-directive"></a>directiva \_ pragma de matriz de paquetes

Directiva Pragma que especifica la alineación de empaquetado para matrices.



| \#pragma pack \_ matrix( *alignment* ) |
|--------------------------------------|



 

## <a name="parameters"></a>Parámetros



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="alignment"></span><span id="ALIGNMENT"></span><em>Alineación</em><br/></td>
<td>Alineación que se establecerá para matrices. Este parámetro puede tomar uno de los valores enumerados en la tabla siguiente. <br/> 
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
<td>Predeterminada. Establece la alineación del empaquetado de la matriz en la columna principal.</td>
</tr>
<tr class="even">
<td>row_major</td>
<td>Establece la alineación de empaquetado de matriz en fila principal.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se establece la alineación de empaquetado de matriz en fila principal.


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Directivas de preprocesador (HLSL de DirectX)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#directiva pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





