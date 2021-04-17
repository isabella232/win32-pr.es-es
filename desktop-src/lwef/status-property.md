---
title: Propiedad status
description: Propiedad status
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402e88185e1024aa5958d06936a6529ae4012622
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704695"
---
# <a name="status-property"></a>Propiedad status

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve el estado del canal de salida de audio.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente * * *. Estado de AudioOutput.**



| Value | Descripción                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| 0     | El canal de salida de audio está disponible (no está ocupado).                                                                 |
| 1     | No se admite la salida de audio; por ejemplo, dado que no hay ninguna tarjeta de sonido.                                |
| 2     | No se puede abrir el canal de salida de audio (está ocupado). por ejemplo, como otra aplicación está reproduciendo audio. |
| 3     | El canal de salida de audio está ocupado porque el servidor está procesando la entrada de voz de usuario.                              |
| 4     | El canal de salida de audio está ocupado porque un carácter está hablando actualmente.                                       |
| 5     | El canal de salida de audio no está ocupado, pero está esperando la entrada de voz de usuario.                                    |
| 6     | Hubo otro problema (desconocido) al intentar acceder al canal de salida de audio.                          |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta configuración permite a la aplicación cliente consultar el canal de salida de audio y devolver un valor entero que indica el estado del canal de salida de audio. Puede utilizar esta opción para determinar si es adecuado que el carácter hable o si es adecuado intentar activar el modo de escucha (mediante el método de [**escucha**](listen-method.md) ).

## <a name="see-also"></a>Consulte también

[**Evento ListenComplete**](listencomplete-event.md)


 

 




