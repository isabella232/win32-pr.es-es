---
title: PlaylistArray. Item (método)
description: El método Item recupera la lista de reproducción en el índice especificado.
ms.assetid: cc851695-f9a2-4594-8bd3-3555c18bfa10
keywords:
- método de elemento Media Player de Windows
- método de elemento Windows Media Player, clase PlaylistArray
- Clase PlaylistArray Windows Media Player, método Item
topic_type:
- apiref
api_name:
- PlaylistArray.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6144f6e1cfda93be32060e8206a96b0da7568d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718890"
---
# <a name="playlistarrayitem-method"></a>PlaylistArray. Item (método)

El método **Item** recupera la lista de reproducción en el índice especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = PlaylistArray.item(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

**Número** (**largo**) que contiene el índice de la lista de reproducción que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto de **lista de reproducción** .

## <a name="remarks"></a>Observaciones

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





