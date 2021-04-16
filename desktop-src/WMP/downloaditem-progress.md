---
title: DownloadItem. Progress
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad Progress recupera el progreso de la descarga en bytes.
ms.assetid: 58644eac-8dd0-4e9d-8055-03833c863a6e
keywords:
- DownloadItem. Progress Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.progress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1967c1eb3dc72c00b8b10b70da5d797343e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699487"
---
# <a name="downloaditemprogress"></a>DownloadItem. Progress

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La propiedad **Progress** recupera el progreso de la descarga en bytes.

## <a name="syntax"></a>Sintaxis

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).progress
      
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

[**DownloadItem. Size**](downloaditem-size.md)
</dt> </dl>

 

 





