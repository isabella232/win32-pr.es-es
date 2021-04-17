---
description: Limitaciones del programa de ejemplo
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: Limitaciones del programa de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1fde65fa1870ac3ed118bd7c9f95c6add5192f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668031"
---
# <a name="example-program-limitations"></a>Limitaciones del programa de ejemplo

Los principios de una buena práctica de programación no se siguen siempre en estos programas de ejemplo para proporcionar código más conciso y más legible. En concreto:

-   Solo se muestran las respuestas de error limitadas. Los programas de trabajo siempre deben comprobar los códigos de error devueltos y realizar las acciones adecuadas cuando se produce un error.
-   Solo se lleva a cabo la administración de memoria y recursos limitados. En los programas de trabajo, todas las claves y los [*valores hash*](../secgloss/h-gly.md) deben destruirse, se debe liberar toda la memoria asignada, se deben cerrar todos los archivos y se deben liberar todos los identificadores. Estos programas de ejemplo solo proporcionan demostraciones limitadas del uso de funciones que realizan estas tareas. Estos programas de ejemplo no realizan ninguna tarea de administración de recursos ni memoria en el caso de la finalización del programa debido a errores.

 

 
