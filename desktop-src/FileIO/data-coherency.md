---
description: Si los datos son coherentes, los datos del servidor y todos los clientes se sincronizan. Un tipo de sistema de software que proporciona coherencia de datos es un sistema de control de revisiones (RCS).
ms.assetid: cd33d20e-bf25-4a50-9b20-344495554434
title: Coherencia de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b0877ffb9470385111c60729c96597d38852ad37220c09f6c27e6977e0e97c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150851"
---
# <a name="data-coherency"></a>Coherencia de datos

Los datos *coherentes* son los mismos en toda la red. En otras palabras, si los datos son coherentes, los datos del servidor y todos los clientes se sincronizan. Un tipo de sistema de software que proporciona coherencia de datos es un sistema de control de revisiones (RCS). Este tipo de sistema suele ser bastante sencillo, y solo un usuario puede modificar un archivo especificado a la vez. Otros usuarios pueden leer el archivo, pero no pueden cambiarlo.

Se dice que el usuario que puede cambiar un archivo lo ha desprotegido. A continuación, el usuario comprueba el archivo modificado para que otros usuarios puedan ver los cambios. Solo después de que el usuario haya vuelto a comprobar un archivo, puede que otro usuario lo desprotega.

Una RCS requiere la intervención activa de los usuarios para funcionar de una manera útil. Un sistema de archivos que opera a través de una red debe controlar el problema automáticamente.

Proporcionar almacenamiento en caché local de datos coherentes es bastante sencillo cuando se tiene un subproceso en un cliente que accede a un archivo a través de la red a la vez. Sin embargo, en la mayoría de los casos, muchos subprocesos diferentes en uno o varios equipos pueden estar leyendo el mismo archivo. Esta situación sigue siendo bastante sencilla. Dado que los datos del archivo son estáticos, cada equipo cliente puede tener su propia copia local sin implicaciones para la coherencia de datos.

Una situación más común es que un subproceso modifica el archivo y muchos otros subprocesos lo leen. En el momento en que se produce una operación de escritura, todas las memorias caché locales de ese archivo están obsoletas. El servidor debe notificar a cada cliente que abandone su caché. Las operaciones de lectura posteriores para el archivo deben realizarse a través de la red.

En otra situación común, varios subprocesos en uno o varios clientes de red podrían intentar escribir en el mismo archivo. Esta situación es similar a una en la que varios usuarios RCS desean realizar cambios en el mismo archivo. Cada usuario en secuencia debe revisar el archivo, realizar cambios y, a continuación, volver a comprobarlo. De forma similar, en un esquema de almacenamiento en caché local, el servidor debe entregar el privilegio de escribir en un archivo en un subproceso de cliente a la vez.

 

 



