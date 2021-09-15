---
title: warning pragma (directiva)
description: Directiva Pragma que modifica el comportamiento de los mensajes de advertencia del compilador.
ms.assetid: 69488014-36e3-4c87-8b65-6123b5e87bcb
keywords:
- advertencia de directiva pragma HLSL
topic_type:
- apiref
api_name:
- warning pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d98e80ba691422b0a197b732dbc5fc762a25562
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568381"
---
# <a name="warning-pragma-directive"></a>warning pragma (directiva)

Directiva Pragma que modifica el comportamiento de los mensajes de advertencia del compilador.



| \#pragma warning( *warning-specifier* : *warning-number-list* \[ ; *warning-specifier:* *warning-number-list*... \] ) |
|----------------------------------------------------------------------------------------------------------------------|



 

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
<td><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>warning-specifier</em><br/></td>
<td>Comportamiento que se establece para las advertencias especificadas. Este parámetro puede tomar uno de los valores enumerados en la tabla siguiente. <br/> 
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
<td>Muestra el mensaje de las advertencias con los números especificados solo una vez.</td>
</tr>
<tr class="even">
<td>default</td>
<td>Restablezca el comportamiento de las advertencias con los números especificados a su valor predeterminado. Esto también tiene el efecto de activar una advertencia que está desactivada de forma predeterminada. La advertencia se generará en su nivel predeterminado.</td>
</tr>
<tr class="odd">
<td>1, 2, 3, 4</td>
<td>Aplique el nivel especificado a las advertencias con los números especificados. Esto también tiene el efecto de activar una advertencia que está desactivada de forma predeterminada.</td>
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
<td><p><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>warning-number-list</em></p></td>
<td><p>Lista delimitada por espacios en blanco de los números de las advertencias de las que se modificará el comportamiento.</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Puede especificar cualquier número de cambios de comportamiento de advertencia distintos dentro de la misma pragma de advertencia separando los cambios con punto y coma.

El compilador agregará 4000 a cualquier número de advertencia que esté entre 0 y 999. Para los números de advertencia mayores que 4699, (los asociados a la generación de código) la pragma de advertencia solo tiene efecto cuando se coloca fuera de las definiciones de función. La pragma se omite si especifica un número mayor que 4699 y se usa dentro de una función.

La pragma de advertencia hlsl  no admite la funcionalidad **de** inserción y pop de la pragma de advertencia incluida en el compilador de C++.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se deshabilitan las advertencias 4507 y 4034, se muestra la advertencia 4385 una vez y se notifica la advertencia 4164 como un error.


```
#pragma warning( disable : 4507 34; once : 4385; error : 164 )
```



El ejemplo anterior es funcionalmente equivalente al siguiente:


```
#pragma warning( disable : 4507 34 )
#pragma warning( once : 4385 )
#pragma warning( error : 164 )
```



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Directivas de preprocesador (HLSL de DirectX)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#directiva pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





