---
description: Al usar los CSP de proveedores de servicios criptográficos, tenga en cuenta las siguientes convenciones.
ms.assetid: 70053b89-4d39-4a86-985a-0e8f05fbc9c0
title: 'Uso de CSP: procesos generales'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f067ef0e3cd837b1b347daac3e3da21543047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687076"
---
# <a name="using-csps-general-processes"></a>Uso de CSP: procesos generales

Al usar los CSP de [*proveedores de servicios criptográficos*](../secgloss/c-gly.md) , tenga en cuenta las siguientes convenciones.

## <a name="private-key-caching"></a>Almacenamiento en caché de clave privada

Un CSP puede almacenar en caché algunas [*claves privadas*](../secgloss/p-gly.md). Es posible controlar este almacenamiento en caché de clave privada de forma global, pero no es específico de la aplicación. El almacenamiento en caché de los cambios se realiza modificando ciertos valores del registro. Para obtener más información, vea [**constantes de almacenamiento en caché de clave privada**](private-key-caching-constants.md).

## <a name="example-code-conventions"></a>Convenciones de código de ejemplo

Para proporcionar un código más conciso y más legible, algunos de los principios de prácticas recomendadas de programación no siempre se siguen en los ejemplos. En concreto:

-   Solo se muestran las respuestas de error limitadas. Los programas completos y bien escritos comprueban los códigos de error devueltos y realizan las acciones adecuadas cuando se produce un error.
-   Solo se lleva a cabo la administración de memoria y recursos limitados. Programas completos y escritos destruyen todas las claves y [*algoritmos hash*](../secgloss/h-gly.md), liberan toda la memoria asignada, cierran todos los archivos y liberan todos los identificadores. En estos ejemplos solo se proporcionan demostraciones limitadas del uso de funciones que realizan estas tareas. En estos ejemplos no se realiza ninguna tarea de administración de recursos ni memoria en el caso de la finalización del programa debido a errores.

Los temas siguientes presentan información general sobre los ejemplos de procedimientos y el código de ejemplo.

-   [Recuperación de datos de longitud desconocida](retrieving-data-of-unknown-length.md)
-   [Enumerar protocolos admitidos](enumerating-supported-protocols.md)

 

 
