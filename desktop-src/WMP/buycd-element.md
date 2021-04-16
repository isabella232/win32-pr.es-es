---
title: Elemento BuyCD
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. | Elemento BuyCD
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- Elemento BuyCD Media Player Windows
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca1ebe4bd85015ca9ce1c0bece24e7dc47ff9fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699625"
---
# <a name="buycd-element"></a>Elemento BuyCD

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El elemento **BuyCD** especifica las direcciones URL de las páginas web que Windows Media Player muestra cuando el usuario decide hacer una compra.

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

Dirección URL de la página web que muestra la tienda en línea para ofrecer un CD o DVD para la compra en Windows Media Player.

</dd> <dt>

<span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**
</dt> <dd>

Dirección URL de la página web que se muestra en la tienda en línea para ofrecer un CD o DVD para la compra en la actualización 2004 de Windows XP Media Center Edition.

</dd> <dt>

<span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**
</dt> <dd>

Dirección URL de la página web que la tienda en línea muestra para ofrecer un CD o DVD para la compra en una ventana del explorador independiente. Windows XP Service Pack 2 o posterior usa esta dirección URL para la característica de la **tienda de música en línea** .

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento         |
|-----------------|-----------------|
| Elementos primarios | **ServiceInfo** |
| Elementos secundarios  | Ninguno            |



 

## <a name="remarks"></a>Observaciones

Cuando el usuario hace clic en un botón o vínculo de Windows Media Player para adquirir un CD o DVD, el reproductor envía la solicitud de dirección URL a ServiceTask1 con los parámetros adjuntos mediante un signo de interrogación (?) separador de cadena de consulta. En la tabla siguiente se detallan los parámetros que se envían con la solicitud URL. Otros pueden estar presentes para fines de compatibilidad heredada.



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



 

Windows XP Media Center Edition 2004 proporciona a los usuarios una interfaz de usuario diseñada para su visualización a distancia. Debe crear páginas web para que el parámetro *MediaCenterURL* se vea en pantallas de gran tamaño.

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

 

 





