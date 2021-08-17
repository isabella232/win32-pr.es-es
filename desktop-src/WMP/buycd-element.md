---
title: Elemento BuyCD
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. | Elemento BuyCD
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- Elemento BuyCD Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc0b2af0f12b06c7d5701db3fcc073d7b7c330e8798408206b64a8b9811f27d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135848"
---
# <a name="buycd-element"></a>Elemento BuyCD

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **elemento BuyCD** especifica las direcciones URL de las páginas web que Reproductor de Windows Media cuando el usuario decide realizar una compra.

``` syntax
<BuyCD
    MediaPlayerURL = "URL"
    MediaCenterURL = "URL"
    BrowserURL = "URL"
/>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (obligatorio)
</dt> <dd>

Dirección URL de la página web que muestra la tienda en línea para ofrecer un CD o DVD para su compra en Reproductor de Windows Media.

</dd> <dt>

<span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**
</dt> <dd>

Dirección URL de la página web que la tienda en línea muestra para ofrecer un CD o DVD para su compra en Windows XP Media Center Edition 2004 Update.

</dd> <dt>

<span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**
</dt> <dd>

Dirección URL de la página web que muestra la tienda en línea para ofrecer un CD o DVD para su compra en una ventana del explorador independiente. Esta dirección URL también la usa Windows XP Service Pack 2 o posterior para la **característica en** línea Comprar música.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento         |
|-----------------|-----------------|
| Elementos primarios | **ServiceInfo** |
| Elementos secundarios  | Ninguno            |



 

## <a name="remarks"></a>Observaciones

Cuando el usuario hace clic en un botón o vínculo en Reproductor de Windows Media para comprar un CD o DVD, el reproductor envía la solicitud de dirección URL a ServiceTask1 con parámetros asociados mediante un separador de cadenas de consulta (?). En la tabla siguiente se detallan los parámetros enviados con la solicitud de dirección URL. Otros pueden estar presentes con fines de compatibilidad heredados.



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



 

Windows XP Media Center Edition 2004 proporciona a los usuarios una interfaz de usuario diseñada para visualizarse a distancia. Debe crear páginas web para que el *parámetro MediaCenterURL* se vea en pantallas grandes.

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

 

 





