---
description: Controles de reproducción en TopoEdit
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: Controles de reproducción en TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c59dfceb30f839ba58d37385a3178d42429eb858c98f3f5196dd95141ac2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239687"
---
# <a name="playback-controls-in-topoedit"></a>Controles de reproducción en TopoEdit

Una vez resuelta una topología, se pone en cola en la sesión multimedia para su reproducción. TopoEdit proporciona control de transporte para cambiar el estado de la topología en la sesión multimedia.

En la tabla siguiente se muestra el comando de menú o barra de herramientas y el método Media Foundation equivalente para cada operación.



| Comando menú/barra de herramientas                                                                                                                                                                                                                          | Media Foundation método                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| En el menú **Controles** , haga clic en **Reproducir**. \[ newline \] -o bien- newline haga clic en el botón de reproducción de la barra de herramientas \[ \] (que se muestra en la siguiente imagen).  \[ Captura de \] ![ pantalla de nueva línea del botón de reproducción](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)    | [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| En el menú **Controles** , haga clic en **Detener**. \[ newline \] -o bien- newline haga clic en el botón Detener de la barra de \[ herramientas \] (que se muestra en la siguiente imagen).  \[ Captura de \] ![ pantalla de nueva línea del botón Detener](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)    | [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| En el menú **Controles** , haga clic **en Pausar**. \[ newline -o bien- newline haga clic en el botón pausar de \] la barra de herramientas \[ \] (que se muestra en la siguiente imagen).  \[ captura de \] ![ pantalla de nueva línea del botón pausar](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg) | [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

Para obtener información sobre cómo controlar la reproducción mediante programación mediante Media Foundation API, vea [Cómo controlar los estados de presentación](how-to-control-presentation-states.md).

## <a name="seeking"></a>Buscando

Si la topología es buscable, puede buscar mediante la barra de búsqueda (que se muestra en la siguiente imagen) para especificar un lugar en la escala de tiempo de la topología para comenzar la reproducción.

![captura de pantalla de la barra de búsqueda](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> Si el origen del medio es buscable, el comando Stop también busca la topología al principio de la secuencia.

 

## <a name="changing-the-playback-rate"></a>Cambiar la velocidad de reproducción

Si el origen multimedia subyacente de la topología admite varias velocidades de reproducción, puede usar la barra de velocidad para cambiar la velocidad de reproducción. Para avanzar rápidamente una topología en la sesión multimedia, aumente la velocidad arrastrando el control deslizante a la derecha, como se muestra en la siguiente imagen.

![captura de pantalla de la barra de velocidad](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> En esta versión, TopoEdit solo admite tasas positivas. No se admite la reproducción inversa.

 

Para obtener información sobre cómo cambiar la velocidad de reproducción mediante programación mediante Media Foundation API, vea [Acerca del control de velocidad.](about-rate-control.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Menús TopoEdit](topoedit-menus.md)
</dt> <dt>

[TopoEdit Toolbar](topoedit-toolbar.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



