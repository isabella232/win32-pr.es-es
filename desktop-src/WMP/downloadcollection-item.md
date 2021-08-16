---
title: DownloadCollection.item (método)
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método item recupera un objeto de descarga pendiente.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- item method Reproductor de Windows Media
- item method Reproductor de Windows Media , DownloadCollection (clase)
- DownloadCollection class Reproductor de Windows Media , item method
topic_type:
- apiref
api_name:
- DownloadCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a82a903236038c2f0372786137eec48ad5c5f502d7fd614eb8944f3f4684aea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997045"
---
# <a name="downloadcollectionitem-method"></a>DownloadCollection.item (método)

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **método item** recupera un objeto de descarga pendiente.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*itemId* \[ En\]
</dt> <dd>

**Number** (**long**) que especifica el índice del **elemento DownloadItem** que se recuperará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **objeto DownloadItem.**

## <a name="remarks"></a>Comentarios

El *valor itemID* es de base cero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/>                                  |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DownloadCollection (objeto)**](downloadcollection-object.md)
</dt> <dt>

[**DownloadItem (objeto)**](downloaditem-object.md)
</dt> </dl>

 

 





