---
description: Al hacer clic en Ejecutar expertos en la ventana Expertos de Monitor de red interfaz de usuario se inician los expertos seleccionados para el archivo de captura y se llama a la función Ejecutar. Cuando se inicia, el experto analiza el archivo de captura mediante varias funciones de fotogramas expertos.
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: Expertos en inicio y ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc85ba39c393ac253ca688a826bc77747c8d17bea29b089250a63f6f833066c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555334"
---
# <a name="starting-and-running-experts"></a>Expertos en inicio y ejecución

Al **hacer clic en Ejecutar** expertos en la ventana Expertos de Monitor de red interfaz de usuario se inician los expertos seleccionados para el archivo de captura y se llama a la función [**Ejecutar.**](run.md) Cuando se inicia, el experto analiza el archivo de captura mediante varias funciones de fotogramas expertos.

La [**función ExpertIndicateStatus proporciona**](expertindicatestatus.md) información de estado del experto. Al ejecutar un experto con Monitor de red, la ventana Vista de estado experto muestra información de estado actualizada periódicamente (de 0 a 100 % de finalización).

![ventana de vista de estado experto](images/exview.png)

El experto está activo hasta que los datos completan su paso a través del archivo de captura. Cuando se complete el paso, aparecerá Visor de eventos ventana. La información de esta ventana depende del tipo de experto que analizó los datos. En la ilustración siguiente se muestra una vista de experto de distribución de propiedades, que resume los datos del marco que el experto analizó.

![vista de experto de distribución de propiedades](images/exview1.png)

Un segundo informe (no mostrado) resume los resultados del experto retransmitido del Protocolo de control de transmisión (TCP).

También puede:

-   Cree una entrada para una página de referencia de eventos (ERP) que informe al usuario de las condiciones o problemas detectados (como se muestra en la ventana Análisis).
-   Cree entradas para correcciones sugeridas o datos explicativos que proporcionen información adicional (como se muestra en la ventana Resolución).

Una vez que el experto completa su tarea, Monitor de red quita el experto de la memoria activa. Los expertos deben usar las funciones de memoria protegida incluidas en platform software development kit (SDK); estas funciones limpian la memoria si se producirá un error en los expertos durante el tiempo de ejecución.

 

 



