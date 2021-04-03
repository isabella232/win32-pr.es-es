---
title: Usar IMAPi
description: En los temas siguientes se muestra el uso de la API de maestro de imágenes.
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccd44d01e925d07d251e93a29c5268cc7e9c5076
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903876"
---
# <a name="using-imapi"></a>Usar IMAPi

En los temas siguientes se muestra el uso de la API de maestro de imágenes.

## <a name="usage-scenarios"></a>Escenarios de uso

La siguiente documentación proporciona instrucciones detalladas para escenarios comunes de IMAPi.



| Escenario                                                                                                         | Descripción                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comprobando la compatibilidad con la unidad](checking-drive-support.md)                                                             | Muestra la detección de la compatibilidad de una unidad de medios.<br/>                                                                                                   |
| [Comprobando la compatibilidad con medios](checking-media-support.md)                                                             | Muestra la detección de compatibilidad con los medios.<br/>                                                                                                           |
| [Grabación de una imagen de disco](burning-a-disc.md)                                                                       | Muestra la maestra (grabación de un disco) mediante IMAPi.<br/>                                                                                                       |
| [Agregar una imagen de arranque](adding-a-boot-image.md)                                                                   | Se basa en el ejemplo de [grabación de una imagen de disco](burning-a-disc.md) mediante la adición de código para incluir una imagen de arranque en la sección de arranque del disco.<br/>               |
| [Creación de un disco de múltiples sesiones](creating-a-multisession-disc.md)                                                 | Muestra la creación de un disco de múltiples sesiones mediante IMAPi.<br/>                                                                                              |
| [Supervisar el progreso con eventos](monitoring-progress-with-events.md)                                           | Muestra el uso de interfaces específicas para permitir la implementación de un controlador de eventos para que se pueda recibir información de progreso. <br/>        |
| [Evitar el cierre de sesión o la suspensión durante una grabación](preventing-logoff-or-suspend-during-a-burn.md)                     | Contiene información que detalla las consideraciones de desarrollo de aplicaciones que se deben realizar en lo que respecta a los escenarios que implican el usuario ' Logoff ' y ' Suspend ' en Windows.<br/> |
| [Proporcionar permisos de usuario para dispositivos de grabación de multimedia](providing-user-permissions-for-media-burning-devices.md) | Detalla el proceso necesario para asegurarse de que un usuario tiene los permisos adecuados para el uso de dispositivos de grabación multimedia en Windows XP y Windows Server 2003.<br/>             |



 

## <a name="application-compatibility"></a>Compatibilidad de aplicaciones

La siguiente documentación contiene información importante que se debe tener en cuenta al desarrollar una aplicación que use IMAPi.



| Instrucciones                                                   | Descripción                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Distribución de la multisesión de IMAPi](imapi-multisession-layout.md) | Detalla el diseño del disco que IMAPi emplea para implementar la multisesión. Esta información se utiliza para garantizar la interoperabilidad entre IMAPi y otro software de grabación, además de permitir la creación de imágenes de disco multisesión compatibles con IMAPi.<br/> |



 

 

 





