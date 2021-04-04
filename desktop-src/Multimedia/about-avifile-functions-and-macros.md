---
title: Acerca de las funciones y macros de AVIFile
description: Acerca de las funciones y macros de AVIFile
ms.assetid: 877f6759-8271-47eb-8a7f-540393e5ae89
keywords:
- AVIFileInit función)
- AVIFileExit función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f66bbac900b69841fd7cba814aad339731b75727
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076334"
---
# <a name="about-avifile-functions-and-macros"></a>Acerca de las funciones y macros de AVIFile

Las funciones y macros de AVIFile controlan la información de los archivos basados en tiempo como uno o varios *flujos de datos* en lugar de los bloques etiquetados de los datos denominados fragmentos. Los flujos de datos hacen referencia a los componentes de un archivo basado en el tiempo. Un archivo AVI puede contener varios tipos diferentes de datos, como una secuencia de vídeo, una banda sonora en inglés y una banda sonora en francés. Con AVIFile, una aplicación puede tener acceso a cada uno de estos componentes por separado.

> [!Note]  
> Aunque las funciones y macros de AVIFile funcionan con cualquier archivo RIFF, en esta información general solo se muestra su uso con archivos AVI. Los archivos AVI suelen ser los archivos basados en el tiempo que se usan con las macros y funciones de AVIFile.

 

Las funciones y macros de AVIFile se encuentran en una biblioteca de vínculos dinámicos. Para inicializar la biblioteca, utilice la función [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) . Después de inicializar la biblioteca, puede utilizar cualquiera de las funciones o macros de AVIFile. Para liberar la biblioteca, utilice la función [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) . AVIFile mantiene un recuento de referencias de las aplicaciones que usan la biblioteca, pero no las que la han liberado. Las aplicaciones deben equilibrar cada uso de **AVIFileInit** con una llamada a **AVIFileExit** para liberar por completo la biblioteca después de que cada aplicación termine de usarla.

 

 




