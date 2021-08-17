---
title: Método DownloadItem.cancel
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método cancel cancela la descarga.
ms.assetid: b3715fde-6a83-45fa-92ea-1cbffbee7274
keywords:
- cancel method Reproductor de Windows Media
- método cancel Reproductor de Windows Media , Clase DownloadItem
- DownloadItem class Reproductor de Windows Media , cancel (método)
topic_type:
- apiref
api_name:
- DownloadItem.cancel
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6208719b5ac2e81fb9175db9de67bcf1f00ad7c34787ed1ab45251abd517bd65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749736"
---
# <a name="downloaditemcancel-method"></a>Método DownloadItem.cancel

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **método cancel** cancela la descarga.

## <a name="syntax"></a>Sintaxis


```JScript
DownloadItem.cancel()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Los elementos cancelados no se quitan de la colección de descarga. Los elementos cancelados devuelven **un valor downloadState** de 4 (cancelado).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DownloadItem (objeto)**](downloaditem-object.md)
</dt> <dt>

[**DownloadItem.downloadState**](downloaditem-downloadstate.md)
</dt> </dl>

 

 





