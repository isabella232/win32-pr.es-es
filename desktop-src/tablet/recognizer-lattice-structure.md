---
description: Los reconocedores creados para su uso con Windows Vista y Windows XP Tablet PC Edition usan un conjunto de estructuras, cada una de las cuales se denomina Lattice, para devolver los resultados de reconocimiento a las bibliotecas de plataforma de Tablet PC.
ms.assetid: 628ca677-31eb-47d9-bcc6-d7777f8aaf7c
title: Estructura Lattice del reconocedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46bbfe71674571ae0554509dfa8477569ef8b44d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551251"
---
# <a name="recognizer-lattice-structure"></a>Estructura Lattice del reconocedor

Los reconocedores creados para su uso con Windows Vista y Windows XP Tablet PC Edition usan un conjunto de estructuras, cada una de las cuales se denomina Lattice, para devolver los resultados de reconocimiento a las bibliotecas de plataforma de Tablet PC. A continuación, la plataforma de Tablet PC copia la información de estas estructuras en el objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) , la colección [**IInkRecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) y el objeto [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) .

El reconocedor debe devolver un puntero a Lattice cuando la plataforma llama a la función [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr) en el identificador [HRECOCONTEXT](hrecocontext-handle.md) .

En esta sección se describe la estructura de Lattice en detalle. Para obtener información general sobre los reconocedores y los conceptos relacionados, consulte [acerca del reconocimiento de escritura a mano](about-handwriting-recognition.md).

## <a name="the-need-for-a-lattice"></a>La necesidad de un Lattice

Un reconocedor puede encontrar varias formas de dividir un conjunto de trazos de tinta en segmentos de reconocimiento. Lo que el reconocedor utiliza como segmento de reconocimiento depende del tipo de reconocedor. Los reconocedores de idiomas ingleses suelen usar palabras como el segmento de reconocimiento. Otros reconocedores pueden usar caracteres, formas o gestos como segmento de reconocimiento. La flexibilidad de las estructuras Lattice permite la administración lógica del gran número de resultados de reconocimiento que se pueden combinar en relaciones complejas.

Internamente, los reconocedores usan un Lattice para mantener las unidades de reconocimiento básicas para un determinado fragmento de tinta. El Lattice también contiene la puntuación o el nivel de confianza del resultado combinado. Además, el Lattice almacena la asignación de segmentos a los trazos de tinta originales.

Las estructuras Lattice se definen en el archivo de encabezado RecTypes. h. Las estructuras Lattice incluyen las siguientes estructuras:

-   [**RECU \_ LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)
-   [**RECU \_ LATTICE \_ columna**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)
-   [**\_elemento LATTICE de recu \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)
-   [**propiedades de recu \_ LATTICE \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties)
-   [**\_propiedad LATTICE de recu \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)

## <a name="lattice-components"></a>Componentes de Lattice

En los ejemplos siguientes se usan los trazos de la palabra "juntos", tal como se muestra en la siguiente imagen. En los ejemplos, los segmentos se evalúan como una o varias palabras. Los números representan los trazos individuales del segmento que se está evaluando. Tenga en cuenta que cada uno de los caracteres "t" contiene dos trazos.

![trazos de la palabra "juntos"](images/1d5fa9fb-6c38-49b8-8caa-2b6dcc1d5dec.gif)

Un Lattice se compone de una o más columnas, una para cada segmento. Cada columna a su vez contiene uno o más elementos. Un elemento contiene una alternativa de reconocimiento discreto. Para obtener más información sobre las columnas, vea la estructura de [**\_ \_ columnas de recu LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column) . Para obtener más información sobre los elementos, vea la estructura del [**\_ \_ elemento recu LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element) .

El reconocedor puede devolver un solo segmento al evaluar el ejemplo de entrada de lápiz que se muestra en el ejemplo anterior. En este caso, Lattice contiene una sola columna con un solo elemento.

Un ejemplo más complejo se presenta cuando el reconocedor evalúa el ejemplo de entrada de lápiz y aparece con varios segmentos y varias alternativas para cada segmento.

El número de alternativas de reconocimiento puede ser escalonado, incluso para un ejemplo de tinta pequeña. Por ejemplo, "t o g e t h e r" puede producir los siguientes resultados:

-   "para obtener" (más alternativas para cada palabra)
-   "para recopilar" (más alternativas para cada palabra)
-   "para obtenerlo" (más alternativas para cada palabra)
-   "juntos" (más alternativas para la palabra)

En este caso, un reconocedor podría crear la siguiente estructura Lattice.

![Lattice estructura de la palabra "juntos"](images/2496c3dd-8b08-4f86-9fe3-f118be49a8c8.gif)

> [!Note]  
> Cada columna comparte el mismo orden de trazos porque hacen referencia a la misma colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

 

 

 
