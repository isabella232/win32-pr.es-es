---
description: El Windows Installer proporciona muchas acciones integradas para realizar el proceso de instalación. Para obtener una lista de estas acciones, consulte la referencia de acciones estándar.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9623351bdcd4cd109d2112724d13e0f9ccaa6b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082786"
---
# <a name="custom-actions"></a>Acciones personalizadas

El Windows Installer proporciona muchas acciones integradas para realizar el proceso de instalación. Para obtener una lista de estas acciones, consulte la [referencia de acciones estándar](standard-actions-reference.md).

Las acciones estándar son suficientes para ejecutar una instalación en la mayoría de los casos. Sin embargo, hay situaciones en las que el desarrollador de un paquete de instalación encuentra que es necesario escribir una acción personalizada. Por ejemplo:

-   Quiere iniciar un archivo ejecutable durante la instalación que está instalado en el equipo del usuario o que se está instalando con la aplicación.
-   Desea llamar a funciones especiales durante una instalación definida en una biblioteca de vínculos dinámicos (DLL).
-   Quiere usar funciones escritas en los lenguajes de desarrollo Microsoft Visual Basic Scripting Edition o el texto de script literal de Microsoft JScript durante una instalación.
-   Desea aplazar la ejecución de algunas acciones hasta el momento en que se ejecuta el script de instalación.
-   Desea agregar información de tiempo y progreso a un control ProgressBar y a un control de texto TimeRemaining.

En las secciones siguientes se describen las acciones personalizadas y cómo incorporarlas en un paquete de instalación:

-   [Acerca de las acciones personalizadas](about-custom-actions.md)
-   [Uso de acciones personalizadas](using-custom-actions.md)
-   [Referencia de acción personalizada](custom-action-reference.md)
-   [Lista de Resumen de todos los tipos de acciones personalizadas](summary-list-of-all-custom-action-types.md)

 

 



