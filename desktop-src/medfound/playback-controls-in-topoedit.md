---
description: Controles de reproducción en TopoEdit
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: Controles de reproducción en TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174317fbf53dc6d2573414c60d5d4cde1a010f95
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580245"
---
# <a name="playback-controls-in-topoedit"></a>Controles de reproducción en TopoEdit

Una vez resuelta una topología, se pone en cola en la sesión multimedia para su reproducción. TopoEdit proporciona control de transporte para cambiar el estado de la topología en la sesión multimedia.

En la tabla siguiente se muestra el comando de menú o barra de herramientas y el método Media Foundation equivalente para cada operación.



| Menú o comando de barra de herramientas                                                                                                                                                                                                                          | Media Foundation (método)                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| En el menú **Controles** , haga clic en **Reproducir**. \[ newline -o bien- newline haga clic en el botón reproducir de la barra de \] \[ herramientas \] (que se muestra en la siguiente imagen).  \[ Captura de \] ![ pantalla de nueva línea del botón de reproducción](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)    | [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| En el menú **Controles** , haga clic en **Detener.** \[ newline -o bien- newline haga clic en el botón Detener de la barra de \] \[ herramientas \] (que se muestra en la siguiente imagen).  \[ Captura de pantalla \] ![ de nueva línea del botón Detener](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)    | [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| En el menú **Controles** , haga clic **en Pausar**. \[ newline -o bien- newline haga clic en el botón pausar de la barra de \] \[ herramientas \] (que se muestra en la siguiente imagen).  \[ Captura de pantalla \] ![ de nueva línea del botón pausar](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg) | [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

Para obtener información sobre cómo controlar la reproducción mediante programación mediante Media Foundation API, vea [How to Control Presentation States](how-to-control-presentation-states.md).

## <a name="seeking"></a>Buscando

Si la topología es buscable, puede buscar mediante la barra de búsqueda (que se muestra en la siguiente imagen) para especificar un lugar en la escala de tiempo de la topología para iniciar la reproducción.

![captura de pantalla de la barra de búsqueda](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> Si el origen del medio es buscable, el comando Stop también busca la topología al principio de la secuencia.

 

## <a name="changing-the-playback-rate"></a>Cambiar la velocidad de reproducción

Si el origen multimedia subyacente de la topología admite varias velocidades de reproducción, puede usar la barra de velocidad para cambiar la velocidad de reproducción. Para avanzar rápidamente una topología en la sesión multimedia, aumente la velocidad arrastrando el control deslizante a la derecha, como se muestra en la imagen siguiente.

![captura de pantalla de la barra de velocidad](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> En esta versión, TopoEdit solo admite tasas positivas. No se admite la reproducción inversa.

 

Para obtener información sobre cómo cambiar la velocidad de reproducción mediante programación mediante Media Foundation API, vea [About Rate Control](about-rate-control.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Menús TopoEdit](topoedit-menus.md)
</dt> <dt>

[TopoEdit Toolbar](topoedit-toolbar.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



