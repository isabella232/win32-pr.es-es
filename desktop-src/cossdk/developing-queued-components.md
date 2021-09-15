---
description: Desarrollo de componentes en cola
ms.assetid: 867b7512-82ad-4877-8675-aa2d7e62ff8a
title: Desarrollo de componentes en cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8808ef3e6cba8ff561dd94473fca8f00631081f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568493"
---
# <a name="developing-queued-components"></a>Desarrollo de componentes en cola

El servicio de componentes en cola de COM+ requiere que todos los métodos de aplicación solo contengan \[ \] parámetros, sin valores devueltos. Dado que el objeto de servidor no está necesariamente disponible cuando el cliente realiza la llamada, los resultados del servidor se pueden devolver mediante el envío de un mensaje que crea otro objeto. De este modo, la comunicación bidireccional no se produce en todos los casos, sino solo cuando es necesaria, por una serie de mensajes un solo sentido entre objetos.

Para usar el servicio de componentes en cola de COM+, debe tener el [servicio Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) ya instalado. Message Queuing no se instala automáticamente. Message Queuing debe seleccionarse durante la instalación del sistema operativo o mediante **Agregar o quitar programas**. Un certificado interno de Message Queuing se crea automáticamente al iniciar sesión.

Los temas descritos en la tabla siguiente proporcionan consideraciones adicionales para situaciones más especializadas.



| Tema                                                                                           | Descripción                                                                                            |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Pasar objetos como parámetros](passing-objects-as-parameters.md)<br/>                   | Describe cómo pasar objetos como en \[ parámetros a componentes en \] cola.<br/>                    |
| [Limitaciones de seguridad en el modo de grupo de trabajo](security-limitations-in-workgroup-mode.md)<br/> | Describe las limitaciones sobre el uso de la autenticación de Message Queuing en modo de grupo de trabajo.<br/>       |
| [Consideraciones sobre los subprocesos](threading-considerations.md)<br/>                             | Describe cuestiones específicas relacionadas con el paso de punteros de interfaz de grabadora entre subprocesos.<br/> |
| [Recibir una respuesta](receiving-a-response.md)<br/>                                     | Describe cómo construir una respuesta a una llamada de componente en cola.<br/>                           |



 

 

 




