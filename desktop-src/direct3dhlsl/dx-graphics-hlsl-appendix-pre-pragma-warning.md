---
title: Warning (Directiva pragma)
description: Directiva pragma que modifica el comportamiento de los mensajes de advertencia del compilador.
ms.assetid: 69488014-36e3-4c87-8b65-6123b5e87bcb
keywords:
- Warning (Directiva pragma) HLSL
topic_type:
- apiref
api_name:
- warning pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7599886b47830b33c69f11c0c341c7775c644dd3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994710"
---
# <a name="warning-pragma-directive"></a>Warning (Directiva pragma)

Directiva pragma que modifica el comportamiento de los mensajes de advertencia del compilador.



| \#pragma warning ( *Warning-Specifier* : *Warning-Number-List* \[ ; *Warning-Specifier* : *ADVERTENCIA-número-lista*... \] ) |
|----------------------------------------------------------------------------------------------------------------------|



 

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
<td><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>Warning-Specifier</em><br/></td>
<td>Comportamiento que se va a establecer para las advertencias especificadas. Este parámetro puede tomar uno de los valores enumerados en la tabla siguiente. <br/> 
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>once</td>
<td>Muestra el mensaje de las advertencias con los números especificados una sola vez.</td>
</tr>
<tr class="even">
<td>default</td>
<td>Restablezca el comportamiento de las advertencias con los números especificados a su valor predeterminado. Esto también tiene el efecto de activar una advertencia en que está desactivada de forma predeterminada. La advertencia se generará en su nivel predeterminado.</td>
</tr>
<tr class="odd">
<td>1, 2, 3, 4</td>
<td>Aplica el nivel especificado a las advertencias con los números especificados. Esto también tiene el efecto de activar una advertencia en que está desactivada de forma predeterminada.</td>
</tr>
<tr class="even">
<td>disable</td>
<td>No emita las advertencias con los números especificados.</td>
</tr>
<tr class="odd">
<td>error</td>
<td>Notificar las advertencias con los números especificados como errores.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>ADVERTENCIA: número-lista</em></p></td>
<td><p>Lista delimitada por espacios en blanco de los números de las advertencias para modificar el comportamiento de.</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Puede especificar cualquier número de cambios de comportamiento de advertencia distintos dentro de la misma pragma warning separando los cambios con punto y coma.

El compilador agregará 4000 a cualquier número de advertencia que esté entre 0 y 999. Para los números de advertencia mayores que 4699 (los asociados a la generación de código), la pragma warning solo tiene efecto cuando se colocan fuera de las definiciones de función. La Directiva pragma se omite si especifica un número mayor que 4699 y se utiliza dentro de una función.

La instrucción pragma de advertencia de HLSL no admite la **funcionalidad de** **extracción** y de confirmación de la pragma warning incluida en el compilador de C++.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se deshabilitan las advertencias 4507 y 4034, se muestra la advertencia 4385 una vez y se notifica la advertencia 4164 como un error.


```
#pragma warning( disable : 4507 34; once : 4385; error : 164 )
```



El ejemplo anterior es funcionalmente equivalente a lo siguiente:


```
#pragma warning( disable : 4507 34 )
#pragma warning( once : 4385 )
#pragma warning( error : 164 )
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Directivas de preprocesador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#pragma (Directiva) (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





