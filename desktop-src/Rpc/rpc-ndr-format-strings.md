---
title: Cadenas de formato RPC RPC
description: Cadenas de formato BAND de llamada a procedimiento remoto (RPC).
ms.assetid: 9c83a039-49d3-491d-8110-29d1548730de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf0569a913d6c5a4b19b342cc288d6a8682dfc4a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473588"
---
# <a name="rpc-ndr-format-strings"></a>Cadenas de formato RPC RPC

## <a name="ndr-engine-32-bit-interpreter"></a>Motor BAND: intérprete de 32 bits

En este documento se describen los descriptores de cadena de formato, a veces denominados MOP, para el motor VEC de 32 bits. En esta sección se describen los cambios asociados a la evolución del intérprete [**–Oi**](/windows/desktop/Midl/-oi) a la capa del intérprete **–Oif,** así como las adiciones relacionadas con las canalizaciones y la compatibilidad asincrónica.

En este documento se describe la tecnología Lenguaje de definición de interfaz de Microsoft (MIDL) actual desde la perspectiva del motor y el motor TECHNOLOGY actual.

## <a name="overview"></a>Información general

El motor COMPOSICIÓN es el motor de serialización de los componentes de llamada a procedimiento remoto (RPC) y DCOM. Controla todos los problemas relacionados con el código auxiliar de una llamada remota. Como proceso, la serialización de JJ está controlada por el código C de códigos auxiliares generados por MIDL, un generador de tipo JIT de MIDL o por códigos auxiliares generados por otras herramientas o escritos manualmente. A su vez, el motor COMPOSICIÓN impulsa el tiempo de ejecución subyacente (DCOM o RPC) que se comunica con transportes específicos.

El objetivo original del diseño había sido proporcionar una herramienta para serializar de forma eficaz los datos arbitrarios, en función de la información proporcionada por el compilador MIDL. Las cadenas de formato que se describen en este documento y, de hecho, toda la información generada por el compilador para el consumo del motor DOCUMENTAR, siempre se han considerado una interfaz interna entre el compilador y el motor. Del mismo modo, las interfaces disponibles para el motor para controlar los problemas en tiempo de ejecución también son principalmente internas (existen algunas excepciones en el lado del tiempo de ejecución de RPC y algunas interfaces DCOM usadas por el motor son externas).

Dos enfoques típicos de serialización siempre han sido la tecnología insertada y controlada por datos (interpretada). MIDL admite tanto a través de sus [**modificadores –Os**](/windows/desktop/Midl/-os) como [**–Oi \***](/windows/desktop/Midl/-oi) en sus códigos auxiliares generados por C. Además, MIDL puede generar las bibliotecas de TLB que usa el paquete oleautomation. En consecuencia, una perspectiva de los elementos internos del motor es que consta de dos partes.

El primero es un conjunto de rutinas que controlan el tamaño, la serialización, y así sucesivamente, correspondientes a objetos de tipo de datos típicos, como una estructura o una matriz. Estas rutinas están ajustadas para mejorar el rendimiento. Por ejemplo, normalmente intentan bloquear la copia de datos siempre que sea posible. A menudo, esta parte se conoce como el motor MOTOR principal.

La segunda parte consta de un intérprete y sus partes relacionadas. El intérprete usa rutinas del motor VMM básico, como si fuera de una biblioteca interna, para ejecutar una llamada remota con todos sus argumentos serializados y sin marmar, según corresponda.

El motor LEJOS principal se usa de forma similar tanto si se usa desde código auxiliar en línea como desde el intérprete. Todas las rutinas principales del motor dependen del estado pasado por una estructura de mensajes de código auxiliar. La estructura se configura correctamente mediante el código auxiliar en línea o el intérprete. A lo largo de los años, el motor principal se había usado en un contexto diferente. actualmente, el intérprete es realmente un conjunto de varios bucles de intérprete distintos. Están relacionados con los intérpretes antiguos y nuevos ([**–Oi**](/windows/desktop/Midl/-oi) frente a **–Oif),** así como con bucles relacionados con la serialización de datos (pickling), la compatibilidad asincrónica de RPC y la compatibilidad asincrónica con DCOM (RPC y DCOM tienen diferentes modelos de programación asincrónica).

Más allá de la adición de nuevas características, un aspecto importante de la evolución del motor VERT es un cambio general en el enfoque de los intérpretes. La versión NTE 1.1 comenzó como parte de un nuevo enfoque midl 2.0 para serializar, con el código auxiliar en línea preferido para las consideraciones de rendimiento. Con la versión más reciente de INSERT, [**–Oif**](/windows/desktop/Midl/-oi) se ha convertido en el modo más usado del compilador, casi hasta la exclusión de códigos auxiliares en línea.

Los descriptores de cadena de formato del motor RPC RPC se describen con más detalle en los temas siguientes:

-   [Cadenas de formato](format-strings.md)
-   [Cadenas de formato de procedimiento](procedure-format-strings.md)
-   [Descriptor de encabezado de procedimiento](procedure-header-descriptor.md)
-   [Asas](handles.md)
-   [Encabezado](the-header.md)
-   [Descriptores de parámetros](parameter-descriptors.md)
-   [Cadenas de formato de tipo](type-format-strings.md)

 

 