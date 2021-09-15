---
title: Evento Player.Buffering
description: El evento de almacenamiento en búfer tiene lugar cuando el control Reproductor de Windows Media inicia o finaliza el almacenamiento en búfer o la descarga. | Evento Player.Buffering
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Almacenamiento en búfer de eventos Reproductor de Windows Media
- Almacenamiento en búfer de eventos Reproductor de Windows Media , clase Player
- Player class Reproductor de Windows Media , Buffering event
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
ms.openlocfilehash: 3a73ac77f9b8e81162a6cc0f9220562caba26eae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359271"
---
# <a name="playerbuffering-event"></a>Evento Player.Buffering

El **evento de almacenamiento** en búfer tiene lugar cuando el control Reproductor de Windows Media inicia o finaliza el almacenamiento en búfer o la descarga.

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

## <a name="remarks"></a>Observaciones

Use este evento para determinar cuándo se inicia o se detiene el almacenamiento en búfer o la descarga. Puede usar el mismo bloque de eventos para ambos casos y probar *red*. **bufferingProgress** y *Network*. **downloadProgress para** determinar si Reproductor de Windows Media almacena en búfer o descarga contenido.

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede acceder a un método o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la mayúscula.

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

 

 





