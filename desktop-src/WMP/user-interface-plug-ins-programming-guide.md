---
title: Guía de programación de complementos de la interfaz de usuario
description: Guía de programación de complementos de la interfaz de usuario
ms.assetid: 7bc0805a-306d-4b48-bc24-41077c8c7b3d
keywords:
- Media Player de Windows, Complementos
- Media Player de Windows, Complementos de la interfaz de usuario
- Complementos de Windows Media Player, interfaz de usuario
- complementos, interfaz de usuario
- Complementos de la interfaz de usuario, guía de programación
- Complementos de la interfaz de usuario, guía de programación
- Guía de programación, Complementos de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d417d246e92a642711e8cb02f77ff3795d47c995
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903644"
---
# <a name="user-interface-plug-ins-programming-guide"></a>Guía de programación de complementos de la interfaz de usuario

Los dos ejemplos de código que se describen en esta sección muestran el proceso de implementación de un complemento de interfaz de usuario personalizado a partir del código generado por el Asistente para complementos de Media Player de Windows.

El complemento de la interfaz de usuario de búsqueda es un complemento de área de metadatos que proporciona un botón de **búsqueda** . Al hacer clic en este botón, se inicia una página de búsqueda en el explorador Web predeterminado que contiene información sobre el artista del elemento multimedia actual.

El primer paso para crear este complemento es iniciar un nuevo proyecto en Microsoft Visual C++ seleccionando el **Asistente para complementos de Windows Media Player** en la pestaña **proyectos** . Asigne al proyecto el nombre "Buscar" y haga clic en **Aceptar**. Elija **complemento de la interfaz de usuario** y haga clic en **siguiente**. A continuación, elija el tipo de metadatos en la lista de opciones y haga clic en **siguiente**. Por último, haga clic en la casilla compatibilidad con la ejecución automática para que el complemento se cargue automáticamente y, a continuación, haga clic en **Finalizar**. El asistente genera los archivos de proyecto necesarios, incluidas las implementaciones básicas de la clase CSearch y la interfaz **IWMPPluginUI** que admite, y la clase CPluginWindow que proporciona la interfaz de usuario. Este es el código que se modificará para proporcionar la funcionalidad de complemento que se describe en esta sección.

En el último tema de esta sección se describe cómo crear un complemento de la interfaz de usuario de fondo para Windows Media Player 10 Mobile. Este complemento usa código modificado generado a partir del Asistente para complementos de Media Player de Windows para crear un complemento para Windows Media Player 10 Mobile.

Esta sección contiene los temas siguientes.



| Tema                                                                                                                                            | Descripción                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Implementación de CSearch](implementing-csearch.md)                                                                                                 | Describe los cambios necesarios para la clase CSearch.                                |
| [Implementación de CPluginWindow](implementing-cpluginwindow.md)                                                                                     | Describe los cambios necesarios para la clase CPluginWindow.                          |
| [Crear un complemento de la interfaz de usuario para Windows Media Player 10 Mobile](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md) | Describe cómo crear un complemento de la interfaz de usuario de fondo para Windows Media Player 10 Mobile. |



 

 

 




