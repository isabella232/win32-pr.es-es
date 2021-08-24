---
description: La infraestructura del mismo nivel no garantiza el orden de recepción y procesamiento de registros.
ms.assetid: 840aa931-c54c-463d-b37b-7d01c8a44409
title: Dependencias de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8121c22525a3a2d8065014eaf27143a324b2f6410f194d3257ec3b840958d5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675025"
---
# <a name="record-dependencies"></a>Dependencias de registro

La infraestructura del mismo nivel no garantiza el orden de recepción y procesamiento de registros. Si la aplicación tiene dependencias de registro, lo que significa que el procesamiento o validación de un registro se basa en otro registro, la aplicación debe ser capaz de controlar situaciones en las que los registros se puedan recibir en un orden arbitrario e imprevisible. Por ejemplo, una aplicación de chat puede tener dos tipos de registros: un registro que contiene información sobre un usuario específico y un registro que contiene un mensaje de chat que hace referencia al registro de usuario.

Una aplicación debe ser capaz de controlar la situación cuando se recibe un registro de mensaje de chat antes del registro de usuario para el mensaje de chat. Una manera de controlar la situación es esperar el registro de usuario mediante una lista **de** espera o una caché y un temporizador. La aplicación puede examinar periódicamente cada registro de la lista o caché y, a continuación, controlar la situación cuando se recibe el registro de usuario necesario.

Para controlar las dependencias de registros, una aplicación bien diseñada consta de lo siguiente:

-   Comprueba siempre las dependencias de registros antes de realizar una acción.
-   Prevé las condiciones que pueden producirse cuando los registros se reciben en un orden inesperado y, a continuación, controla la situación.

 

 



