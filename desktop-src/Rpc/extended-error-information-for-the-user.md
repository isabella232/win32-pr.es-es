---
title: Información de error extendida para el usuario
description: Si hay disponible información de error ampliada, los componentes que participan en la creación de la información de error extendida deben facilitar la búsqueda del problema.
ms.assetid: 10c54f53-f449-4e7d-ba84-7b000beaee22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f52e45e3f181c5aaa0db196f9ce791581cc38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903553"
---
# <a name="extended-error-information-for-the-user"></a>Información de error extendida para el usuario

Si hay disponible información de error ampliada, los componentes que participan en la creación de la información de error extendida deben facilitar la búsqueda del problema. El primer paso es revisar el último registro de error extendido y determinar en qué equipo y qué proceso se originó el problema. Esta suele ser la causa del error de RPC \_ S \_ \* . Busque la ubicación de detección y determine el significado de los parámetros de esta ubicación de detección. Normalmente, indican un error en una llamada de función o en una comprobación determinada. A partir de ahí, determine por qué se produce un error en la función o comprobación y tome medidas correctivas.

Los registros antes del último registro indican la ruta de acceso en la que llegó el error y, por lo general, sirven como comprobación de validez en lugar de una solución alternativa en el proceso de solución de problemas.

 

 




