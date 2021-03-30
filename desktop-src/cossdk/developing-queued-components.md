---
description: Desarrollar componentes en cola
ms.assetid: 867b7512-82ad-4877-8675-aa2d7e62ff8a
title: Desarrollar componentes en cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8808ef3e6cba8ff561dd94473fca8f00631081f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807183"
---
# <a name="developing-queued-components"></a>Desarrollar componentes en cola

El servicio de componentes en cola de COM+ requiere que todos los métodos de aplicación solo contengan \[ \] parámetros in, sin valores devueltos. Dado que el objeto de servidor no está necesariamente disponible cuando el cliente realiza la llamada, se pueden devolver resultados del servidor mediante el envío de un mensaje que cree otro objeto. De esta manera, la comunicación bidireccional no se produce en todos los casos, sino solo cuando es necesario, mediante una serie de mensajes unidireccionales entre los objetos.

Para usar el servicio de componentes en cola de COM+, debe tener el servicio de [Message Queue Server](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) ya instalado. Message Queue Server no se instala automáticamente. Message Queue Server debe estar seleccionado durante la instalación del sistema operativo o mediante **Agregar o quitar programas**. Se crea automáticamente un certificado interno de Message Queue Server al iniciar sesión.

Los temas que se describen en la tabla siguiente proporcionan consideraciones adicionales para las situaciones más especializadas.



| Tema                                                                                           | Descripción                                                                                            |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Pasar objetos como parámetros](passing-objects-as-parameters.md)<br/>                   | Describe cómo pasar objetos como \[ parámetros in \] a los componentes en cola.<br/>                    |
| [Limitaciones de seguridad en el modo de grupo de trabajo](security-limitations-in-workgroup-mode.md)<br/> | Describe las limitaciones en el uso de la autenticación de Message Queue Server en el modo de grupo de trabajo.<br/>       |
| [Consideraciones sobre los subprocesos](threading-considerations.md)<br/>                             | Describe problemas específicos relacionados con el paso de punteros de interfaz de la grabadora entre subprocesos.<br/> |
| [Recibir una respuesta](receiving-a-response.md)<br/>                                     | Describe cómo construir una respuesta a una llamada de componente en cola.<br/>                           |



 

 

 




