---
title: Elemento InfoCenter
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. | Elemento InfoCenter
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- Elemento InfoCenter Reproductor de Windows Media
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef62e0f6b41090642400a7f0a8b88af72818da4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249615"
---
# <a name="infocenter-element"></a>Elemento InfoCenter

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **elemento InfoCenter** especifica la dirección URL de la página web que Reproductor de Windows Media muestra en la característica Vista del Centro de información de **Reproducción** ahora cuando la tienda en línea está activa.

``` syntax
<InfoCenter
    URL = "URL"
/>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**Dirección URL** (obligatorio)
</dt> <dd>

Dirección URL de la página web Reproductor de Windows Media muestra.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento         |
|-----------------|-----------------|
| Elementos primarios | **ServiceInfo** |
| Elementos secundarios  | Ninguno            |



 

## <a name="remarks"></a>Observaciones

El usuario controla cuándo está activa la vista del Centro de información.

Para recuperar información sobre el elemento multimedia que se está reproduciendo actualmente, debe insertar una instancia de Reproductor de Windows Media control en la página web y usar el modelo de objetos Player.

En la tabla siguiente se detallan los parámetros enviados con la solicitud de dirección URL. Otros pueden estar presentes con fines de compatibilidad heredados.



| Nombre         | Value                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | Windows de ubicación geográfica. El usuario especifica el identificador de  ubicación en el área Ubicación de la configuración Regional e Idioma de Panel de control. |
| *locale*     | Reproductor de Windows Media de configuración regional.                                                                                                                                     |
| *userlocale* | Windows de configuración regional. El usuario especifica la configuración regional en el área **Estándares** y formatos de la configuración Regional y opciones de idioma Panel de control.        |
| *version*    | Reproductor de Windows Media número de versión con el siguiente formato: 10.0.x.xxxx o 11.0.x.xxxx.                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 10 o posterior.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Documento ServiceInfo de ejemplo para un almacén en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





