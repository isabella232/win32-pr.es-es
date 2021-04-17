---
description: La infraestructura del mismo nivel no garantiza el orden de recepción y procesamiento de registros.
ms.assetid: 840aa931-c54c-463d-b37b-7d01c8a44409
title: Dependencias de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7cce0803ad25f4a67908256ad78c7abe4b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667384"
---
# <a name="record-dependencies"></a>Dependencias de registro

La infraestructura del mismo nivel no garantiza el orden de recepción y procesamiento de registros. Si la aplicación tiene dependencias de registros, lo que significa que el procesamiento o la validación de un registro se basa en otro registro, la aplicación debe ser capaz de controlar las situaciones en las que los registros se pueden recibir en un orden arbitrario e impredecible. Por ejemplo, una aplicación de chat puede tener dos tipos de registros: un registro que contiene información acerca de un usuario específico y un registro que contiene un mensaje de chat que hace referencia al registro del usuario.

Una aplicación debe ser capaz de controlar la situación cuando se recibe un registro de mensaje de chat antes del registro del usuario para el mensaje de chat. Una manera de controlar la situación es esperar el registro de usuario mediante una lista en **espera**, o una caché y un temporizador. La aplicación puede examinar periódicamente cada registro de la lista o la memoria caché y, a continuación, controlar la situación en que se recibe el registro de usuario necesario.

Para controlar las dependencias de registro, una aplicación bien diseñada consta de lo siguiente:

-   Comprueba siempre las dependencias del registro antes de realizar una acción.
-   Prevé las condiciones que pueden producirse cuando los registros se reciben en un orden inesperado y, a continuación, controla la situación.

 

 



