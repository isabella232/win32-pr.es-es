---
title: Evento Player.CdromMediaChange
description: El evento CdromMediaChange tiene lugar cuando se inserta o expulsa un CD o DVD en una unidad de CD o DVD. | Evento Player.CdromMediaChange
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- CdromMediaChange event Reproductor de Windows Media
- CdromMediaChange event Reproductor de Windows Media , Player (Clase)
- Player class Reproductor de Windows Media , CdromMediaChange event
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
ms.openlocfilehash: ca5e7301c1fb697f4dbbceea2d4dc46af1d884fe4b3e06166b5c24aa43502a73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747391"
---
# <a name="playercdrommediachange-event"></a>Evento Player.CdromMediaChange

El **evento CdromMediaChange** tiene lugar cuando se inserta o expulsa un CD o DVD en una unidad de CD o DVD.

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

**Número** **(long)** que especifica el índice de la unidad de CD o DVD.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

El índice de la unidad de CD corresponde al índice de un objeto **Cdrom** en **CdromCollection**.

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede acceder a un método o pasarlo a un método en un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la mayúscula.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Cdrom (objeto)**](cdrom-object.md)
</dt> <dt>

[**CdromCollection (objeto)**](cdromcollection-object.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





