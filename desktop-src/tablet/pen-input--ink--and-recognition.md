---
description: Una característica nueva interesante de Tablet PC es el sistema de entrada de lápiz.
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: Entrada de lápiz, entrada de lápiz y reconocimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8645a1a68499975ad3ef5cdafb8c07685e9ed9e600cdc9ca2129babaa8b953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716273"
---
# <a name="pen-input-ink-and-recognition"></a>Entrada de lápiz, entrada de lápiz y reconocimiento

Una característica nueva interesante de Tablet PC es el sistema de entrada de lápiz. Todos los equipos tablet PC tienen un digitalizador debajo de la pantalla que acepta la entrada de lápiz. Este nuevo mecanismo de entrada requiere que piense en cómo compilar aplicaciones específicamente para Tablet PC. La interfaz de programación de aplicaciones (API) de la plataforma de Tablet PC le ayuda a hacerlo.

## <a name="collection-data-management-and-recognition"></a>Recopilación, Administración de datos y reconocimiento

La plataforma de Tablet PC se puede dividir en tres áreas distintas:

-   Colección ink (objetos que se usan para recopilar la entrada de lápiz del digitalizador).
-   Administración de datos ink (objetos que se usan para administrar la entrada de lápiz recopilada).
-   Reconocimiento de lápiz (objetos que se usan para convertir la entrada de lápiz recopilada en otros tipos de datos, como texto).

En la imagen siguiente se muestra, en un nivel alto, cómo funcionan conjuntamente Ink Collection API (Pen API), Ink Administración de datos API (Ink API) y Ink Recognition API (Recognition API) en la plataforma de Tablet PC.

![ilustración en la que se muestra cómo funcionan conjuntamente la API de lápiz, la API de entrada de lápiz y la API de reconocimiento](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

La API de la plataforma de Tablet PC está disponible en las API administradas, así como en una biblioteca COM. En los temas siguientes se describen los objetos de la API y se muestra cómo las aplicaciones usan estos objetos:

-   [Ink Collection](ink-collection.md)
-   [Datos de entrada de lápiz](ink-data.md)
-   [Reconocimiento de lápiz](ink-recognition.md)
-   [Análisis de lápiz](ink-analysis.md)
-   [Reconocimiento de escritura a mano Windows Server 2008 R2](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



