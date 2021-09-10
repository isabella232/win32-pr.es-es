---
title: Acerca de las funciones y macros de AVIFile
description: Acerca de las funciones y macros de AVIFile
ms.assetid: 877f6759-8271-47eb-8a7f-540393e5ae89
keywords:
- Función AVIFileInit
- Función AVIFileExit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f66bbac900b69841fd7cba814aad339731b75727
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369844"
---
# <a name="about-avifile-functions-and-macros"></a>Acerca de las funciones y macros de AVIFile

Las funciones y macros AVIFile controlan la información de los archivos basados en el tiempo como uno o varios flujos de datos en lugar de *bloques etiquetados* de datos denominados fragmentos. Los flujos de datos hacen referencia a los componentes de un archivo basado en el tiempo. Un archivo AVI puede contener varios tipos diferentes de datos, como una secuencia de vídeo, un inglés y un francés. Con AVIFile, una aplicación puede acceder a cada uno de estos componentes por separado.

> [!Note]  
> Aunque las funciones y macros AVIFile funcionan con cualquier archivo RIFF, esta información general muestra su uso solo con archivos AVI. Los archivos AVI suelen ser los archivos basados en el tiempo que se usan con las macros y funciones AVIFile.

 

Las funciones y macros AVIFile están contenidas en una biblioteca de vínculos dinámicos. Para inicializar la biblioteca, use la [**función AVIFileInit.**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) Después de inicializar la biblioteca, puede usar cualquiera de las funciones o macros AVIFile. Para liberar la biblioteca, use la [**función AVIFileExit.**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) AVIFile mantiene un recuento de referencias de las aplicaciones que usan la biblioteca, pero no de las que la han publicado. Las aplicaciones deben equilibrar cada uso de **AVIFileInit** con una llamada a **AVIFileExit** para liberar completamente la biblioteca una vez que cada aplicación termina de usarla.

 

 




