---
description: Si los datos son coherentes, se sincronizan los datos del servidor y de todos los clientes. Un tipo de sistema de software que proporciona la coherencia de datos es un sistema de control de revisiones (RCS).
ms.assetid: cd33d20e-bf25-4a50-9b20-344495554434
title: Coherencia de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f300296ff0fdc807beb95e2c03662814957bedb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912317"
---
# <a name="data-coherency"></a>Coherencia de datos

Los datos *coherentes* son los datos que son iguales en la red. En otras palabras, si los datos son coherentes, se sincronizan los datos del servidor y de todos los clientes. Un tipo de sistema de software que proporciona la coherencia de datos es un sistema de control de revisiones (RCS). Este sistema suele ser bastante sencillo, con un solo usuario con permiso para modificar un archivo especificado a la vez. Otros usuarios pueden leer el archivo pero no cambiarlo.

Se dice que el usuario que puede cambiar un archivo ha desprotegido. A continuación, el usuario protege el archivo modificado para que otros usuarios puedan ver los cambios. Solo después de que el usuario haya desprotegido un archivo en, el otro usuario puede desprotegerlo.

Un RCS requiere la intervención activa de los usuarios para que funcione de forma útil. Un sistema de archivos que funciona a través de una red debe controlar el problema automáticamente.

Proporcionar almacenamiento en caché local de datos coherentes es bastante sencillo cuando tiene un subproceso en un cliente que tiene acceso a un archivo a través de la red a la vez. Sin embargo, en la mayoría de los casos, muchos subprocesos diferentes en uno o varios equipos pueden estar leyendo el mismo archivo. Esta situación sigue siendo bastante sencilla. Dado que los datos del archivo son estáticos, cada equipo cliente puede tener su propia copia local sin implicaciones en la coherencia de los datos.

Una situación más común es un subproceso que modifica el archivo y muchos otros subprocesos lo leen. El momento en que se produce una operación de escritura, todas las memorias caché locales de ese archivo están obsoletas. El servidor debe notificar a cada cliente que abandone su memoria caché. Todas las operaciones de lectura posteriores del archivo deben realizarse a través de la red.

En otra situación común, es posible que varios subprocesos de uno o más clientes de red intenten escribir en el mismo archivo. Esta situación es similar a aquella en la que varios usuarios de RCS quieren realizar cambios en el mismo archivo. Cada usuario en secuencia debe desproteger el archivo, realizar cambios y, a continuación, volver a proteger el archivo. Del mismo modo, en un esquema de almacenamiento en caché local, el servidor debe entregar el privilegio de escribir en un archivo en un subproceso de cliente cada vez.

 

 



