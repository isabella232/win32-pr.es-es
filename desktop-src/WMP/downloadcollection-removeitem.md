---
title: Método DownloadCollection.removeItem
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método removeItem quita un elemento de descarga de una colección de descarga.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- Método removeItem Reproductor de Windows Media
- Método removeItem Reproductor de Windows Media , clase DownloadCollection
- Clase DownloadCollection Reproductor de Windows Media método , removeItem
topic_type:
- apiref
api_name:
- DownloadCollection.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d7eaa7b26a4d64070cae426d1bbc23418593fa8ec5472e870ed7529ce8a122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997075"
---
# <a name="downloadcollectionremoveitem-method"></a>Método DownloadCollection.removeItem

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **método removeItem** quita un elemento de descarga de una colección de descarga.

## <a name="syntax"></a>Sintaxis


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*itemID* \[ En\]
</dt> <dd>

**Number** (**long**) que especifica el índice del **elemento DownloadItem** que se quitará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si la descarga representada por *itemID* está en curso, este método cancela la descarga.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/>                                  |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DownloadCollection.item**](downloadcollection-item.md)
</dt> <dt>

[**DownloadCollection (objeto)**](downloadcollection-object.md)
</dt> </dl>

 

 





