---
title: The Component Object Model [Modelo de objetos componentes (COM)]
description: The Component Object Model [Modelo de objetos componentes (COM)]
ms.assetid: f5f66603-466c-496b-be29-89a8ed9361dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ad81adeaf41670468dd41bbf344a3fd7358c14f4b3cbeb2e482812a083ecfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462345"
---
# <a name="the-component-object-model"></a>The Component Object Model [Modelo de objetos componentes (COM)]

Microsoft Component Object Model (COM) es un sistema orientado a objetos, distribuido e independiente de la plataforma para crear componentes de software binarios que pueden interactuar. COM es la tecnología fundamental para ole de Microsoft (documentos compuestos), ActiveX (componentes habilitados para Internet), así como otros.

Para comprender COM (y, por tanto, todas las tecnologías basadas en COM), es fundamental entender que no es un lenguaje orientado a objetos, sino un estándar. COM tampoco especifica cómo se debe estructurar una aplicación; Los detalles de lenguaje, estructura e implementación se deja al desarrollador de la aplicación. En su lugar, COM especifica un modelo de objetos y requisitos de programación que permiten que los objetos COM (también denominados componentes COM o, a veces, simplemente objetos *)* interactúen con otros objetos. Estos objetos pueden estar dentro de un único proceso, en otros procesos e incluso pueden estar en equipos remotos. Se pueden escribir en distintos lenguajes y pueden ser estructuralmente bastante diferentes, por lo que SE HACE referencia a COM como un *estándar binario*; un estándar que se aplica después de que un programa se haya traducido al código de máquina binario.

El único requisito de lenguaje para COM es que el código se genera en un lenguaje que puede crear estructuras de punteros y, de forma explícita o implícita, llamar a funciones a través de punteros. Los lenguajes orientados a objetos, como C++ y Smalltalk, proporcionan mecanismos de programación que simplifican la implementación de objetos COM, pero se pueden usar lenguajes como C, Java y VBScript para crear y usar objetos COM.

COM define la naturaleza esencial de un objeto COM. En general, un objeto de software se forma de un conjunto de datos y las funciones que manipulan los datos. Un objeto COM es en el que el acceso a los datos de un objeto se logra exclusivamente a través de uno o varios conjuntos de funciones relacionadas. Estos conjuntos de funciones se *denominan interfaces* y las funciones de una interfaz se denominan *métodos*. Además, COM requiere que la única manera de obtener acceso a los métodos de una interfaz sea a través de un puntero a la interfaz .

Además de especificar el estándar de objeto binario básico, COM define determinadas interfaces básicas que proporcionan funciones comunes a todas las tecnologías basadas en COM y proporciona un pequeño número de funciones que requieren todos los componentes. COM también define cómo funcionan conjuntamente los objetos en un entorno distribuido y ha agregado características de seguridad para ayudar a proporcionar integridad del sistema y los componentes.

En los temas siguientes de esta sección se describen los problemas com básicos relacionados con el diseño de objetos COM:

-   [Objetos COM e interfaces](com-objects-and-interfaces.md)
-   [Uso e implementación de IUnknown](using-and-implementing-iunknown.md)
-   [Volver ausar objetos](reusing-objects.md)
-   [La biblioteca COM](the-com-library.md)
-   [Administración de la asignación de memoria](managing-memory-allocation.md)

 

 




