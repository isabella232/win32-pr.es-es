---
title: Cadenas de formato NDR de RPC
description: Cadenas de formato NDR de llamada a procedimiento remoto (RPC).
ms.assetid: 9c83a039-49d3-491d-8110-29d1548730de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf0569a913d6c5a4b19b342cc288d6a8682dfc4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904789"
---
# <a name="rpc-ndr-format-strings"></a>Cadenas de formato NDR de RPC

## <a name="ndr-engine-32-bit-interpreter"></a>Motor NDR: intérprete de 32 bits

En este documento se describen los descriptores de cadena de formato, a veces denominados MOPs, para el motor NDR de 32 bits. En esta sección se describen los cambios asociados con la evolución del intérprete [**– OI**](/windows/desktop/Midl/-oi) a la capa de intérpretes **– salientes** , así como las adiciones relacionadas con las canalizaciones y la compatibilidad asincrónica.

En este documento se describe la tecnología de Lenguaje de definición de interfaz de Microsoft actual (MIDL) desde la perspectiva del motor y el motor NDR actual.

## <a name="overview"></a>Información general

El motor NDR es el motor de serialización de los componentes llamada a procedimiento remoto (RPC) y DCOM. Controla todos los problemas relacionados con el código auxiliar de una llamada remota. Como proceso, el cálculo de referencias de NDR está controlado por el código C de los códigos auxiliares generados por MIDL, un generador de tipos JIT de MIDL o por códigos auxiliares generados por otras herramientas o escritos manualmente. A su vez, el motor NDR impulsa el tiempo de ejecución subyacente (DCOM o RPC) que se comunica con transportes específicos.

El objetivo original del diseño era proporcionar una herramienta para la serialización efectiva de datos arbitrarios, en función de la información proporcionada por el compilador de MIDL. Las cadenas de formato descritas en este documento y, en realidad, toda la información generada por el compilador para el consumo del motor NDR, siempre se han considerado una interfaz interna entre el compilador y el motor. Del mismo modo, las interfaces disponibles para el motor para controlar los problemas en tiempo de ejecución también son principalmente internas (algunas excepciones existen en el lado de ejecución de RPC y algunas interfaces DCOM utilizadas por el motor son externas).

Dos enfoques típicos para calcular las referencias se han realizado siempre en línea y en la tecnología controlada por datos (interpretada). MIDL admite a través de sus modificadores [**– os**](/windows/desktop/Midl/-os) y [**– OI \***](/windows/desktop/Midl/-oi) en sus códigos auxiliares generados por C. Además, MIDL puede generar las bibliotecas TLB usadas por el paquete oleautomation. En consecuencia, una perspectiva de los elementos internos del motor es que se compone de dos partes.

El primero es un conjunto de rutinas que controlan el tamaño, el cálculo de referencias, etc., que se corresponde con objetos de tipo de datos típicos como una estructura o una matriz. Estas rutinas se ajustan para mejorar el rendimiento; por ejemplo, normalmente intentan bloquear la copia de datos siempre que sea posible. Esta parte se conoce a menudo como el motor NDR principal.

La segunda parte consta de un intérprete y sus elementos relacionados. El intérprete usa rutinas del motor de NDR principal, como si se tratase de una biblioteca interna, para ejecutar una llamada remota con todos sus argumentos calculados y cuyas referencias no se han calculado, según corresponda.

El motor NDR principal se utiliza de forma similar si se utiliza desde código auxiliar en línea o desde el intérprete. Todas las rutinas del motor principal dependen del estado pasado por una estructura de mensaje de código auxiliar. La estructura se configura correctamente mediante el código auxiliar en línea o el intérprete. A lo largo de los años, el motor principal se usaba en un contexto diferente. Actualmente, el intérprete es realmente un conjunto de varios bucles intérprete distintos. Estos se relacionan con los intérpretes antiguos y nuevos ([**– OI**](/windows/desktop/Midl/-oi) frente a las **interfaces**), así como con los bucles relacionados con la serialización de datos (picking), la compatibilidad con RPC Async y la compatibilidad ASINCRÓNICA de DCOM (RPC y DCOM tienen diferentes modelos de programación asincrónica).

Además de agregar nuevas características, un aspecto importante de la evolución del motor de NDR es un cambio general en el enfoque de los intérpretes. La versión 1.1 de NDR comenzó como parte de un nuevo enfoque MIDL 2,0 para la serialización, con el código auxiliar en línea que se prefiere para las consideraciones de rendimiento. Con la versión más reciente de NDR, [**– las interfaces**](/windows/desktop/Midl/-oi) se han convertido en el modo de uso más extendido del compilador, casi a la exclusión de códigos auxiliares en línea.

Los descriptores de cadena de formato del motor NDR de RPC se describen con más detalle en los temas siguientes:

-   [Cadenas de formato](format-strings.md)
-   [Cadenas de formato de procedimiento](procedure-format-strings.md)
-   [Descriptor de encabezado de procedimiento](procedure-header-descriptor.md)
-   [Handles](handles.md)
-   [El encabezado](the-header.md)
-   [Descriptores de parámetros](parameter-descriptors.md)
-   [Cadenas de formato de tipo](type-format-strings.md)

 

 