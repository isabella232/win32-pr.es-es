---
description: IsProvisioningProfile
MS-HAID: WWAN\_profile\_v4.element\_IsProvisioningProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsProvisioningProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0bacf17e9f9e73f4e442cff7c00acab79454e05
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883538"
---
# <a name="span-idwwan_profile_v4element_isprovisioningprofilespanisprovisioningprofile"></a><span id="WWAN_profile_v4.element_IsProvisioningProfile"></span>IsProvisioningProfile

Especifica que este perfil se usará solo para el aprovisionamiento. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto de Protocolo de datos de paquetes (PDP). Este elemento es nuevo para v4.

Si **IsProvisioningProfile** es true, [**IsDefault**](element-isdefault.md) debe ser false y [**ConnectionMode**](element-connectionmode.md) debe ser manual.

## <a name="element-hierarchy"></a>Jerarquía de elemento

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;IsProvisioningProfile&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<IsProvisioningProfile>

  boolean

</IsProvisioningProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Ninguno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios

Ninguno.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios


| Elemento primario | Descripción | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>El <strong>elemento MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior. Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</p><p>Puede haber más de un elemento MbnProfileExt en un perfil que describa la configuración del perfil para un conjunto determinado de condiciones de funcionamiento. Use el <a href="element-profileconditionedon.md"><strong>elemento secundario ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</p> | 


 

## <a name="requirements"></a>Requisitos


| | | <p>Espacio de nombres</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



