---
description: Una aplicación habilitada para tinta se comunica con el sistema de reconocimiento a través de las API de la plataforma de Tablet PC.
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: Arquitectura de la API de reconocimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72838b77e11092cacd4adb998c669167940ecad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568243"
---
# <a name="recognition-api-architecture"></a>Arquitectura de la API de reconocimiento

Una aplicación habilitada para tinta se comunica con el sistema de reconocimiento a través de las API de la plataforma de Tablet PC. Las aplicaciones utilizan el objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) para lograr esto. La plataforma de Tablet PC interactúa con el reconocedor mediante el uso de las interfaces de estilo C que se documentan en esta sección. En la ilustración siguiente, el área dentro de la línea discontinua muestra lo que se documenta en esta sección.

![Ilustración de la arquitectura de reconocimiento con el reconocedor resaltado](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

Un reconocedor personalizado debe incluir recapitulais. h (se instala de forma predeterminada en C: \\ archivos de programa \\ Microsoft Tablet PC Platform SDK \\ include). Excepto en los casos en los que se indique, la biblioteca de vínculos dinámicos (DLL) debe exportar todas las funciones de la API, incluso si elige que algunos devuelvan E \_ NOTIMPL.

En ningún caso, el reconocedor será llamado directamente por una aplicación habilitada para tinta. En su lugar, las aplicaciones llamarán a las API de automatización o a las API administradas para obtener los resultados del reconocedor.

 

 



