---
title: The Component Object Model [Modelo de objetos componentes (COM)]
description: The Component Object Model [Modelo de objetos componentes (COM)]
ms.assetid: f5f66603-466c-496b-be29-89a8ed9361dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786a4bef59401877f642273ba7a97756232ac083
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253124"
---
# <a name="the-component-object-model"></a>The Component Object Model [Modelo de objetos componentes (COM)]

El Modelo de objetos componentes (COM) de Microsoft es un sistema orientado a objetos, distribuido y independiente de la plataforma para crear componentes de software binarios que pueden interactuar. COM es la tecnología fundamental para ole de Microsoft (documentos compuestos), ActiveX (componentes habilitados para Internet), así como otros.

Para comprender COM (y, por tanto, todas las tecnologías basadas en COM), es fundamental entender que no es un lenguaje orientado a objetos, sino un estándar. COM tampoco especifica cómo se debe estructurar una aplicación; Los detalles de lenguaje, estructura e implementación se quedan al desarrollador de la aplicación. En su lugar, COM especifica un modelo de objetos y requisitos de programación que permiten a los objetos COM (también denominados componentes COM o, a veces, simplemente objetos *)* interactuar con otros objetos. Estos objetos pueden estar dentro de un único proceso, en otros procesos, e incluso pueden estar en equipos remotos. Se pueden escribir en distintos lenguajes y pueden ser estructuralmente bastante diferentes, por lo que COM se conoce como *estándar binario*; un estándar que se aplica después de que un programa se haya traducido al código de máquina binario.

El único requisito de lenguaje para COM es que el código se genera en un lenguaje que puede crear estructuras de punteros y, de forma explícita o implícita, llamar a funciones a través de punteros. Los lenguajes orientados a objetos, como C++ y Smalltalk, proporcionan mecanismos de programación que simplifican la implementación de objetos COM, pero se pueden usar lenguajes como C, Java y VBScript para crear y usar objetos COM.

COM define la naturaleza esencial de un objeto COM. En general, un objeto de software se forma de un conjunto de datos y las funciones que manipulan los datos. Un objeto COM es uno en el que el acceso a los datos de un objeto se logra exclusivamente a través de uno o varios conjuntos de funciones relacionadas. Estos conjuntos de funciones se *denominan interfaces* y las funciones de una interfaz se denominan *métodos*. Además, COM requiere que la única manera de obtener acceso a los métodos de una interfaz sea a través de un puntero a la interfaz .

Además de especificar el estándar de objetos binarios básicos, COM define ciertas interfaces básicas que proporcionan funciones comunes a todas las tecnologías basadas en COM y proporciona un pequeño número de funciones que requieren todos los componentes. COM también define cómo funcionan conjuntamente los objetos en un entorno distribuido y ha agregado características de seguridad para ayudar a proporcionar integridad del sistema y los componentes.

En los temas siguientes de esta sección se describen los problemas com básicos relacionados con el diseño de objetos COM:

-   [Objetos COM e interfaces](com-objects-and-interfaces.md)
-   [Uso e implementación de IUnknown](using-and-implementing-iunknown.md)
-   [Volver a hacer lausación de objetos](reusing-objects.md)
-   [La biblioteca COM](the-com-library.md)
-   [Administración de la asignación de memoria](managing-memory-allocation.md)

 

 




