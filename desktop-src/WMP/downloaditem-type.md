---
title: DownloadItem. tipo
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad Type recupera el tipo de la descarga.
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- DownloadItem. Escriba Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.type
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cdcf21ce7443d7730d4a75518fb4749af0b9e52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699423"
---
# <a name="downloaditemtype"></a>DownloadItem. tipo

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La propiedad **Type** recupera el tipo de la descarga.

## <a name="syntax"></a>Sintaxis

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de solo lectura que contiene uno de los valores siguientes.



| Value      | Descripción                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| background | (Solo Windows XP). La descarga se produce como un proceso en segundo plano a medida que el tiempo de procesador está disponible. Los Estados de descarga se conservan incluso cuando se apaga Windows Media Player o Windows XP. |
| en tiempo real  | (Todos los sistemas operativos compatibles). La descarga se produce a la vez. No se conservan los Estados de descarga entre sesiones.                                                                       |



 

## <a name="remarks"></a>Observaciones

Cada tipo de descarga tiene ventajas y desventajas. La descarga en segundo plano permite al usuario continuar con otras tareas e incluso reiniciar Windows sin cancelar la descarga, pero tarda más tiempo en completarse para completar la descarga y solo es compatible con Windows XP. La descarga en tiempo real tarda menos tiempo en completarse, pero requiere que el usuario finalice la descarga antes de cerrar Windows Media Player.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/>                                  |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





