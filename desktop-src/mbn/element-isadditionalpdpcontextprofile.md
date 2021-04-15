---
description: IsAdditionalPdpContextProfile
MS-HAID: WWAN\_profile\_v3.element\_IsAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsAdditionalPdpContextProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169aa9a34a561f65eed5dfc315e7711ef6bb9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360270"
---
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile

El elemento **IsAdditionalPdpContextProfile** contiene un **valor booleano** que es **true** si se trata de un perfil "PDP adicional (Protocolo de datos de paquetes)" y **false**, de lo contrario,. El valor predeterminado es **false**.

Un perfil de "contexto PDP adicional" es un perfil que no se activa a través del puerto predeterminado del adaptador físico y establecer este elemento en true garantiza que este perfil no se muestre de forma inapropiada en la interfaz de usuario.

Tenga en cuenta que si este elemento está establecido en true, también debe cumplirse lo siguiente.

-   El elemento [**IsDefault**](./schema-isdefault-mbnprofile-element.md) no debe especificarse o establecerse en **false** para que el perfil sea válido.
-   El elemento [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) debe estar sin especificar o establecerse en **manual** para que el perfil sea válido.

## <a name="element-hierarchy"></a>Jerarquía de elemento

**<IsAdditionalPdpContextProfile>**

## <a name="syntax"></a>Sintaxis

``` syntax
<IsAdditionalPdpContextProfile>

  boolean

</IsAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Ninguno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios

Ninguno.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios

Es posible que este elemento externo (documento) no esté incluido en otros elementos.

## <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Espacio de nombres</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v3</p></td>
</tr>
</tbody>
</table>

 

 
