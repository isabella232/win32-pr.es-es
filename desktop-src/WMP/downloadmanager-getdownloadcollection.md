---
title: DownloadManager. getDownloadCollection, método
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método getDownloadCollection recupera la colección de descarga especificada.
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- método getDownloadCollection de Windows Media Player
- método getDownloadCollection de Windows Media Player, clase DownloadManager
- Clase DownloadManager Windows Media Player, método getDownloadCollection
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
ms.openlocfilehash: 2e879d82c3f49db08d75b8aec37271e8d966019e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699417"
---
# <a name="downloadmanagergetdownloadcollection-method"></a>DownloadManager. getDownloadCollection, método

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El método **getDownloadCollection** recupera la colección de descarga especificada.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*collectionId* \[ de\]
</dt> <dd>

**Número** (**largo**) que especifica el identificador de la colección de descarga que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **DownloadCollection** .

## <a name="remarks"></a>Observaciones

Primero debe llamar a *Downloadmanager*. **createDownloadCollection** para crear una nueva colección y recuperar su valor de identificador.

Una colección de descargas existente puede contener elementos marcados como cancelados.

Los elementos de descarga en tiempo real no completados en una sesión anterior no se recuperan como parte de la colección. Las descargas en segundo plano que se completaron antes de la sesión actual permanecen en la colección de descargas hasta que se quitan.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/>                                  |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DownloadManager**](downloadmanager-object.md)
</dt> <dt>

[**DownloadManager. createDownloadCollection**](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[**Objeto DownloadCollection**](downloadcollection-object.md)
</dt> </dl>

 

 





