---
title: Evento Player. CdromMediaChange
description: El evento CdromMediaChange se produce cuando se inserta o se expulsa un CD o DVD en una unidad de CD o DVD. | Evento Player. CdromMediaChange
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- Media Player CdromMediaChange de eventos de Windows
- Evento CdromMediaChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento CdromMediaChange
topic_type:
- apiref
api_name:
- Player.CdromMediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c3125235d5f8d19963b85284e7dbe40c7af408d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708763"
---
# <a name="playercdrommediachange-event"></a>Evento Player. CdromMediaChange

El evento **CdromMediaChange** se produce cuando se inserta o se expulsa un CD o DVD en una unidad de CD o DVD.

## <a name="syntax"></a>Sintaxis


```JScript
Player.CdromMediaChange(
  CdromNum
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CdromNum* 
</dt> <dd>

**Número** (**largo**) que especifica el índice de la unidad de CD o DVD.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El índice de la unidad de CD corresponde al índice de un objeto **CDROM** en **CdromCollection**.

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

**Windows Media Player 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDROM (objeto)**](cdrom-object.md)
</dt> <dt>

[**Objeto CdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





