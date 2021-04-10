---
title: Personalización del proyecto de ejemplo
description: Personalización del proyecto de ejemplo
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Windows Media Player tiendas en línea, personalizar proyectos de ejemplo
- tiendas en línea, personalizar proyectos de ejemplo
- tipo 2 tiendas en línea, personalizar proyectos de ejemplo
- Windows Media Player tiendas en línea, proyectos de ejemplo
- tiendas en línea, proyectos de ejemplo
- tipo 2 tiendas en línea, proyectos de ejemplo
- personalizar proyectos de ejemplo
- ejemplos, tipo 2 tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeec3ebcb74304cd5181783e9c457d6a149b0cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994515"
---
# <a name="customizing-the-sample-project"></a>Personalización del proyecto de ejemplo

Al crear su propia tienda en línea, querrá cambiar las implementaciones de los siguientes métodos en el archivo denominado YourProject. cpp:

-   **CYourProject:: allowPlay**. Utilice esta función para aplicar las reglas de negocios para permitir la reproducción de contenido protegido.
-   **CYourProject:: allow CDBurn**. Utilice esta función para aplicar las reglas de negocios para permitir que los usuarios copien contenido protegido en un CD.
-   **CYourProject:: allowPDATransfer**. Utilice esta función para aplicar las reglas de negocios para permitir que los usuarios transfieran contenido protegido a un dispositivo portátil.
-   **CYourProject:: startBackgroundProcessing**. Utilice esta función para iniciar las tareas de procesamiento en segundo plano que necesite. Por ejemplo, podría usarlo como una oportunidad para comprobar las licencias caducadas.
-   **CYourProject::D eviceavailable**. Use esta función para iniciar cualquier tarea relacionada con un dispositivo conectado.
-   **CYourProject::P repareforsync**. Utilice esta función para realizar las tareas necesarias justo antes de sincronizar los medios digitales con el dispositivo.
-   **CYourProject:: serviceEvent**. Utilice esta función para iniciar y finalizar las tareas que desea ejecutar cuando la tienda en línea sea la activa.
-   **CYourProject:: stopBackgroundProcessing**. Use esta función para detener las tareas de procesamiento en segundo plano que se iniciaron cuando Windows Media Player llamó a **CYourProject:: startBackgroundProcessing**.

## <a name="working-with-media-and-playlist-objects"></a>Trabajar con objetos multimedia y de lista de reproducción

El método **allowPlay** proporciona un puntero a la interfaz **IWMPMedia** como parámetro. Esta interfaz es la interfaz de Media Player de Windows que representa los objetos multimedia. Al llamar a los métodos en esta interfaz, puede trabajar con los atributos y las propiedades de un elemento multimedia individual.

Los métodos **allowCDBurn** y **allowPDATransfer** proporcionan un puntero a la interfaz **IWMPPlaylist** como parámetro. Esta interfaz es la interfaz de Media Player de Windows que representa los objetos de la lista de reproducción. Al llamar a los métodos en esta interfaz, puede trabajar con los atributos y las propiedades de una lista de reproducción, agregar elementos a una lista de reproducción o quitar elementos de una lista de reproducción.

Para obtener información sobre cómo quitar un elemento de una lista de reproducción mediante programación, vea la implementación de **CAllowBaseDialog <T> :: OnRemoveMediaFromPlaylist**. Para obtener más información sobre cómo trabajar con objetos multimedia y de lista de reproducción, vea [modelo de objetos de reproductor para lenguajes de scripting](player-object-model-for-scripting-languages.md).

## <a name="code-that-can-be-removed"></a>Código que se puede quitar

Probablemente querrá quitar el código que abre los cuadros de diálogo porque es improbable que quiera que los usuarios decidan qué elementos multimedia se pueden reproducir o copiar. En YourProject. h, quite el código siguiente:

-   La declaración de **CAllowBaseDialog**.
-   La declaración de **CAllowBurnDialog**.
-   La declaración de **CAllowTransferDialog**.

En YourProject. cpp, quite el código siguiente:

-   Implementación de **CAllowBaseDialog <T> :: OnInitDialog**.
-   Implementación de **CAllowBaseDialog <T> :: OnRemoveMediaFromPlaylist**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Compilar el complemento para una tienda en línea de tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




