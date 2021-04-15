---
title: Evento Player. buffering
description: El evento de almacenamiento en búfer se produce cuando el control de Media Player de Windows comienza o finaliza la descarga o el almacenamiento en búfer. | Evento Player. buffering
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Almacenar en búfer ventanas de eventos Media Player
- Almacenar en búfer ventanas de eventos Media Player, clase Player
- Clase de reproductor Windows Media Player, evento de almacenamiento en búfer
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708764"
---
# <a name="playerbuffering-event"></a>Evento Player. buffering

El evento de **almacenamiento en búfer** se produce cuando el control de Media Player de Windows comienza o finaliza la descarga o el almacenamiento en búfer.

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

**Valor booleano** que contiene uno de los valores siguientes.



| Value | Descripción            |
|-------|------------------------|
| true  | El almacenamiento en búfer se ha iniciado. |
| false | El almacenamiento en búfer ha finalizado.   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Utilice este evento para determinar cuándo se inicia o se detiene el almacenamiento en búfer o la descarga. Puede usar el mismo bloque de eventos para ambos casos y probar la *red*. **bufferingProgress** y *red*. **downloadProgress** para determinar si Windows Media Player está almacenando en búfer o descargando contenido actualmente.

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Network. bufferingProgress**](network-bufferingprogress.md)
</dt> <dt>

[**Network. downloadProgress**](network-downloadprogress.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





