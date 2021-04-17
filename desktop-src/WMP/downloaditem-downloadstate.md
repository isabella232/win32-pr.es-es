---
title: DownloadItem.downloadState
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad downloadState recupera el estado de la descarga.
ms.assetid: dde27f43-40ee-4eb9-b316-42312ee937d0
keywords:
- DownloadItem. downloadState Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.downloadState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd2af2fab2ecb69df5b4695b227631b5be2dd96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700346"
---
# <a name="downloaditemdownloadstate"></a>DownloadItem.downloadState

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La propiedad **downloadState** recupera el estado de la descarga.

## <a name="syntax"></a>Sintaxis

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).downloadState
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura que contiene uno de los valores siguientes.



| Value | Descripción |
|-------|-------------|
| 0     | Downloading (Descargando) |
| 1     | En pausa      |
| 2     | Processing  |
| 3     | Completado   |
| 4     | Canceled    |



 

## <a name="remarks"></a>Observaciones

Los Estados de descarga se pueden producir en cualquier orden. No Escriba código que dependa de la aparición de un estado de descarga determinado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/>                                  |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





