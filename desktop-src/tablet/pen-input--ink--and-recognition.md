---
description: Una nueva característica interesante de Tablet PC es el sistema de entrada manuscrita.
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: Entrada de lápiz, tinta y reconocimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d865e40d1779edaa2607b1754c45659609b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558862"
---
# <a name="pen-input-ink-and-recognition"></a>Entrada de lápiz, tinta y reconocimiento

Una nueva característica interesante de Tablet PC es el sistema de entrada manuscrita. Todos los equipos de Tablet PC tienen un digitalizador debajo de la pantalla que acepta entradas manuscritas. Este nuevo mecanismo de entrada requiere que piense en cómo crear aplicaciones específicamente para Tablet PC. La interfaz de programación de aplicaciones (API) de la plataforma de Tablet PC le ayuda a hacerlo.

## <a name="collection-data-management-and-recognition"></a>Recopilación, Administración de datos y reconocimiento

La plataforma de Tablet PC se puede dividir en tres áreas distintas:

-   Colección de entradas manuscritas (objetos que se usan para recopilar entradas manuscritas del digitalizador).
-   Administración de datos de tinta (objetos que se usan para administrar la entrada de lápiz recopilada).
-   Reconocimiento de entradas manuscritas (objetos que se usan para convertir la entrada manuscrita recopilada en otros tipos de datos, como texto).

En la siguiente imagen se muestra, en un nivel alto, cómo la API de recopilación de tintas (lápiz API), la API de Ink Administración de datos (API de tinta) y la API de reconocimiento de tinta (API de reconocimiento) funcionan en conjunto en la plataforma de Tablet PC.

![Ilustración que muestra cómo la API de lápiz, la API de tinta y la API de reconocimiento funcionan juntas](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

La API de la plataforma de Tablet PC está disponible en las API administradas y en una biblioteca COM. En los temas siguientes se describen los objetos de la API y se ilustra cómo usan estos objetos:

-   [Colección de entradas manuscritas](ink-collection.md)
-   [Datos de tinta](ink-data.md)
-   [Reconocimiento de tinta](ink-recognition.md)
-   [Análisis de tinta](ink-analysis.md)
-   [Reconocimiento de escritura a mano en Windows Server 2008 R2](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



