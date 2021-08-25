---
title: Personalización de la plantilla de Project
description: Personalización de la plantilla de Project
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Reproductor de Windows Media en línea, personalizar proyectos de ejemplo
- tiendas en línea, personalizar proyectos de ejemplo
- tiendas en línea de tipo 2, personalizar proyectos de ejemplo
- Reproductor de Windows Media en línea, proyectos de ejemplo
- tiendas en línea, proyectos de ejemplo
- tiendas en línea de tipo 2, proyectos de ejemplo
- personalizar proyectos de ejemplo
- samples,type 2 online stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdb57327904d81ac85114af0df9037d6c2c054938f16048f6ca72e711063cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902085"
---
# <a name="customizing-the-sample-project"></a>Personalización de la plantilla de Project

Al crear su propia tienda en línea, querrá cambiar las implementaciones de los métodos siguientes en el archivo denominado YourProject.cpp:

-   **CYourProject::allowPlay**. Use esta función para aplicar las reglas de negocio para permitir la reproducción de contenido protegido.
-   **CYourProject::allow CDProject**. Use esta función para aplicar las reglas de negocio para permitir a los usuarios copiar contenido protegido en un CD.
-   **CYourProject::allowPDATransfer**. Use esta función para aplicar las reglas de negocio para permitir a los usuarios transferir contenido protegido a un dispositivo portátil.
-   **CYourProject::startBackgroundProcessing**. Use esta función para iniciar las tareas de procesamiento en segundo plano que necesite. Por ejemplo, puede usarlo como una oportunidad para comprobar si hay licencias expiradas.
-   **CYourProject::d eviceAvailable**. Use esta función para iniciar las tareas relacionadas con un dispositivo conectado.
-   **CYourProject::p repareForSync**. Use esta función para realizar las tareas necesarias justo antes de sincronizar los medios digitales con el dispositivo.
-   **CYourProject::serviceEvent**. Use esta función para comenzar y finalizar las tareas que desea ejecutar cuando la tienda en línea sea la activa.
-   **CYourProject::stopBackgroundProcessing**. Use esta función para detener las tareas de procesamiento en segundo plano que inició Reproductor de Windows Media llamada **a CYourProject::startBackgroundProcessing.**

## <a name="working-with-media-and-playlist-objects"></a>Trabajar con objetos multimedia y de lista de reproducción

El **método allowPlay** proporciona un puntero a la **interfaz IWMPMedia** como parámetro. Esta interfaz es la interfaz Reproductor de Windows Media que representa objetos multimedia. Al llamar a los métodos de esta interfaz, puede trabajar con los atributos y propiedades de un elemento multimedia individual.

Los **métodos allowCDTransfer** **y allowPDATransfer** proporcionan un puntero a la **interfaz IWMPPlaylist** como parámetro. Esta interfaz es la interfaz Reproductor de Windows Media que representa objetos de lista de reproducción. Al llamar a los métodos de esta interfaz, puede trabajar con los atributos y propiedades de una lista de reproducción, agregar elementos a una lista de reproducción o quitar elementos de una lista de reproducción.

Para obtener información sobre cómo quitar un elemento de una lista de reproducción mediante programación, vea la implementación de **CAllowBaseDialog <T> ::OnRemoveMediaFromPlaylist**. Para obtener más información sobre cómo trabajar con objetos multimedia y de lista de reproducción, vea [Player Object Model for Scripting Languages](player-object-model-for-scripting-languages.md).

## <a name="code-that-can-be-removed"></a>Código que se puede quitar

Probablemente querrá quitar el código que abre los cuadros de diálogo porque es poco probable que quiera que los usuarios decidan qué elementos multimedia se pueden reproducir o copiar. En YourProject.h, quite el código siguiente:

-   Declaración de **CAllowBaseDialog**.
-   Declaración de **CAllowDialogDialog**.
-   Declaración de **CAllowTransferDialog**.

En YourProject.cpp, quite el código siguiente:

-   Implementación de **CAllowBaseDialog <T> ::OnInitDialog**.
-   Implementación de **CAllowBaseDialog <T> ::OnRemoveMediaFromPlaylist**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación del complemento para una tienda en línea de tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




