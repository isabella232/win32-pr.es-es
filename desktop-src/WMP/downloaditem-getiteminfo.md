---
title: DownloadItem.getItemInfo (método)
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método getItemInfo recupera el valor de un atributo para el elemento de descarga.
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- Método getItemInfo Reproductor de Windows Media
- Método getItemInfo Reproductor de Windows Media , clase DownloadItem
- DownloadItem class Reproductor de Windows Media , getItemInfo (método)
topic_type:
- apiref
api_name:
- DownloadItem.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e51414f70d518c37c560ee6f4db66994ed0cc0cadd95fc44e9f0d569601617ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935844"
---
# <a name="downloaditemgetiteminfo-method"></a>DownloadItem.getItemInfo (método)

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **método getItemInfo** recupera el valor de un atributo para el elemento de descarga.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = DownloadItem.getItemInfo(
  itemname
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*itemname* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo. Los valores admitidos son AlbumArtist, Album, Duration, WM/Provider, Title, UserRating y WM/TrackNumber.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena que** contiene el valor del atributo especificado por *itemname*.

## <a name="remarks"></a>Comentarios

Este método recupera los atributos especificados mediante la cadena de descripción de BITS. Vea [Reproductor de Windows Media de trabajo de BITS .](windows-media-player-bits-job-convention.md)

Este método es compatible con la descarga en segundo plano. El código no debe llamar a este método cuando se usa la descarga en tiempo real.

Este método puede recuperar información para los trabajos bits agregados durante la sesión Reproductor de Windows Media sesión actual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 10 o posterior<br/>                                        |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DownloadItem.type**](downloaditem-type.md)
</dt> <dt>

[**DownloadItem (objeto)**](downloaditem-object.md)
</dt> </dl>

 

 





