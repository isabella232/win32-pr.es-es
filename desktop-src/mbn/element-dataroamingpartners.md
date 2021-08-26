---
description: DataRoamingPartners
MS-HAID: WWAN\_profile\_v4.element\_DataRoamingPartners
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: DataRoamingPartners
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c29edf9c-4e70-4b8f-8c71-0ec8a9fad60d
api_name:
- DataRoamingPartners
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: eb304a89faca2381f8c8c0ede6ba743f740c4d0f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468902"
---
# <a name="span-idwwan_profile_v4element_dataroamingpartnersspandataroamingpartners"></a><span id="WWAN_profile_v4.element_DataRoamingPartners"></span>DataRoamingPartners

Especifica una lista de proveedores de red preferidos en itinerancia.

Para obtener más información, consulte la documentación del elemento [**DataRoamingPartners**](./schema-dataroamingpartners-mbnprofile-element.md) v1.

## <a name="element-hierarchy"></a>Jerarquía de elemento

[<MBNProfileExt>](element-mbnprofileext.md)  
**<DataRoamingPartners>**

## <a name="syntax"></a>Syntax

``` syntax
<DataRoamingPartners>

  <!-- Child elements -->
  Provider+

</DataRoamingPartners>
```

### <a name="key"></a>Clave

`+`   requerido (uno o varios)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Ninguno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios


| Elemento secundario | Descripción | 
|---------------|-------------|
| <a href="element-provider.md">Proveedor</a> | <p>Especifica un proveedor de red preferido en una lista de proveedores que se usarán durante la itinerancia.</p><p>El valor de este elemento es una instancia del tipo complejo <a href="../mbn/schema-providertype-complextype.md"><strong>providerType</strong></a> v1.</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios


| Elemento primario | Descripción | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>El <strong>elemento MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior. Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</p><p>Puede haber más de un elemento MbnProfileExt en un perfil que describa la configuración del perfil para un conjunto determinado de condiciones de funcionamiento. Use el <a href="element-profileconditionedon.md"><strong>elemento secundario ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</p> | 


 

## <a name="requirements"></a>Requisitos


| | | <p>Espacio de nombres</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
