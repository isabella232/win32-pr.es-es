---
title: Serialización de interfaces
description: Serialización de interfaces
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5112b67e643fb95e1025fd4ed297043f81f576e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705031"
---
# <a name="interface-marshaling"></a>Serialización de interfaces

A menos que sepa más allá de la duda de que la interfaz nunca se usará en los límites de apartamento, subproceso o proceso, debe decidir cómo proporcionar compatibilidad de serialización para las interfaces. Hay tres maneras de proporcionar compatibilidad con el cálculo de referencias:

-   Escriba su propio código de proxy o código auxiliar que llama al canal COM, que a su vez llama a las bibliotecas en tiempo de ejecución de RPC. Teóricamente, es posible hacer esto, pero en la práctica es casi imposible hacerlo sin una cantidad significativa de esfuerzo.
-   Describa las interfaces en un archivo de lenguaje de definición de interfaz (IDL) y use el compilador MIDL para generar un archivo DLL de proxy/código auxiliar. Este método proporciona el mejor rendimiento y la mayor flexibilidad en términos de tipos de datos aceptables. Mediante el uso de código auxiliar de proxy generado por MIDL, puede controlar no solo la administración de memoria, sino también la serialización y la desserialización de tipos de datos complejos en distintas plataformas.
-   Use MIDL para generar una biblioteca de tipos que el sistema utiliza para proporcionar compatibilidad de serialización en tiempo de ejecución. Esta es la manera más sencilla de implementar la compatibilidad con el cálculo de referencias. Todo lo que tiene que hacer es generar una biblioteca de tipos y registrarla. Las interfaces deben ser compatibles con la automatización (ya sea [**oleautomation**](/windows/desktop/Midl/oleautomation) o [**dual**](/windows/desktop/Midl/dual)), lo que establece algunas restricciones en los tipos de datos que se pueden usar como parámetros de método. Sin embargo, en la mayoría de los casos, la ventaja de tener las interfaces accesibles para los programas escritos en otros lenguajes, como Microsoft Visual Basic y Java, supera las limitaciones en los tipos de datos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comunicación entre objetos](inter-object-communication.md)
</dt> </dl>

 

 