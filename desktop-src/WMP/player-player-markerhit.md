---
title: Evento Player.MarkerHit
description: El evento MarkerHit tiene lugar cuando se alcanza un marcador. | Evento Player.MarkerHit
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- Evento MarkerHit Reproductor de Windows Media
- Evento MarkerHit Reproductor de Windows Media , clase Player
- Player class Reproductor de Windows Media , MarkerHit event
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070983"
---
# <a name="playermarkerhit-event"></a>Evento Player.MarkerHit

El **evento MarkerHit** tiene lugar cuando se alcanza un marcador.

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

**Number** (**long**) que indica el número del marcador al que se ha alcanzado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede acceder a un método o pasarlo a un método en un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la mayúscula.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





