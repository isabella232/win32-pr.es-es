---
title: DownloadItem.type
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad type recupera el tipo de la descarga.
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- DownloadItem.type Reproductor de Windows Media
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
ms.openlocfilehash: 038f348093a512095ee930c4147024bc789ead5edd3498243eb83a01608bfac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749716"
---
# <a name="downloaditemtype"></a>DownloadItem.type

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La **propiedad type** recupera el tipo de la descarga.

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura** que contiene uno de los valores siguientes.



| Value      | Descripción                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| background | (solo Windows XP). La descarga se produce como un proceso en segundo plano a medida que el tiempo del procesador está disponible. Los estados de descarga persisten incluso cuando Reproductor de Windows Media o Windows xp se apaga. |
| en tiempo real  | (Todos los sistemas operativos compatibles). La descarga se produce a la vez. No se conservan estados de descarga entre sesiones.                                                                       |



 

## <a name="remarks"></a>Comentarios

Cada tipo de descarga tiene ventajas y desventajas. La descarga en segundo plano permite al usuario continuar con otras tareas e incluso reiniciar Windows sin cancelar la descarga, pero tarda más tiempo en completar la descarga y solo es compatible con Windows XP. La descarga en tiempo real tarda menos tiempo en completarse, pero requiere que el usuario finalice todas las descargas antes de Reproductor de Windows Media.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/>                                  |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DownloadItem (objeto)**](downloaditem-object.md)
</dt> </dl>

 

 





