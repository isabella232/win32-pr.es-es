---
title: External.DownloadManager
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad DownloadManager recupera el objeto DownloadManager.
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- External.DownloadManager Reproductor de Windows Media
topic_type:
- apiref
api_name:
- External.DownloadManager
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d828435c43f57406e637312245b2bb3ae3e7c35510c9b2daf478a7fec39b599
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649215"
---
# <a name="externaldownloadmanager"></a>External.DownloadManager

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La **propiedad DownloadManager** recupera el **objeto DownloadManager.**

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un objeto **DownloadManager de** solo lectura.

## <a name="remarks"></a>Comentarios

En Reproductor de Windows Media 10 o posterior, la propiedad **DownloadManager** y el objeto solo son accesibles desde los paneles de tareas del servicio de la tienda en línea. No se puede usar **DownloadManager desde otras** características en las que el **objeto** Externo está disponible, como HTMLView, vista del centro de información e información del álbum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 2**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





