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
ms.openlocfilehash: f55e6371f5c8d1e5dfcb17762340a82e8d921c17
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241958"
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

## <a name="remarks"></a>Observaciones

En Reproductor de Windows Media 10 o posterior, la propiedad **DownloadManager** y el objeto solo son accesibles desde los paneles de tareas del servicio de la tienda en línea. No se puede usar **DownloadManager desde otras** características en las que el **objeto** Externo está disponible, como HTMLView, vista del centro de información e información del álbum.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 2**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





