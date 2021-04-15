---
description: Al hacer clic en ejecutar expertos en la ventana expertos de la interfaz de usuario de Monitor de red se inician los expertos seleccionados para el archivo de captura y se llama a la función ejecutar. Cuando se inicia, el experto analiza el archivo de captura mediante el uso de varias funciones de marco de experto.
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: Expertos en Inicio y en ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bd41472d286727541d26bade1942eb3b6b5c593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688632"
---
# <a name="starting-and-running-experts"></a>Expertos en Inicio y en ejecución

Al hacer clic en **Ejecutar expertos** en la ventana expertos de la interfaz de usuario de monitor de red se inician los expertos seleccionados para el archivo de captura y se llama a la función [**Ejecutar**](run.md) . Cuando se inicia, el experto analiza el archivo de captura mediante el uso de varias funciones de marco de experto.

La función [**ExpertIndicateStatus**](expertindicatestatus.md) proporciona información de estado del experto. Al ejecutar un experto con Monitor de red, la ventana vista de estado de experto muestra información de estado actualizada periódicamente (de 0 a 100% de finalización).

![ventana vista de estado de experto](images/exview.png)

El experto está activo hasta que los datos completan su paso a través del archivo de captura. Cuando se complete el paso, aparecerá una ventana de Visor de eventos. La información de esta ventana depende del tipo de experto que ha analizado los datos. En la ilustración siguiente se muestra una vista experta de distribución de propiedades, que resume los datos del marco analizados por el experto.

![vista de experto de distribución de propiedades](images/exview1.png)

Un segundo informe (no se muestra), resume los resultados del experto de retransmisión del Protocolo de control de transmisión (TCP).

También puede:

-   Cree una entrada para una página de referencia de eventos (ERP) que aconseje al usuario las condiciones o problemas detectados (como se muestra en la ventana de análisis).
-   Cree entradas para correcciones o datos explicativos sugeridos que proporcionen información adicional (como se muestra en la ventana de resolución).

Una vez que el experto completa su tarea, Monitor de red quita el experto de la memoria activa. Los expertos deben usar las funciones de memoria protegida incluidas en el kit de desarrollo de software (SDK) de la plataforma. Estas funciones limpian la memoria si se produce un error en los expertos durante el tiempo de ejecución.

 

 



