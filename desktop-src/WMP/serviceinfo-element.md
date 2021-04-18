---
title: ServiceInfo, elemento
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El elemento ServiceInfo es el elemento principal del documento ServiceInfo.xml.
ms.assetid: d2f9e642-143e-405d-8588-c78e4355b9b9
keywords:
- Elemento ServiceInfo Media Player Windows
topic_type:
- apiref
api_name:
- ServiceInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ac41edd4ae8548ecdb6d3ef6631fba5d6175762
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649822"
---
# <a name="serviceinfo-element"></a>ServiceInfo, elemento

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El elemento **ServiceInfo** es el elemento principal del documento ServiceInfo.xml.

``` syntax
<ServiceInfo
    Version = 1.00
    Key = "service key"
    ContentPartner = "true|false"
/>
```

## <a name="attributes"></a>Atributos



| Término                                                                                                                                             | Descripción                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Versión** (opcional)<br/> | Versión del archivo de ServiceInfo.xml. La versión 1,00 es compatible con Windows Media Player.<br/>                                                                                                                                                            |
| <span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Clave** (obligatorio)<br/>                 | Cadena de clave de servicio que identifica de forma única la tienda en línea.<br/>                                                                                                                                                                                   |
| <span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**<br/>                 | Indica si la tienda en línea es un almacén de tipo 1. Un valor de "true" indica que el almacén es un almacén de tipo 1. Un valor de "false" indica que el almacén no es un almacén de tipo 1; es decir, es un almacén de tipo 2. El valor predeterminado es "false".<br/> |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos primarios | None                                                                                                                                                                               |
| Elementos secundarios  | **AlbumInfo**, **BuyCD**, **color**, **Description**, **FriendlyName**, **HTMLView**, **Image**, **Infocenter**, **install**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |



 

## <a name="remarks"></a>Observaciones

En la tabla siguiente se detallan los parámetros que se envían con la solicitud URL. Otros pueden estar presentes para fines de compatibilidad heredada. La solicitud también incluirá los parámetros especificados mediante el parámetro de línea de comandos ServiceExtra de Windows Media Player el programa de instalación.



| Nombre         | Value                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | IDENTIFICADOR de ubicación geográfica de Windows. El ID. de ubicación lo especifica el usuario en el área **Ubicación** de la configuración de configuración regional y de idioma del panel de control. |
| *locale*     | IDENTIFICADOR de configuración regional de Windows Media Player.                                                                                                                                     |
| *UserLocale* | IDENTIFICADOR de configuración regional de Windows. El usuario especifica la configuración regional en el área **estándares y formatos** de la configuración configuración regional y de idioma del panel de control.        |
| *version*    | Windows Media Player número de versión con el formato siguiente: 10.0. x. xxxx o 11.0. x. xxxx.                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------|
| Versión<br/> | Windows Media Player 10 o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





