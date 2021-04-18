---
title: DownloadItem. Cancel (método)
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método CANCEL cancela la descarga.
ms.assetid: b3715fde-6a83-45fa-92ea-1cbffbee7274
keywords:
- cancelar el método Media Player de Windows
- método CANCEL Windows Media Player, clase DownloadItem
- Clase DownloadItem Windows Media Player, método CANCEL
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
ms.openlocfilehash: c14d538e85d0930a43db883e226c007bea70de24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700084"
---
# <a name="downloaditemcancel-method"></a>DownloadItem. Cancel (método)

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El método **Cancel** cancela la descarga.

## <a name="syntax"></a>Sintaxis


```JScript
DownloadItem.cancel()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los elementos cancelados no se quitan de la colección de descargas. Los elementos cancelados devuelven un valor de **downloadState** de 4 (cancelado).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> <dt>

[**DownloadItem.downloadState**](downloaditem-downloadstate.md)
</dt> </dl>

 

 





