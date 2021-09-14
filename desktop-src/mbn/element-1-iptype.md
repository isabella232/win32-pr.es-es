---
description: '\/MódemDMConfigProfile... \/ IPType (v4)'
MS-HAID: WWAN\_profile\_v4.element\_1\_IPType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPType (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09ff4fd6c0290c29aa8737efea5d94da2d2025cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168206"
---
# <a name="span-idwwan_profile_v4element_1_iptypespanmodemdmconfigprofileiptype-v4"></a><span id="WWAN_profile_v4.element_1_IPType"></span>\/MódemDMConfigProfile... \/ IPType (v4)

Especifica el tipo de IP que se va a usar en esta conexión de datos.

Este elemento es nuevo en la versión 4 del esquema. El elemento puede tener uno de los valores siguientes.

| Value   | Significado                                       |
|---------|-----------------------------------------------|
| Valor predeterminado | El tipo de IP se debe seleccionar por capas inferiores.     |
| IPv4    | Uso de IPv4                                      |
| IPv6    | Usar IPv6                                      |
| IPv4v6  | Use IPv4 o IPv6, según esté disponible.           |
| XLAT    | Uso de 464XLAT para tuner IPv4 a través de redes IPv6 |

 

## <a name="element-hierarchy"></a>Jerarquía de elemento

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

## <a name="syntax"></a>Sintaxis

``` syntax
<IPType>

  "Default" | "IPv4" | "IPv6" | "IPv4v6" | "XLAT"

</IPType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Ninguno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios

Ninguno.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios


| Elemento primario | Descripción | 
|----------------|-------------|
| <a href="element-1-context.md">Contexto</a> | <p>Especifica los parámetros necesarios para establecer una conexión de datos.</p> | 


 

## <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p>Espacio de nombres</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



