---
title: DownloadItem.downloadState
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad downloadState recupera el estado de la descarga.
ms.assetid: dde27f43-40ee-4eb9-b316-42312ee937d0
keywords:
- DownloadItem.downloadState Reproductor de Windows Media
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
ms.openlocfilehash: a3f2f1d7338370aaa5132c479d155ffbfc4282a686d082df37446be053efab3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997055"
---
# <a name="downloaditemdownloadstate"></a>DownloadItem.downloadState

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La **propiedad downloadState** recupera el estado de la descarga.

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).downloadState
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** que contiene uno de los valores siguientes.



| Value | Descripción |
|-------|-------------|
| 0     | Downloading (Descargando) |
| 1     | En pausa      |
| 2     | Processing  |
| 3     | Completado   |
| 4     | Canceled    |



 

## <a name="remarks"></a>Comentarios

Los estados de descarga pueden producirse en cualquier orden. No escriba código que dependa de la aparición de un estado de descarga determinado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/>                                  |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DownloadItem (objeto)**](downloaditem-object.md)
</dt> </dl>

 

 





