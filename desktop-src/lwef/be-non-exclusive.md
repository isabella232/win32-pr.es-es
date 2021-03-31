---
title: No es exclusivo
description: No es exclusivo
ms.assetid: 7a44840d-6bf9-4c12-ba14-66d7067a984d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b637bcf0860ccc4917b1af344664f9828b0da8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418532"
---
# <a name="be-non-exclusive"></a>No es exclusivo

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Los caracteres interactivos se pueden emplear en la interfaz de usuario como asistentes, guías, artistas, narradores, agentes de ventas o en otros roles. Un carácter que realice automáticamente o que ayude no debe diseñarse de forma contraria al principio de diseño de mantener el control del usuario. Al agregar un carácter a la interfaz de un sitio web o aplicación convencional, use el carácter como una mejora, en lugar de reemplazar la interfaz principal. Evite implementar cualquier característica u operación que requiera exclusivamente un carácter.

Del mismo modo, permita que el usuario elija Cuándo desea interactuar con el carácter. Un usuario debe poder descartar el carácter y hacer que se devuelva solo con el permiso del usuario. Forzar la interacción de los caracteres en los usuarios puede tener un efecto negativo grave. Para admitir el control de usuario de la interacción de caracteres, Microsoft Agent incluye automáticamente comandos para ocultar y mostrar. La API de Microsoft Agent también admite estos métodos, por lo que puede incluir compatibilidad con estas funciones en su propia interfaz. Además, la interfaz de usuario de Microsoft Agent incluye propiedades globales que permiten al usuario invalidar ciertas opciones de salida de caracteres. Para asegurarse de que se mantienen las preferencias del usuario, estas propiedades no se pueden invalidar a través de la API.

 

 




