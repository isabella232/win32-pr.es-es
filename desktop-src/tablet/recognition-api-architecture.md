---
description: Una aplicación habilitada para lápiz se comunica con el sistema de reconocimiento a través de las API de la plataforma de Tablet PC.
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: Arquitectura de API de reconocimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59775658bcda2ecafd142476e6ff48ccdda2e82b31af62d5f49b218513f9b326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966903"
---
# <a name="recognition-api-architecture"></a>Arquitectura de API de reconocimiento

Una aplicación habilitada para lápiz se comunica con el sistema de reconocimiento a través de las API de la plataforma de Tablet PC. Las aplicaciones usan [**el objeto IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) para lograr esto. Tablet PC Platform interactúa con el reconocedor mediante las interfaces de estilo C que se documentan en esta sección. En la ilustración siguiente, el área dentro de la línea discontinua muestra lo que se documenta en esta sección.

![ilustración de la arquitectura de reconocimiento con el reconocedor resaltado](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

Un reconocedor personalizado debe incluir Recapis.h (instalado de forma predeterminada en C: Archivos de programa Microsoft \\ Tablet PC Platform SDK \\ \\ Include). Excepto donde se indica, la biblioteca de vínculos dinámicos (DLL) debe exportar todas las funciones de API, incluso si decide que algunas de ellas devuelvan E \_ NOTIMPL.

En ningún caso, una aplicación habilitada para lápiz llamará directamente al reconocedor. En su lugar, las aplicaciones llamarán a las API de Automation o a las API administradas para obtener resultados del reconocedor.

 

 



