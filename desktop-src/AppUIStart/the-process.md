---
title: Información general sobre el desarrollo de la interfaz de usuario
description: En esta sección se describen las tres fases del diseño de la interfaz de usuario y se presentan las tareas que normalmente están asociadas a cada fase.
ms.assetid: ab544cb9-eed3-4575-a8dd-2f5d7b5c575f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b531fb07a1805c14441c81777bbdddad0739e7cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170190"
---
# <a name="overview-of-the-user-interface-development-process"></a>Información general del proceso de Interfaz de usuario desarrollo

En esta sección se describen las tres fases del diseño de la interfaz de usuario y se presentan las tareas que normalmente están asociadas a cada fase.

## <a name="the-application-user-interface-and-the-user-experience"></a>La aplicación Interfaz de usuario y la experiencia del usuario

Para empezar, se deben aclarar los términos "interfaz de usuario" y "experiencia del usuario".

La interfaz de usuario de una aplicación normalmente implica los objetos con los que un usuario ve e interactúa directamente en su pantalla. Por ejemplo, estos objetos incluyen el espacio del documento, los menús, los cuadros de diálogo, los iconos, las imágenes y las animaciones.

Sin embargo, la interfaz de usuario de una aplicación es solo un aspecto de la experiencia general del usuario. Otros aspectos de la experiencia del usuario que no son visibles para el usuario, pero que son integrales para una aplicación y críticos para su facilidad de uso, incluyen el tiempo de inicio, la latencia, el control de errores y las tareas automatizadas que se completan sin interacción directa del usuario.

En general, una interfaz de usuario requiere la acción de un usuario para realizar una tarea, mientras que se puede lograr una experiencia de usuario excelente sin ninguna interfaz de usuario.

## <a name="user-interface-development"></a>Interfaz de usuario development

Proporcionar una experiencia de usuario correcta requiere un enfoque equilibrado a lo largo del ciclo de vida de desarrollo. Para garantizar este equilibrio, no solo debe centrarse en implementar la funcionalidad necesaria para completar una tarea, sino también en cómo se expone la tarea a través de la interfaz de usuario. Recuerde que la interfaz de usuario no solo debe ser funcional, sino que también debe poder usarse.

A continuación se describen las fases típicas del proceso de desarrollo de la interfaz de usuario:

### <a name="designing"></a>Diseño

-   Requisitos funcionales: determine los requisitos y los objetivos iniciales de la aplicación.
-   Análisis de usuarios: identifique los escenarios de usuario y comprenda las necesidades y expectativas de los usuarios para cada escenario.
-   Diseño conceptual: modele el negocio subyacente que la aplicación debe admitir.
-   Diseño lógico: diseñe el proceso y el flujo de información de la aplicación.
-   Diseño físico: decida cómo se implementará el diseño lógico en plataformas físicas específicas.

### <a name="implementing"></a>Implementar

-   Prototipo: desarrolle prototipos de papel o de pantalla interactiva que se centren en la interfaz y no incluyan elementos de diseño visuales que distraen.
-   Construcción: compile la aplicación y prepárese para las solicitudes de cambio de diseño.

### <a name="testing"></a>Prueba

-   Pruebas de facilidad de uso: pruebe la aplicación con varios usuarios y escenarios.
-   Pruebas de accesibilidad: pruebe la aplicación con tecnologías accesibles y herramientas de prueba automatizadas.

 

 




