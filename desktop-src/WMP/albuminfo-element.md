---
title: Elemento AlbumInfo
description: El elemento AlbumInfo especifica la dirección URL de la página web que Reproductor de Windows Media cuando el usuario elige ver más información sobre un elemento multimedia determinado.
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- Elemento AlbumInfo Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9a5f8fab7da8f61ce6ee5451ebcef4dc33517aae2396f0817fac19222713db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055383"
---
# <a name="albuminfo-element"></a>Elemento AlbumInfo

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **elemento AlbumInfo** especifica la dirección URL de la página web que Reproductor de Windows Media cuando el usuario elige ver más información sobre un elemento multimedia determinado.

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**Dirección URL** (obligatorio)
</dt> <dd>

Dirección URL de la página web que Reproductor de Windows Media muestra.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento         |
|-----------------|-----------------|
| Elementos primarios | **ServiceInfo** |
| Elementos secundarios  | Ninguno            |



 

## <a name="remarks"></a>Observaciones

Cuando el usuario hace clic en un botón de Reproductor de Windows Media para ver información adicional sobre un elemento multimedia determinado, el Reproductor envía la solicitud de dirección URL con parámetros adjuntos mediante un separador de cadenas de consulta (?). En la tabla siguiente se detallan los parámetros enviados con la solicitud de dirección URL. Otros pueden estar presentes con fines de compatibilidad heredados.



| Nombre         | Value                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Álbum*      | Valor del **atributo WM/AlbumTitle** para el elemento multimedia.                                                                                                        |
| *Artista*     | Valor del **atributo WM/AlbumArtist,** si existe, o bien el valor del atributo **Author** para el elemento multimedia.                                         |
| *Geoid*      | Windows de ubicación geográfica. El usuario especifica el identificador de  ubicación en el área Ubicación de la configuración Regional e Idioma de Panel de control. |
| *locale*     | Reproductor de Windows Media de configuración regional.                                                                                                                                     |
| *Título*      | Valor del atributo **Title** para el elemento multimedia.                                                                                                                |
| *UFID*       | Valor del **atributo WM/UniqueFileIdentifier** para el elemento multimedia.                                                                                              |
| *userlocale* | Windows de configuración regional. El usuario especifica la configuración regional en el área **Estándares** y formatos de la configuración Regional y opciones de idioma Panel de control.        |
| *version*    | Reproductor de Windows Media número de versión con el siguiente formato: 10.0.x.xxxx o 11.0.x.xxxx.                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 10 o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Documento ServiceInfo de ejemplo para un almacén en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





