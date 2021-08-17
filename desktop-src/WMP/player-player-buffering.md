---
title: Evento Player.Buffering
description: El evento de almacenamiento en búfer se produce cuando el control Reproductor de Windows Media o finaliza el almacenamiento en búfer o la descarga. | Evento Player.Buffering
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Almacenamiento en búfer de eventos Reproductor de Windows Media
- Almacenamiento en búfer de eventos Reproductor de Windows Media , clase Player
- Evento player class Reproductor de Windows Media , Buffering
topic_type:
- apiref
api_name:
- Player.Buffering
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ac382315d37fcd36a5470ae3f7f07bf4454687b660a2311498b5b0866e32b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747526"
---
# <a name="playerbuffering-event"></a>Evento Player.Buffering

El **evento de almacenamiento** en búfer se produce cuando el control Reproductor de Windows Media o finaliza el almacenamiento en búfer o la descarga.

## <a name="syntax"></a>Sintaxis


```JScript
Player.Buffering(
  Start
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

**Valor** booleano que contiene uno de los siguientes valores.



| Value | Descripción            |
|-------|------------------------|
| true  | Se ha iniciado el almacenamiento en búfer. |
| false | El almacenamiento en búfer ha finalizado.   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Use este evento para determinar cuándo se inicia o se detiene el almacenamiento en búfer o la descarga. Puede usar el mismo bloque de eventos para ambos casos y probar *Network*. **bufferingProgress** y *Network*. **downloadProgress para** determinar si Reproductor de Windows Media almacena en búfer o descarga contenido.

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede tener acceso a un método de un archivo JScript importado mediante el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Network.bufferingProgress**](network-bufferingprogress.md)
</dt> <dt>

[**Network.downloadProgress**](network-downloadprogress.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





