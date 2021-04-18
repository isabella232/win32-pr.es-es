---
title: DownloadItem. Size
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad Size recupera el tamaño de la descarga.
ms.assetid: e0fd9cb5-155a-4159-94b8-1bf05b4d1062
keywords:
- DownloadItem. Size Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.size
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0ebb1ce15d34ad04095f1ef1ed84ad2df008c7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699747"
---
# <a name="downloaditemsize"></a>DownloadItem. Size

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La propiedad **size** recupera el tamaño de la descarga.

## <a name="syntax"></a>Sintaxis

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).size
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura (**Long**).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/>                                  |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> <dt>

[**DownloadItem. Progress**](downloaditem-progress.md)
</dt> </dl>

 

 





