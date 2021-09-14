---
description: Contexto de MódemDMConfigProfile \/ (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Contexto (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8f463f14-95b3-4364-b1b1-549a32291959
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 36007bc1a7aecb25c2b6d61f74dd826e888a314b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168209"
---
# <a name="span-idwwan_profile_v4element_1_contextspanmodemdmconfigprofilecontext-v4"></a><span id="WWAN_profile_v4.element_1_Context"></span>Contexto de MódemDMConfigProfile \/ (v4)

Especifica los parámetros necesarios para establecer una conexión de datos.

## <a name="element-hierarchy"></a>Jerarquía de elemento

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a>Sintaxis

``` syntax
<Context>

  <!-- Child elements -->
  AccessString?,
  UserLogonCred?,
  Compression?,
  AuthProtocol?,
  IPType?

</Context>
```

### <a name="key"></a>Clave

`?`   opcional (cero o uno)

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
<td><a href="element-1-accessstring.md">AccessString</a></td>
<td><p>Identifica el APN o la cadena de marcado que se va a usar para establecer una conexión de datos.</p>
<p>Para obtener más información, vea la documentación del elemento <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-authprotocol.md">AuthProtocol</a></td>
<td><p>>Especifica el protocolo de autenticación que se usará para activar un contexto de Protocolo de datos de paquetes (PDP).</p>
<p>Tenga en cuenta que en v4, hay disponible un nuevo valor de enumeración para este elemento. <strong>AutoSelection</strong> significa que un protocolo de autenticación se debe seleccionar mediante capas inferiores.</p>
<p>Para más información, consulte la documentación del elemento <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-compression.md">Compresión</a></td>
<td><p>Especifica si se usará la compresión en el vínculo de datos para la transferencia de encabezados y datos.</p>
<p>Para obtener más información, vea la documentación del elemento <a href="../mbn/schema-compression-contexttype-element.md"><strong>Compression</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-iptype.md">IPType</a></td>
<td><p>Especifica el tipo de IP que se va a usar en esta conexión de datos.</p>
<p>Este elemento es nuevo en la versión 4 del esquema. El elemento puede tener uno de los valores siguientes.</p>
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valor predeterminado</td>
<td>El tipo de IP se debe seleccionar por capas inferiores.</td>
</tr>
<tr class="even">
<td>IPv4</td>
<td>Uso de IPv4</td>
</tr>
<tr class="odd">
<td>IPv6</td>
<td>Usar IPv6</td>
</tr>
<tr class="even">
<td>IPv4v6</td>
<td>Use IPv4 o IPv6, según esté disponible.</td>
</tr>
<tr class="odd">
<td>XLAT</td>
<td>Uso de 464XLAT para tuner IPv4 a través de redes IPv6</td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><a href="element-1-userlogoncred.md">UserLogonCred</a></td>
<td><p>Credenciales de inicio de sesión para una conexión.</p></td>
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
<p>Puede haber más de un elemento MbnProfileExt en un perfil que describa la configuración del perfil para un conjunto determinado de condiciones de funcionamiento. Use el <a href="element-profileconditionedon.md"><strong>elemento secundario ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</p></td>
</tr>
<tr class="even">
<td><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></td>
<td><p>Perfil de configuración de DM de módem.</p></td>
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

 

 



