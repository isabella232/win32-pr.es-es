---
description: Limitaciones del programa de ejemplo
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: Limitaciones del programa de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1fde65fa1870ac3ed118bd7c9f95c6add5192f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173218"
---
# <a name="example-program-limitations"></a>Limitaciones del programa de ejemplo

Los principios de una buena práctica de programación no siempre se siguen en estos programas de ejemplo para proporcionar código más conciso y legible. En concreto:

-   Solo se muestran respuestas de error limitadas. Los programas de trabajo siempre deben comprobar los códigos de error devueltos y realizar las acciones adecuadas cuando se encuentra un error.
-   Solo se realiza la administración limitada de recursos y memoria. En los programas de trabajo, se deben destruir todas las claves y [*hashes,*](../secgloss/h-gly.md) liberar toda la memoria asignada, cerrar todos los archivos y liberar todos los identificadores. Estos programas de ejemplo proporcionan solo demostraciones limitadas del uso de funciones que realizan estas tareas. Estos programas de ejemplo no realizan ninguna tarea de administración de recursos o memoria en caso de finalización del programa debido a errores.

 

 
