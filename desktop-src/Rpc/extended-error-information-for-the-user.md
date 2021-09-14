---
title: Información de error extendida para el usuario
description: Si hay información de error extendida disponible, los componentes que participan en la creación de la información de error extendida deben facilitar la tarea de encontrar el problema.
ms.assetid: 10c54f53-f449-4e7d-ba84-7b000beaee22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f52e45e3f181c5aaa0db196f9ce791581cc38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361957"
---
# <a name="extended-error-information-for-the-user"></a>Información de error extendida para el usuario

Si hay información de error extendida disponible, los componentes que participan en la creación de la información de error extendida deben facilitar la tarea de encontrar el problema. El primer paso consiste en revisar el último registro de errores extendido y determinar en qué equipo y qué proceso se originó el problema. Esta suele ser la causa del error de RPC \_ \_ \* S. Busque la ubicación de detección y determine qué significan los parámetros de esta ubicación de detección. Normalmente indican un error de una llamada de función o una comprobación determinada. A partir de ahí, determine por qué se produce un error en la función o la comprobación y tome medidas correctivas.

Los registros anteriores al último registro indican la ruta de acceso por la que llegó el error y, por lo general, sirven como una comprobación de estado en lugar de un asistente en el proceso de solución de problemas.

 

 




