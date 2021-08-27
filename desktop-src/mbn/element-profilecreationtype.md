---
description: ProfileCreationType (en MBNProfileExt)
MS-HAID: WWAN\_profile\_v4.element\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileCreationType (en MBNProfileExt)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29892e6a9dd0f32bb571103668d3a2d7dea32311
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473951"
---
# <a name="span-idwwan_profile_v4element_profilecreationtypespanprofilecreationtype-in-mbnprofileext"></a><span id="WWAN_profile_v4.element_ProfileCreationType"></span>ProfileCreationType (en MBNProfileExt)

Especifica el creador del perfil.

Para obtener más información sobre este elemento, vea la documentación del elemento [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) v1.

## <a name="element-hierarchy"></a>Jerarquía de elemento

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileCreationType>**

## <a name="syntax"></a>Syntax

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
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


 

## <a name="related-elements"></a>Elementos relacionados

Los elementos siguientes tienen el mismo nombre que este, pero contenido o atributos diferentes:

-   **[ProfileCreationType (en ModemDMConfigProfile)](element-1-profilecreationtype.md)**

## <a name="requirements"></a>Requisitos


| | | <p>Espacio de nombres</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
