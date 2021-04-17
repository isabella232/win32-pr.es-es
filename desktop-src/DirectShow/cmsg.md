---
description: La clase CMsgThread proporciona compatibilidad con un subproceso de trabajo al que se pueden publicar solicitudes de forma asincrónica en lugar de enviarse directamente.
ms.assetid: 1cf159c9-80d0-4e3b-88d8-2ba4cd18e768
title: Clase CMsg
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg
api_type:
- COM
api_location: ''
ms.openlocfilehash: a57a841b9c36a21895099c931acbf18a1e01ea0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666123"
---
# <a name="cmsg-class"></a>Clase CMsg

La clase [**CMsgThread**](cmsgthread.md) proporciona compatibilidad con un subproceso de trabajo al que se pueden publicar solicitudes de forma asincrónica en lugar de enviarse directamente. La clase [**CAMThread**](camthread.md) proporciona un subproceso de trabajo al que se pueden enviar solicitudes individuales. Solo un cliente puede realizar una solicitud a la vez y el cliente se bloquea hasta que el subproceso de trabajo haya completado la solicitud. Por el contrario, la clase **CMsgThread** proporciona un subproceso de trabajo en el que se puede publicar cualquier número de solicitudes. Las solicitudes (en forma de `CMsg` objeto) se ponen en cola y se ejecutan en orden, de forma asincrónica. No se recibe ninguna respuesta o valor devuelto.



| Miembros de datos              | Descripción                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dwFlags                   | Parámetro de marca para el código de solicitud.                                                                                                                                               |
| lpParam                   | Datos requeridos por el subproceso de trabajo como parámetros o valores devueltos. Estos datos no deberían estar basados en la pila, ya que se hará referencia a él después de completar la operación de puesta en cola. |
| As                    | Objeto de evento que un subproceso de trabajo puede señalar para indicar la finalización de la operación.                                                                                         |
| uMsg                      | Código de solicitud definido por el cliente de la clase de subproceso y comprensible por la función de subproceso de trabajo invalidada.                                                           |
| Funciones de miembro          | Descripción                                                                                                                                                                       |
| [**CMsg**](cmsg-cmsg.md) | Construye un objeto [**CMsg**](cmsg-cmsg.md) .                                                                                                                                    |



 

 

 



