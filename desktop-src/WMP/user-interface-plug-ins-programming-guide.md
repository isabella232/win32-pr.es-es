---
title: Interfaz de usuario de programación de complementos de Interfaz de usuario
description: Interfaz de usuario de programación de complementos de Interfaz de usuario
ms.assetid: 7bc0805a-306d-4b48-bc24-41077c8c7b3d
keywords:
- Reproductor de Windows Media,complementos
- Reproductor de Windows Media complementos de interfaz de usuario
- Reproductor de Windows Media complementos,interfaz de usuario
- complementos, interfaz de usuario
- complementos de interfaz de usuario, guía de programación
- Complementos de interfaz de usuario, guía de programación
- guía de programación, complementos de interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d417d246e92a642711e8cb02f77ff3795d47c995
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465794"
---
# <a name="user-interface-plug-ins-programming-guide"></a>Interfaz de usuario de programación de complementos de Interfaz de usuario

Los dos ejemplos de código que se describen en esta sección muestran el proceso de implementación de un complemento de interfaz de usuario (UI) personalizado a partir del código generado por el Asistente para complementos de Reproductor de Windows Media.

El complemento Search UI es un complemento de área de metadatos que proporciona un **botón** Buscar. Cuando se hace clic en este botón, se inicia una página de búsqueda en el explorador web predeterminado que contiene información sobre el intérprete del elemento multimedia actual.

El primer paso **para** crear este complemento es iniciar un nuevo proyecto en Microsoft Visual C++ seleccionando el Asistente para complementos Reproductor de Windows Media en la **pestaña** Proyectos. Asigne al proyecto el nombre "Search" y haga clic **en Aceptar.** Elija **Ui Plug-in (Complemento de interfaz de usuario)** y haga clic **en Next (Siguiente).** A continuación, elija el tipo de metadatos en la lista de opciones y haga clic **en Siguiente.** Por último, haga clic en la casilla de compatibilidad con la ejecución automática para que el complemento se cargue automáticamente y, a continuación, haga clic **en Finalizar.** El asistente genera los archivos de proyecto necesarios, incluidas las implementaciones básicas de la clase CSearch y la interfaz **IWMPPluginUI** que admite, y la clase CPluginWindow que proporciona la interfaz de usuario. Este es el código que se modificará para proporcionar la funcionalidad de complemento descrita en esta sección.

En el último tema de esta sección se describe cómo crear un complemento de interfaz de usuario en segundo plano para Reproductor de Windows Media 10 Mobile. Este complemento usa el código modificado generado a partir del Asistente para complementos de Reproductor de Windows Media para crear un complemento para Reproductor de Windows Media 10 Mobile.

Esta sección contiene los temas siguientes.



| Tema                                                                                                                                            | Descripción                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Implementación de CSearch](implementing-csearch.md)                                                                                                 | Describe los cambios necesarios en la clase CSearch.                                |
| [Implementación de CPluginWindow](implementing-cpluginwindow.md)                                                                                     | Describe los cambios necesarios en la clase CPluginWindow.                          |
| [Creación de Interfaz de usuario complemento para Reproductor de Windows Media 10 Mobile](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md) | Describe cómo crear un complemento de interfaz de usuario en segundo plano para Reproductor de Windows Media 10 Mobile. |



 

 

 




