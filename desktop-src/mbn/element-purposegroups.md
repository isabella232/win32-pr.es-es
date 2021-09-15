---
description: PurposeGroups
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroups
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PurposeGroups
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa1daa1b6b1985ddbc94eb302adf15a1b88e2d8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468779"
---
# <a name="span-idwwan_profile_v4element_purposegroupsspanpurposegroups"></a><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups

Una lista opcional de grupos de perfiles, donde cada grupo incluye perfiles usados para un propósito común.

Este elemento es nuevo para la versión 4 del esquema.

Un perfil se puede enumerar en varios grupos.

## <a name="element-hierarchy"></a>Jerarquía de elemento

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;PurposeGroups&gt;**

## <a name="syntax"></a>Sintaxis

``` syntax
<PurposeGroups>

  <!-- Child elements -->
  PurposeGroupGuid{1,10}

</PurposeGroups>
```

### <a name="key"></a>Clave

`{}`   intervalo específico de repeticiones

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Ninguno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Elemento secundario</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-purposegroupguid.md">PurposeGroupGuid</a></td>
<td><p>Representa un perfil en un PurposeGroup de perfiles.</p>
<p>Los perfiles se especifican por su <a href="simpletype-guidtype.md"><strong>valor guidType.</strong></a></p>
<p>Se definen cuatro valores GUID, como se muestra en la tabla siguiente.</p>
<table>
<thead>
<tr class="header">
<th>Grupo de propósitos</th>
<th>GUID</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Internet</td>
<td>3E5545D2-1137-4DC8-A198-33F1C657515F</td>
</tr>
<tr class="even">
<td>mms</td>
<td>53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</td>
</tr>
<tr class="odd">
<td>IMS</td>
<td>474D66ED-0E4B-476B-A455-19BB1239ED13</td>
</tr>
<tr class="even">
<td>SUPL</td>
<td>6D42669F-52A9-408E-9493-1071DCC437BD</td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Elemento primario</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-mbnprofileext.md">MBNProfileExt</a></td>
<td><p>El <strong>elemento MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior. Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</p>
<p>Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento. Use el <a href="element-profileconditionedon.md"><strong>elemento secundario ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento hacen que un perfil determinado sea el perfil activo.</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Espacio de nombres</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



