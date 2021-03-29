---
title: The Component Object Model [Modelo de objetos componentes (COM)]
description: The Component Object Model [Modelo de objetos componentes (COM)]
ms.assetid: f5f66603-466c-496b-be29-89a8ed9361dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786a4bef59401877f642273ba7a97756232ac083
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773573"
---
# <a name="the-component-object-model"></a>The Component Object Model [Modelo de objetos componentes (COM)]

El modelo de objetos componentes (COM) de Microsoft es un sistema independiente de la plataforma, distribuido y orientado a objetos para crear componentes de software binarios que pueden interactuar. COM es la tecnología básica de OLE (documentos compuestos) de Microsoft, ActiveX (componentes habilitados para Internet), así como otros.

Para entender COM (y, por tanto, todas las tecnologías basadas en COM), es fundamental entender que no es un lenguaje orientado a objetos sino un estándar. Tampoco especifica cómo se debe estructurar una aplicación. el lenguaje, la estructura y los detalles de implementación se dejan al desarrollador de la aplicación. En su lugar, COM especifica un modelo de objetos y los requisitos de programación que permiten a los objetos COM (también denominados componentes COM, o a veces simplemente *objetos*) interactuar con otros objetos. Estos objetos pueden estar dentro de un único proceso, en otros procesos, e incluso pueden estar en equipos remotos. Pueden escribirse en lenguajes diferentes y pueden ser estructuralmente bastante diferentes, por lo que COM se conoce como *estándar binario*. estándar que se aplica después de que un programa se haya traducido al código de máquina binaria.

El único requisito de lenguaje para COM es que el código se genere en un lenguaje que pueda crear estructuras de punteros y, ya sea de forma explícita o implícita, llamar a funciones a través de punteros. Los lenguajes orientados a objetos como C++ y Smalltalk proporcionan mecanismos de programación que simplifican la implementación de objetos COM, pero se pueden usar lenguajes como C, Java y VBScript para crear y usar objetos COM.

COM define la naturaleza esencial de un objeto COM. En general, un objeto de software se compone de un conjunto de datos y de las funciones que manipulan los datos. Un objeto COM es aquél en el que el acceso a los datos de un objeto se consigue exclusivamente a través de uno o más conjuntos de funciones relacionadas. Estos conjuntos de funciones se denominan *interfaces* y las funciones de una interfaz se denominan *métodos*. Además, COM requiere que la única manera de obtener acceso a los métodos de una interfaz sea a través de un puntero a la interfaz.

Además de especificar el estándar del objeto binario básico, COM define ciertas interfaces básicas que proporcionan funciones comunes a todas las tecnologías basadas en COM y proporciona un número pequeño de funciones que todos los componentes requieren. COM también define cómo funcionan conjuntamente los objetos en un entorno distribuido y se han agregado características de seguridad para ayudar a proporcionar integridad del sistema y de los componentes.

En los siguientes temas de esta sección se describen los problemas básicos de COM relacionados con el diseño de objetos COM:

-   [Objetos e interfaces COM](com-objects-and-interfaces.md)
-   [Usar e implementar IUnknown](using-and-implementing-iunknown.md)
-   [Reutilizar objetos](reusing-objects.md)
-   [Biblioteca COM](the-com-library.md)
-   [Administrar la asignación de memoria](managing-memory-allocation.md)

 

 




