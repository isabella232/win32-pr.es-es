---
title: Diferencias entre las implementaciones de archivos independientes y compuestos
description: La implementación independiente de las interfaces del conjunto de propiedades y la implementación de archivos compuestos difiere de algunas maneras.
ms.assetid: 650d4759-a58a-47a4-922d-5757e356cf56
keywords:
- IPropertyStorage Strctd STG, implementaciones
- IPropertyStorage Strctd STG, implementaciones, diferencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 988f8a9cfdaca0a131bedf98cd8ff10ae8b89525
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903375"
---
# <a name="differences-between-stand-alone-and-compound-file-implementations"></a>Diferencias entre las implementaciones de archivos independientes y compuestos

La implementación independiente de las interfaces del conjunto de propiedades y la implementación de archivos compuestos difiere de algunas maneras. En la implementación de archivo compuesto de secuencias, almacenamiento, almacenamiento de conjuntos de propiedades y objetos de almacenamiento de propiedades, las diversas interfaces se coordinan entre sí porque comparten una implementación común. En la implementación independiente, las implementaciones de interfaz son distintas.

Como resultado, la implementación de archivo compuesto controla los problemas de simultaneidad y sincroniza el objeto de conjunto de propiedades con el objeto de almacenamiento o de secuencia. Con la implementación independiente, el cliente es responsable de controlar los problemas de simultaneidad y sincronización entre el almacenamiento o el objeto de flujo y el conjunto de propiedades. Un cliente puede cumplir estos requisitos siguiendo dos reglas simples. En primer lugar, Nunca manipule un conjunto de propiedades mediante sus interfaces de flujo o de almacenamiento mientras un objeto de almacenamiento de propiedades está abierto en él. En segundo lugar, llame siempre a **commit** en un objeto de almacenamiento de propiedades antes de llamar a **CopyTo**, **MoveElementTo** o **commit** en un objeto de almacenamiento antecesor. En concreto, los siguientes elementos requieren atención del cliente:

-   En la implementación de archivo compuesto, un único mecanismo proporciona protección de simultaneidad para el objeto de almacenamiento y sus objetos de conjunto de propiedades asociados. Sin embargo, en la implementación independiente, la implementación del objeto de almacenamiento es independiente de la implementación del conjunto de propiedades y cada una proporciona sus propios mecanismos de simultaneidad. Por lo tanto, en la implementación independiente, el cliente es responsable de mantener la protección de simultaneidad entre las dos implementaciones a través de un mecanismo de exclusión mutua.
-   En la implementación de archivo compuesto, los cambios en los conjuntos de propiedades se almacenan en búfer en una caché de conjunto de propiedades. Después, cuando se llama al método [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) en el objeto de almacenamiento, la implementación de archivos compuestos vacía automáticamente los cambios del conjunto de propiedades del búfer del conjunto de propiedades antes de que se confirme el objeto de almacenamiento. Por lo tanto, los cambios del conjunto de propiedades se hacen visibles como parte de la transacción que se confirma.

    En la implementación independiente, el cliente debe vaciar explícitamente el búfer del conjunto de propiedades mediante una llamada a [**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) antes de llamar al método [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) en el almacenamiento. Como alternativa, el cliente puede utilizar el nuevo \_ valor no almacenado en búfer de PROPSETFLAG en la implementación independiente para escribir directamente en el conjunto de propiedades en lugar de almacenar en caché los cambios en el búfer interno del conjunto de propiedades. Si \_ se utiliza PROPSETFLAG sin almacenar en búfer, se cumplen automáticamente las responsabilidades del cliente. La implementación de archivo compuesto no admite el valor de PROPSETFLAG no \_ almacenado en búfer. Para obtener más información, vea [**constantes PROPSETFLAG**](propsetflag-constants.md).

-   Al igual que con los almacenamientos con transacciones, la implementación de archivo compuesto actualiza el conjunto de propiedades vaciando su búfer interno antes de ejecutar una llamada a [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) o [**IStorage:: MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto). Por lo tanto, los cambios realizados en el conjunto de propiedades se reflejan en el elemento de almacenamiento copiado o que se ha cambiado.

    En la implementación independiente, el cliente debe vaciar explícitamente el búfer del conjunto de propiedades mediante una llamada a [**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) antes de llamar a [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) o [**IStorage:: MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto). Como alternativa, el cliente puede utilizar el nuevo valor no almacenado en búfer de PROPSETFLAG \_ para escribir directamente en el conjunto de propiedades en lugar de almacenar en caché los cambios en el búfer del conjunto de propiedades. Para obtener más información, vea [**constantes PROPSETFLAG**](propsetflag-constants.md).

 

 




