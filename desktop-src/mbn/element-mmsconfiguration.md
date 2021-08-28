---
description: MmsConfiguration
MS-HAID: WWAN\_profile\_v4.element\_MmsConfiguration
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsConfiguration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff6612ce37bfa39b9498b6db4b9ce49cb06a6326
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982138"
---
# <a name="span-idwwan_profile_v4element_mmsconfigurationspanmmsconfiguration"></a><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration

Información de configuración de Multimedia Messaging Service (MMS).

Además de establecer los elementos de configuración dentro de este elemento, un perfil mms debe tener la siguiente configuración.

-   Su [**elemento Name**](element-name.md) debe contener un nombre único para todo el sistema.
-   Su [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) debe establecerse en **UserProvisioned.**
-   Su [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) debe contener el VALOR DE LA SIM para el que está pensado este perfil.
-   Su [**ConnectionMode debe**](./schema-connectionmode-mbnprofile-element.md) establecerse en **Manual.**
-   [**PurposeGroupGuid debe**](element-purposegroupguid.md) contener el GUID para el grupo de propósito de MMS.
-   Su [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) debe establecerse en **true.**

## <a name="element-hierarchy"></a>Jerarquía de elemento

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;MmsConfiguration&gt;**

## <a name="syntax"></a>Sintaxis

``` syntax
<MmsConfiguration>

  <!-- Child elements -->
  MmscUrl?,
  MmscPort?,
  MmsMaximumMessageSize?

</MmsConfiguration>
```

### <a name="key"></a>Clave

`?`   opcional (cero o uno)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Ninguno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios


| Elemento secundario | Descripción | 
|---------------|-------------|
| <a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a> | <p>Especifica el tamaño máximo de los mensajes MMS, en kilobytes. Opcional.</p> | 
| <a href="element-mmscport.md">MmscPort</a> | <p>Especifica el número de puerto del servidor MMSC para el dispositivo. Especifique 0 para indicar que no se ha especificado ningún puerto específico. Opcional.</p> | 
| <a href="element-mmscurl.md">MmscUrl</a> | <p>Especifica la dirección URL del servidor MMSC para el dispositivo. Opcional.</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios


| Elemento primario | Descripción | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>El <strong>elemento MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior. Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</p><p>Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento. Use el <a href="element-profileconditionedon.md"><strong>elemento secundario ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento hacen que un perfil determinado sea el perfil activo.</p> | 


 

## <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p>Espacio de nombres</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
