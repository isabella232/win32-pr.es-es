---
description: Limitaciones del programa de ejemplo
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: Limitaciones del programa de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0244f373264ed6886632979f00ace873949c1ab7e781262b4ef30dab2072f8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007443"
---
# <a name="example-program-limitations"></a>Limitaciones del programa de ejemplo

Los principios de una buena práctica de programación no siempre se siguen en estos programas de ejemplo para proporcionar código más conciso y legible. En concreto:

-   Solo se muestran respuestas de error limitadas. Los programas de trabajo siempre deben comprobar los códigos de error devueltos y realizar las acciones adecuadas cuando se encuentra un error.
-   Solo se realiza la administración limitada de recursos y memoria. En los programas de trabajo, se deben destruir todas las claves y [*hashes,*](../secgloss/h-gly.md) liberar toda la memoria asignada, cerrar todos los archivos y liberar todos los identificadores. Estos programas de ejemplo proporcionan solo demostraciones limitadas del uso de funciones que realizan estas tareas. Estos programas de ejemplo no realizan tareas de administración de recursos o memoria en caso de finalización del programa debido a errores.

 

 
