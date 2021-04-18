---
title: DownloadCollection. removeItem (método)
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método removeItem quita un elemento de descarga de una colección de descargas.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- método removeItem Media Player Windows
- método removeItem Windows Media Player, clase DownloadCollection
- Clase DownloadCollection Windows Media Player, método removeItem
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
ms.openlocfilehash: a1798665b79327b7956c1b78509b55cc6e6dd70c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700348"
---
# <a name="downloadcollectionremoveitem-method"></a>DownloadCollection. removeItem (método)

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El método **RemoveItem** quita un elemento de descarga de una colección de descargas.

## <a name="syntax"></a>Sintaxis


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*itemID* \[ de\]
</dt> <dd>

**Número** (**largo**) que especifica el índice del **DownloadItem** que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la descarga representada por *itemID* está en curso, este método cancela la descarga.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/>                                  |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DownloadCollection. Item**](downloadcollection-item.md)
</dt> <dt>

[**Objeto DownloadCollection**](downloadcollection-object.md)
</dt> </dl>

 

 





