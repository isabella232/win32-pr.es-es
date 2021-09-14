---
description: La clase CMsgThread proporciona compatibilidad con un subproceso de trabajo en el que las solicitudes se pueden publicar de forma asincrónica en lugar de enviarse directamente.
ms.assetid: 1cf159c9-80d0-4e3b-88d8-2ba4cd18e768
title: CMsg (clase)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361371"
---
# <a name="cmsg-class"></a>CMsg (clase)

La [**clase CMsgThread**](cmsgthread.md) proporciona compatibilidad con un subproceso de trabajo en el que las solicitudes se pueden publicar de forma asincrónica en lugar de enviarse directamente. La [**clase CAMThread**](camthread.md) proporciona un subproceso de trabajo al que se pueden enviar solicitudes únicas. Solo un cliente puede realizar una solicitud a la vez y el cliente se bloquea hasta que el subproceso de trabajo ha completado la solicitud. Por el contrario, la **clase CMsgThread** proporciona un subproceso de trabajo en el que se puede publicar cualquier número de solicitudes. Las solicitudes (en forma de objeto) se ponen en cola y `CMsg` se ejecutan en orden de forma asincrónica. No se recibe ningún valor devuelto o de respuesta.



| Miembros de datos              | Descripción                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dwFlags                   | Marca el parámetro en el código de solicitud.                                                                                                                                               |
| lpParam                   | Datos requeridos por el subproceso de trabajo como parámetros o valores devueltos. Estos datos no deben basarse en la pila, ya que se hará referencia a estos algún tiempo después de completar la operación de cola. |
| pEvent                    | Objeto de evento que un subproceso de trabajo puede señalar para indicar la finalización de la operación.                                                                                         |
| uMsg                      | Solicite código definido por el cliente de la clase de subproceso y comprendido por la función de subproceso de trabajo invalidada.                                                           |
| Funciones de miembro          | Descripción                                                                                                                                                                       |
| [**CMsg**](cmsg-cmsg.md) | Construye un [**objeto CMsg.**](cmsg-cmsg.md)                                                                                                                                    |



 

 

 



