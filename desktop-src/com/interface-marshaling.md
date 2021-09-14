---
title: Serialización de interfaces
description: Serialización de interfaces
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5112b67e643fb95e1025fd4ed297043f81f576e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965220"
---
# <a name="interface-marshaling"></a>Serialización de interfaces

A menos que sepa sin duda que la interfaz nunca se usará a través de los límites de apartamento, subproceso o proceso, debe decidir cómo proporcionar compatibilidad con la serialización para las interfaces. Hay tres maneras de proporcionar compatibilidad con la serialización:

-   Escriba su propio código proxy/código auxiliar que llame al canal COM, que a su vez llama a las bibliotecas rpc en tiempo de ejecución. En teoría, es posible hacerlo, pero en la práctica es casi imposible hacerlo sin una cantidad significativa de esfuerzo.
-   Describa las interfaces en un archivo de lenguaje de definición de interfaz (IDL) y use el compilador MIDL para generar un archivo DLL de proxy o código auxiliar. Este método proporciona el mejor rendimiento y la máxima flexibilidad en términos de tipos de datos aceptables. Con los códigos auxiliares de proxy generados por MIDL, puede controlar no solo la administración de memoria, sino también la serialización y desmarque de tipos de datos complejos en distintas plataformas.
-   Use MIDL para generar una biblioteca de tipos que el sistema usa para proporcionar compatibilidad con la serialización en tiempo de ejecución. Esta es la manera más fácil de implementar la compatibilidad con la serialización. Todo lo que tiene que hacer es generar una biblioteca de tipos y registrarla. Las interfaces deben ser compatibles con Automation [**(oleautomation**](/windows/desktop/Midl/oleautomation) o [**dual),**](/windows/desktop/Midl/dual)lo que coloca algunas restricciones en los tipos de tipos de datos que puede usar como parámetros de método. Sin embargo, en la mayoría de los casos, la ventaja de tener las interfaces accesibles para programas escritos en otros lenguajes, como Microsoft Visual Basic y Java, supera las limitaciones de los tipos de datos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comunicación entre objetos](inter-object-communication.md)
</dt> </dl>

 

 