---
title: Elemento AlbumInfo
description: El elemento AlbumInfo especifica la dirección URL de la página web que Windows Media Player muestra cuando el usuario elige ver más información sobre un elemento multimedia determinado.
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- Elemento AlbumInfo Media Player Windows
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3805ae2d5fca687ce024efca74e0254db7c8ae3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699751"
---
# <a name="albuminfo-element"></a>Elemento AlbumInfo

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El elemento **AlbumInfo** especifica la dirección URL de la página web que Windows Media Player muestra cuando el usuario elige ver más información sobre un elemento multimedia determinado.

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obligatorio)
</dt> <dd>

Dirección URL de la página web que Windows Media Player muestra.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento         |
|-----------------|-----------------|
| Elementos primarios | **ServiceInfo** |
| Elementos secundarios  | Ninguno            |



 

## <a name="remarks"></a>Observaciones

Cuando el usuario hace clic en un botón de Windows Media Player para ver información adicional sobre un elemento multimedia determinado, el reproductor envía la solicitud de dirección URL con los parámetros adjuntos mediante un signo de interrogación (?) separador de cadena de consulta. En la tabla siguiente se detallan los parámetros que se envían con la solicitud URL. Otros pueden estar presentes para fines de compatibilidad heredada.



| Nombre         | Value                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Álbum*      | Valor del atributo **WM/álbum** para el elemento multimedia.                                                                                                        |
| *Artistas*     | Valor del atributo **WM/AlbumArtist** , si existe, o el valor del atributo **Author** del elemento multimedia.                                         |
| *Geoid*      | IDENTIFICADOR de ubicación geográfica de Windows. El ID. de ubicación lo especifica el usuario en el área **Ubicación** de la configuración de configuración regional y de idioma del panel de control. |
| *locale*     | IDENTIFICADOR de configuración regional de Windows Media Player.                                                                                                                                     |
| *Título*      | Valor del atributo **title** del elemento multimedia.                                                                                                                |
| *UFID*       | Valor del atributo **WM/UniqueFileIdentifier** para el elemento multimedia.                                                                                              |
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

 

 





