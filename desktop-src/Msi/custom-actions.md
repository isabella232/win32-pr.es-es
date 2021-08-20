---
description: El instalador Windows proporciona muchas acciones integradas para realizar el proceso de instalación. Para obtener una lista de estas acciones, consulte la Referencia de acciones estándar.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3e2eb466934d7d332307e0d5288d6d328297d7664d884e62c406eb3409728a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947906"
---
# <a name="custom-actions"></a>Acciones personalizadas

El instalador Windows proporciona muchas acciones integradas para realizar el proceso de instalación. Para obtener una lista de estas acciones, consulte la [Referencia de acciones estándar](standard-actions-reference.md).

Las acciones estándar son suficientes para ejecutar una instalación en la mayoría de los casos. Sin embargo, hay situaciones en las que el desarrollador de un paquete de instalación encuentra que es necesario escribir una acción personalizada. Por ejemplo:

-   Quiere iniciar un archivo ejecutable durante la instalación que se instala en la máquina del usuario o que se está instalando con la aplicación.
-   Quiere llamar a funciones especiales durante una instalación que se definen en una biblioteca de vínculos dinámicos (DLL).
-   Quiere usar funciones escritas en los lenguajes de desarrollo Microsoft Visual Basic Scripting Edition o Microsoft JScript texto de script literal durante una instalación.
-   Quiere aplazar la ejecución de algunas acciones hasta el momento en que se ejecuta el script de instalación.
-   Quiere agregar información de tiempo y progreso a un control ProgressBar y un control TimeRemaining Text.

En las secciones siguientes se describen las acciones personalizadas y cómo incorporarlas a un paquete de instalación:

-   [Acerca de las acciones personalizadas](about-custom-actions.md)
-   [Uso de acciones personalizadas](using-custom-actions.md)
-   [Referencia de acción personalizada](custom-action-reference.md)
-   [Lista de resumen de todos los tipos de acción personalizados](summary-list-of-all-custom-action-types.md)

 

 



