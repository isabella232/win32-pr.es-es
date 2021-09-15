---
description: Al usar los PROVEEDORES de servicios criptográficos, tenga en cuenta las siguientes convenciones.
ms.assetid: 70053b89-4d39-4a86-985a-0e8f05fbc9c0
title: 'Uso de LOSP: procesos generales'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f067ef0e3cd837b1b347daac3e3da21543047d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127477662"
---
# <a name="using-csps-general-processes"></a>Uso de LOSP: procesos generales

Al usar [*los PROVEEDORES de servicios criptográficos,*](../secgloss/c-gly.md) tenga en cuenta las siguientes convenciones.

## <a name="private-key-caching"></a>Almacenamiento en caché de claves privadas

Un CSP puede almacenar en caché algunas [*claves privadas.*](../secgloss/p-gly.md) Es posible controlar este almacenamiento en caché de claves privadas de forma global, pero no específica de la aplicación. Los cambios de almacenamiento en caché se realizan mediante la modificación de determinadas configuraciones del Registro. Para obtener más información, vea [**Constantes de almacenamiento en caché de claves privadas.**](private-key-caching-constants.md)

## <a name="example-code-conventions"></a>Convenciones de código de ejemplo

Para proporcionar código más conciso y legible, algunos principios de una buena práctica de programación no siempre se siguen en los ejemplos. En concreto:

-   Solo se muestran respuestas de error limitadas. Los programas completos y bien escritos comprueban los códigos de error devueltos y realizan las acciones adecuadas cuando se encuentra un error.
-   Solo se realiza la administración limitada de recursos y memoria. Los programas completos y bien escritos destruyen todas las claves y [*hashes,*](../secgloss/h-gly.md)liberan toda la memoria asignada, cierran todos los archivos y liberan todos los identificadores. Estos ejemplos proporcionan solo demostraciones limitadas del uso de funciones que realizan estas tareas. Estos ejemplos no realizan tareas de administración de recursos o memoria en caso de finalización del programa debido a errores.

En los temas siguientes se presenta información general sobre ejemplos de procedimientos, así como código de ejemplo.

-   [Recuperar datos de longitud desconocida](retrieving-data-of-unknown-length.md)
-   [Enumeración de protocolos admitidos](enumerating-supported-protocols.md)

 

 
