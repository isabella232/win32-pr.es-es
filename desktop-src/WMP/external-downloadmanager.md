---
title: External. DownloadManager
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad DownloadManager recupera el objeto DownloadManager.
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- Media Player de Windows externa. DownloadManager
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699762"
---
# <a name="externaldownloadmanager"></a>External. DownloadManager

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La propiedad **Downloadmanager** recupera el objeto **Downloadmanager** .

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un objeto **Downloadmanager** de solo lectura.

## <a name="remarks"></a>Observaciones

En Windows Media Player 10 o versiones posteriores, solo se puede tener acceso a la propiedad y el objeto **Downloadmanager** desde los paneles de tareas servicio de tienda en línea. No se puede usar el **Downloadmanager** de otras características en las que el objeto **externo** está disponible, como HTMLView, la vista del centro de información y la información del álbum.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 2**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





