---
description: IsLongStandingAdditionalPdpContextProfile
MS-HAID: WWAN\_profile\_v4.element\_IsLongStandingAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsLongStandingAdditionalPdpContextProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e257666dc91bd2a2153790e0ca4a32a72985075
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168190"
---
# <a name="span-idwwan_profile_v4element_islongstandingadditionalpdpcontextprofilespanislongstandingadditionalpdpcontextprofile"></a><span id="WWAN_profile_v4.element_IsLongStandingAdditionalPdpContextProfile"></span>IsLongStandingAdditionalPdpContextProfile

Especifica que este perfil es un perfil de contexto de PDP adicional de larga duración. Si el valor de este elemento es **true,** [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) también debe establecerse en **true.** Se trata de un nuevo elemento para v4.

## <a name="element-hierarchy"></a>Jerarquía de elemento

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;IsLongStandingAdditionalPdpContextProfile&gt;**

## <a name="syntax"></a>Sintaxis

``` syntax
<IsLongStandingAdditionalPdpContextProfile>

  boolean

</IsLongStandingAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Ninguno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios

Ninguno.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios


| Elemento primario | Descripción | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>El <strong>elemento MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior. Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</p><p>Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento. Use el <a href="element-profileconditionedon.md"><strong>elemento secundario ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento hacen que un perfil determinado sea el perfil activo.</p> | 


 

## <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p>Espacio de nombres</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
