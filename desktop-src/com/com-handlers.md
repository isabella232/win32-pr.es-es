---
title: Controladores COM
description: El propósito de los controladores COM es proporcionar algunos \ 0034;smart \ 0034; código en el espacio de direcciones de cliente que puede optimizar las llamadas entre un cliente y un servidor. Los controladores pueden invalidar algunas interfaces mientras delegan otras directamente en el servidor (a través del proxy).
ms.assetid: 390b0228-4c52-453c-82d8-466600d23a04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22409cd7e2b02bbfa0cc988b062d3417f448c75e41f1970af2cb3ddf5c0ffb6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048483"
---
# <a name="com-handlers"></a>Controladores COM

El propósito de los controladores COM es proporcionar código "inteligente" en el espacio de direcciones de cliente que pueda optimizar las llamadas entre un cliente y un servidor. Los controladores pueden invalidar algunas interfaces mientras delegan otras directamente en el servidor (a través del proxy).

Hay dos tipos de controladores COM:

-   [El controlador OLE](the-ole-handler.md) es un archivo DLL pesado que proporciona servicios importantes para vincular e insertar. Normalmente se crea antes de iniciar el servidor y se inicializa para que el servidor se active cuando el objeto incrustado entra en estado de ejecución.
-   [El controlador ligero del lado cliente](the-lightweight-client-side-handler.md) se puede crear para cualquier propósito, puede ser muy pequeño y no se puede crear antes del servidor.

 

 




