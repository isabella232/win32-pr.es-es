---
description: Los reconocedores creados para su uso con Windows Vista y Windows XP Tablet PC Edition usan un conjunto de estructuras, cada una de las cuales se denomina lattice, para devolver los resultados del reconocimiento a las bibliotecas de plataforma de Tablet PC.
ms.assetid: 628ca677-31eb-47d9-bcc6-d7777f8aaf7c
title: Recognizer Lattice (estructura)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46bbfe71674571ae0554509dfa8477569ef8b44d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467161"
---
# <a name="recognizer-lattice-structure"></a>Recognizer Lattice (estructura)

Los reconocedores creados para su uso con Windows Vista y Windows XP Tablet PC Edition usan un conjunto de estructuras, cada una de las cuales se denomina lattice, para devolver los resultados del reconocimiento a las bibliotecas de plataforma de Tablet PC. A continuación, la plataforma de Tablet PC copia la información de estas estructuras en el objeto [**IInkRecognitionResult,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) la colección [**IInkRecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) y el [**objeto IInkRecognitionAlternate.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate)

El reconocedor debe devolver un puntero al lattice cuando la plataforma llama a la función [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr) en el [identificador HRECOCONTEXT.](hrecocontext-handle.md)

En esta sección se describe la estructura lattice en detalle. Para obtener información general sobre los reconocedores y los conceptos relacionados, vea [Acerca del reconocimiento de escritura a mano.](about-handwriting-recognition.md)

## <a name="the-need-for-a-lattice"></a>La necesidad de un lattice

Un reconocedor puede encontrar varias maneras de dividir un conjunto de trazos de lápiz en segmentos de reconocimiento. Lo que el reconocedor usa como segmento de reconocimiento depende del tipo de reconocedor. Los reconocedores de idioma inglés suelen usar palabras como segmento de reconocimiento. Otros reconocedores pueden usar caracteres, formas o gestos como segmento de reconocimiento. La flexibilidad de las estructuras lattice permite la administración lógica del gran número de resultados de reconocimiento que se pueden combinar en relaciones complejas.

Internamente, los reconocedores usan un entramado para contener unidades de reconocimiento básicas para un fragmento de lápiz determinado. El lattice también contiene la puntuación, o nivel de confianza, del resultado combinado. Además, la celosía almacena la asignación de segmentos a los trazos de entrada de lápiz originales.

Las estructuras lattice se definen en el archivo de encabezado RecTypes.h. Las estructuras lattice incluyen las siguientes estructuras:

-   [**RECO \_ LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)
-   [**RECO \_ LATTICE \_ COLUMN**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)
-   [**RECO \_ LATTICE, \_ ELEMENTO**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)
-   [**PROPIEDADES \_ DE RECO LATTICE \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties)
-   [**RECO \_ LATTICE, \_ PROPIEDAD**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)

## <a name="lattice-components"></a>Componentes de Lattice

En los ejemplos siguientes se usan los trazos de la palabra "juntos", como se muestra en la siguiente imagen. En los ejemplos, los segmentos se evalúan como una o varias palabras. Los números representan los trazos individuales del segmento que se está evaluando. Tenga en cuenta que cada uno de los caracteres "t" contiene dos trazos.

![trazos para la palabra "together"](images/1d5fa9fb-6c38-49b8-8caa-2b6dcc1d5dec.gif)

Un entramado se compone de una o varias columnas, una para cada segmento. A su vez, cada columna contiene uno o varios elementos. Un elemento contiene una alternativa de reconocimiento discreto. Para más información sobre las columnas, consulte la [**estructura RECO \_ LATTICE \_ COLUMN.**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column) Para obtener más información sobre los elementos, vea [**la estructura RECO \_ LATTICE \_ ELEMENT.**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)

El reconocedor podría devolver un único segmento al evaluar la muestra de entrada de lápiz que se muestra en el ejemplo anterior. En este caso, la celosía contiene una sola columna con un solo elemento.

Un ejemplo más complejo se presenta cuando el reconocedor evalúa la muestra de entrada de lápiz y presenta varios segmentos y varias alternativas para cada segmento.

El número de alternativas de reconocimiento puede ser escalonado, incluso para una pequeña muestra de lápiz. Por ejemplo, "t o g e t h e r" puede producir los siguientes resultados:

-   "para obtenerla" (más alternativas para cada palabra)
-   "para recopilar" (más alternativas para cada palabra)
-   "to got her" (plus alternates for each word)
-   "together" (más alternativas para la palabra)

En este caso, un reconocedor podría crear la siguiente estructura lattice.

![estructura de lattice para la palabra "together"](images/2496c3dd-8b08-4f86-9fe3-f118be49a8c8.gif)

> [!Note]  
> Cada columna comparte el mismo orden de trazo porque todas hacen referencia a la misma [colección InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))

 

 

 
