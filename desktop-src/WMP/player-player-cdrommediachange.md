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
ms.openlocfilehash: 3c3125235d5f8d19963b85284e7dbe40c7af408d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359268"
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

## <a name="remarks"></a>Observaciones

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

 

 





