---
description: Una característica nueva interesante de Tablet PC es el sistema de entrada de lápiz.
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: Entrada de lápiz, entrada manuscrita y reconocimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d865e40d1779edaa2607b1754c45659609b5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360245"
---
# <a name="pen-input-ink-and-recognition"></a>Entrada de lápiz, entrada manuscrita y reconocimiento

Una característica nueva interesante de Tablet PC es el sistema de entrada de lápiz. Todos los equipos tablet PC tienen un digitalizador debajo de la pantalla que acepta entradas de lápiz. Este nuevo mecanismo de entrada requiere que piense en cómo compilar aplicaciones específicamente para Tablet PC. La interfaz de programación de aplicaciones (API) de la plataforma tablet PC le ayuda a hacerlo.

## <a name="collection-data-management-and-recognition"></a>Recopilación, Administración de datos y reconocimiento

La plataforma tablet PC se puede dividir en tres áreas distintas:

-   Colección de entrada de lápiz (objetos que se usan para recopilar la entrada de lápiz del digitalizador).
-   Administración de datos de entrada manuscrita (objetos que se usan para administrar la entrada de lápiz recopilada).
-   Reconocimiento de entrada de lápiz (objetos que se usan para convertir la entrada de lápiz recopilada en otros tipos de datos, como texto).

En la imagen siguiente se muestra, en un nivel alto, cómo funcionan conjuntamente Ink Collection API (Pen API), Ink Administración de datos API (Ink API) y Ink Recognition API (Recognition API) en la plataforma de Tablet PC.

![ilustración en la que se muestra cómo funcionan conjuntamente la API de lápiz, la API de entrada de lápiz y la API de reconocimiento](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

La API de la plataforma de Tablet PC está disponible en las API administradas, así como en una biblioteca COM. En los temas siguientes se describen los objetos de la API y se muestra cómo las aplicaciones usan estos objetos:

-   [Colección de entrada de lápiz](ink-collection.md)
-   [Datos de entrada de lápiz](ink-data.md)
-   [Reconocimiento de entrada de lápiz](ink-recognition.md)
-   [Análisis de entrada de lápiz](ink-analysis.md)
-   [Reconocimiento de escritura a mano Windows Server 2008 R2](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



