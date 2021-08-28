---
title: DownloadManager.getDownloadCollection (método)
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método getDownloadCollection recupera la colección de descarga especificada.
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- Método getDownloadCollection Reproductor de Windows Media
- Método getDownloadCollection Reproductor de Windows Media , clase DownloadManager
- DownloadManager class Reproductor de Windows Media , getDownloadCollection (método)
topic_type:
- apiref
api_name:
- DownloadManager.getDownloadCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57fc729296f15b39e603683cab38e3d0d878733ab0990d9876e32b4001a15cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749625"
---
# <a name="downloadmanagergetdownloadcollection-method"></a>DownloadManager.getDownloadCollection (método)

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **método getDownloadCollection** recupera la colección de descarga especificada.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*collectionId* \[ En\]
</dt> <dd>

**Número** (**long**) que especifica el identificador de la colección de descarga que se recuperará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **objeto DownloadCollection.**

## <a name="remarks"></a>Comentarios

Primero debe llamar a *DownloadManager.* **createDownloadCollection** para crear una nueva colección y recuperar su valor de identificador.

Una colección de descarga existente puede contener elementos que se han marcado como cancelados.

Los elementos de descarga en tiempo real no completados en una sesión anterior no se recuperan como parte de la colección. Las descargas en segundo plano que se completaron antes de la sesión actual permanecen en la colección de descargas hasta que se quitan.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/>                                  |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DownloadManager (objeto)**](downloadmanager-object.md)
</dt> <dt>

[**DownloadManager. createDownloadCollection**](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[**DownloadCollection (objeto)**](downloadcollection-object.md)
</dt> </dl>

 

 





