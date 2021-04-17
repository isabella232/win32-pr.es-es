---
title: Elemento DownloadStatus (msfeeds. h)
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. | Elemento DownloadStatus (msfeeds. h)
ms.assetid: 08d9719a-390d-454a-935e-27812c0f3599
keywords:
- Elemento DownloadStatus Media Player Windows
topic_type:
- apiref
api_name:
- DownloadStatus Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431da810a9591d891fca914a9ecb6d3146a651d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699826"
---
# <a name="downloadstatus-element"></a>Elemento DownloadStatus

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El elemento **DownloadStatus** especifica una dirección URL que Windows Media Player muestra como un vínculo para permitir que los usuarios vean el estado de la descarga.

``` syntax
<DownloadStatus
    URL = "URL"
/>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="URL"></span><span id="url"></span>Dirección
</dt> <dd>

Dirección URL de la página web que la tienda en línea muestra para mostrar el estado de descarga al usuario.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento         |
|-----------------|-----------------|
| Elementos primarios | **ServiceInfo** |
| Elementos secundarios  | Ninguno            |



 

## <a name="remarks"></a>Observaciones

Windows Media Player muestra un mensaje a los usuarios cuando hay una descarga en curso. Si los servicios activos actuales definen una dirección URL de estado de descarga, el usuario puede hacer clic en el texto del mensaje. Cuando el usuario hace clic en el mensaje, el reproductor navega a la dirección URL especificada por el elemento **DownloadStatus** para que el almacén activo actual pueda proporcionar detalles sobre las descargas en curso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 10 o posterior<br/>                                          |
| Encabezado<br/>  | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





