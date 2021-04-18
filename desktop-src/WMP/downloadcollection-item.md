---
title: DownloadCollection. Item (método)
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método Item recupera un objeto de descarga pendiente.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- método de elemento Media Player de Windows
- método de elemento Windows Media Player, clase DownloadCollection
- Clase DownloadCollection Windows Media Player, método Item
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
ms.openlocfilehash: d57db60a776c71d9ff16eceb1584c79a125bbf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700086"
---
# <a name="downloadcollectionitem-method"></a>DownloadCollection. Item (método)

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El método **Item** recupera un objeto de descarga pendiente.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Itemid* \[ de\]
</dt> <dd>

**Número** (**largo**) que especifica el índice del **DownloadItem** que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **DownloadItem** .

## <a name="remarks"></a>Observaciones

El valor de *itemID* está basado en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/>                                  |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DownloadCollection**](downloadcollection-object.md)
</dt> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





