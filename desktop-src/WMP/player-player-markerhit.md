---
title: Evento Player. MarkerHit
description: El evento MarkerHit se produce cuando se alcanza un marcador. | Evento Player. MarkerHit
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- Media Player MarkerHit de eventos de Windows
- Evento MarkerHit de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento MarkerHit
topic_type:
- apiref
api_name:
- Player.MarkerHit
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce6b9ca7c103e9a9e9151a7ff0467a59786b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690184"
---
# <a name="playermarkerhit-event"></a>Evento Player. MarkerHit

El evento **MarkerHit** se produce cuando se alcanza un marcador.

## <a name="syntax"></a>Sintaxis


```JScript
Player.MarkerHit(
  MarkerNum
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MarkerNum* 
</dt> <dd>

**Número** (**largo**) que indica el número del marcador que se alcanzó.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





