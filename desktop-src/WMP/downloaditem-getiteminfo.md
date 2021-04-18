---
title: DownloadItem. getItemInfo, método
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método getItemInfo recupera el valor de un atributo para el elemento de descarga.
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- método getItemInfo de Windows Media Player
- método getItemInfo de Windows Media Player, clase DownloadItem
- Clase DownloadItem Windows Media Player, método getItemInfo
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
ms.openlocfilehash: 1367e5c7a8990a9172ee758d2b811b9074ed02fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699494"
---
# <a name="downloaditemgetiteminfo-method"></a>DownloadItem. getItemInfo, método

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El método **getItemInfo** recupera el valor de un atributo para el elemento de descarga.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = DownloadItem.getItemInfo(
  itemname
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*itemname* \[ de\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo. Los valores admitidos son AlbumArtist, album, Duration, WM/Provider, title, UserRating y WM/TrackNumber.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena** que contiene el valor del atributo especificado por *itemname*.

## <a name="remarks"></a>Observaciones

Este método recupera los atributos especificados mediante la cadena de descripción de BITS. Vea [Convención de trabajo de Windows Media Player bits](windows-media-player-bits-job-convention.md).

Este método es compatible con la descarga en segundo plano. El código no debe llamar a este método cuando se usa la descarga en tiempo real.

Este método solo puede recuperar información de los trabajos de BITS agregados durante la sesión actual de Windows Media Player.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 10 o posterior<br/>                                        |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DownloadItem. tipo**](downloaditem-type.md)
</dt> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





