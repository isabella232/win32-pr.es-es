---
title: Propiedad Status
description: Propiedad Status
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402e88185e1024aa5958d06936a6529ae4012622
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467220"
---
# <a name="status-property"></a>Propiedad Status

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve el estado del canal de salida de audio.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent!". AudioOutput.Status**



| Value | Descripción                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| 0     | El canal de salida de audio está disponible (no está ocupado).                                                                 |
| 1     | No hay compatibilidad con la salida de audio; por ejemplo, porque no hay ninguna tarjeta de sonido.                                |
| 2     | No se puede abrir el canal de salida de audio (está ocupado); por ejemplo, porque otra aplicación reproduce audio. |
| 3     | El canal de salida de audio está ocupado porque el servidor está procesando la entrada de voz del usuario.                              |
| 4     | El canal de salida de audio está ocupado porque un carácter está hablando actualmente.                                       |
| 5     | El canal de salida de audio no está ocupado, pero está esperando la entrada de voz del usuario.                                    |
| 6     | Hubo algún otro problema (desconocido) al intentar acceder al canal de salida de audio.                          |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta configuración permite a la aplicación cliente consultar el canal de salida de audio y devolver un valor entero que indica el estado del canal de salida de audio. Puede usar esto para determinar si es adecuado que el carácter diga o si es adecuado intentar activar el modo de escucha (mediante el [**método Listen).**](listen-method.md)

## <a name="see-also"></a>Consulte también

[**Evento ListenComplete**](listencomplete-event.md)


 

 




