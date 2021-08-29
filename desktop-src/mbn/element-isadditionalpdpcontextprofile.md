---
description: IsAdditionalPdpContextProfile
MS-HAID: WWAN\_profile\_v3.element\_IsAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsAdditionalPdpContextProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae27c3df672750b1c396d6da3b99a7309d3d2fb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475151"
---
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile

El **elemento IsAdditionalPdpContextProfile** contiene un **valor booleano** que es **true** si se trata de un perfil de "contexto de PDP adicional (Protocolo de datos de paquetes) " y **false**, en caso contrario. El valor predeterminado es **false**.

Un perfil de "contexto de PDP adicional" es un perfil que no se activa a través del puerto predeterminado del adaptador físico y establecer este elemento en true garantiza que este perfil no se muestre de forma inapropiada en la interfaz de usuario.

Tenga en cuenta que si este elemento se establece en true, también debe cumplirse lo siguiente.

-   El [**elemento IsDefault**](./schema-isdefault-mbnprofile-element.md) debe no especificarse o establecerse en **false** para que el perfil sea válido.
-   El [**elemento ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) debe no especificarse o establecerse en **manual** para que el perfil sea válido.

## <a name="element-hierarchy"></a>Jerarquía de elemento

**<IsAdditionalPdpContextProfile>**

## <a name="syntax"></a>Syntax

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

Este elemento más externo (documento) no puede estar incluido en ningún otro elemento.

## <a name="requirements"></a>Requisitos


| | | <p>Espacio de nombres</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v3</p> | 


 

 
