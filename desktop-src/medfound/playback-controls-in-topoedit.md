---
description: Controles de reproducción en TopoEdit
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: Controles de reproducción en TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174317fbf53dc6d2573414c60d5d4cde1a010f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564847"
---
# <a name="playback-controls-in-topoedit"></a>Controles de reproducción en TopoEdit

Una vez que se resuelve una topología, se pone en cola en la sesión multimedia para la reproducción. TopoEdit proporciona control de transporte para cambiar el estado de la topología en la sesión multimedia.

En la tabla siguiente se muestra el comando de menú/barra de herramientas y el método de Media Foundation equivalente para cada operación.



| Comando de menú/barra de herramientas                                                                                                                                                                                                                          | Método Media Foundation                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| En el menú **controles** , haga clic en **reproducir**. \[ nueva línea \] : o bien, \[ \] haga clic en el botón **reproducir** de la barra de herramientas (se muestra en la siguiente imagen). \[ \] ![ captura de pantalla de nueva línea del botón reproducir](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)    | [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| En el menú **controles** , haga clic en **detener**. \[ nueva línea \] -o- \[ nueva línea \] haga clic en el botón **detener** de la barra de herramientas (se muestra en la siguiente imagen). \[ \] ![ captura de pantalla de nueva línea del botón detener](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)    | [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| En el menú **controles** , haga clic en **pausar**. \[ nueva línea \] : o bien, \[ \] haga clic en el botón **pausar** de la barra de herramientas (se muestra en la siguiente imagen). \[ \] ![ captura de pantalla de nueva línea del botón pausar](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg) | [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

Para obtener información sobre cómo controlar la reproducción mediante programación con Media Foundation API, vea [Cómo controlar los Estados de presentación](how-to-control-presentation-states.md).

## <a name="seeking"></a>Invoca

Si se puede buscar en la topología, puede buscar mediante la barra de búsqueda (que se muestra en la imagen siguiente) para especificar un lugar en la escala de tiempo de la topología para comenzar la reproducción.

![captura de pantalla de la barra de búsqueda](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> Si se puede buscar en el origen de medios, el comando STOP también busca la topología en el inicio de la secuencia.

 

## <a name="changing-the-playback-rate"></a>Cambiar la velocidad de reproducción

Si el origen de medios subyacentes de la topología admite varias velocidades de reproducción, puede usar la barra de frecuencia para cambiar la velocidad de reproducción. Para avanzar rápidamente una topología en la sesión multimedia, aumente la velocidad arrastrando el control deslizante hacia la derecha, tal como se muestra en la siguiente imagen.

![captura de pantalla de la barra de tasa](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> En esta versión, TopoEdit solo admite tarifas positivas. No se admite la reproducción inversa.

 

Para obtener información sobre cómo cambiar la velocidad de reproducción mediante programación con Media Foundation API, vea [About Rate Control](about-rate-control.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Menús de TopoEdit](topoedit-menus.md)
</dt> <dt>

[Barra de herramientas TopoEdit](topoedit-toolbar.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



