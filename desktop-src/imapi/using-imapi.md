---
title: Uso de IMAPI
description: En los temas siguientes se muestra el uso de image mastering API.
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7bf19d619f6ed5ab9a2d6b0deb1ca6a42b71a0b0941a96f54cccfa87c14b5f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092435"
---
# <a name="using-imapi"></a>Uso de IMAPI

En los temas siguientes se muestra el uso de image mastering API.

## <a name="usage-scenarios"></a>Escenarios de uso

En la documentación siguiente se proporcionan instrucciones detalladas para escenarios comunes de IMAPI.



| Escenario                                                                                                         | Descripción                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comprobación de la compatibilidad con unidades](checking-drive-support.md)                                                             | Muestra la detección de compatibilidad con una unidad multimedia.<br/>                                                                                                   |
| [Comprobación de la compatibilidad con medios](checking-media-support.md)                                                             | Muestra la detección de compatibilidad con medios.<br/>                                                                                                           |
| [Grabar una imagen de disco](burning-a-disc.md)                                                                       | Muestra la masteración (grabar un disco) mediante IMAPI.<br/>                                                                                                       |
| [Agregar una imagen de arranque](adding-a-boot-image.md)                                                                   | Se basa en el ejemplo [de grabación](burning-a-disc.md) de una imagen de disco agregando código para incluir una imagen de arranque en la sección de arranque del disco.<br/>               |
| [Creación de un disco multisesión](creating-a-multisession-disc.md)                                                 | Muestra la creación de un disco multisesión mediante IMAPI.<br/>                                                                                              |
| [Supervisión del progreso con eventos](monitoring-progress-with-events.md)                                           | Muestra el uso de interfaces específicas para permitir la implementación de un controlador de eventos para que se pueda recibir información de progreso. <br/>        |
| [Evitar el cierre de sesión o suspender durante una grabación](preventing-logoff-or-suspend-during-a-burn.md)                     | Contiene información que detalla las consideraciones de desarrollo de aplicaciones que se deben tener en cuenta en los escenarios que implican al usuario "Logoff" y "Suspend" en Windows.<br/> |
| [Proporcionar permisos de usuario para dispositivos de protección de medios](providing-user-permissions-for-media-burning-devices.md) | Detalla el proceso necesario para asegurarse de que un usuario tiene los permisos adecuados para utilizar dispositivos de grabación multimedia en Windows XP y Windows Server 2003.<br/>             |



 

## <a name="application-compatibility"></a>Compatibilidad de aplicaciones

La siguiente documentación contiene información importante que se debe tener en cuenta al desarrollar una aplicación que usa IMAPI.



| Instrucciones                                                   | Descripción                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Diseño de varias sesiones de IMAPI](imapi-multisession-layout.md) | Detalla el diseño de disco que USA IMAPI para implementar varias sesiones. Esta información se usa para garantizar la interoperabilidad entre IMAPI y otro software de grabación, así como para permitir la creación de imágenes de disco multisesión compatibles con IMAPI.<br/> |



 

 

 





