---
title: Procedimiento de compilación general
description: Página de navegación para el proceso de creación de una aplicación cliente/servidor mediante llamada a procedimiento remoto (RPC).
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8402a14ceac3b34114e7b40998038a4e09fb7ba1a915c173f2062f7fab9e63d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929642"
---
# <a name="general-build-procedure"></a>Procedimiento de compilación general

El proceso para crear una aplicación cliente/servidor mediante RPC de Microsoft es:

-   Desarrolle la interfaz .
-   Desarrolle el servidor que implementa la interfaz .
-   Desarrolle el cliente que usa la interfaz .

En la ilustración siguiente se muestran estos pasos.

![proceso para crear una aplicación cliente-servidor mediante microsoft rpc](images/appdev.png)

Es factible y común desarrollar las aplicaciones cliente y servidor simultáneamente. Sin embargo, dado que los programas de cliente y de servidor dependen de la interfaz, la interfaz entre ellos debe desarrollarse antes de desarrollar el cliente y el servidor, como se muestra en el diagrama anterior.

En esta sección se deberán seguir los pasos necesarios para compilar una aplicación cliente/servidor con RPC. La información se presenta en los temas siguientes:

-   [Desarrollo de la interfaz](developing-the-interface.md)
-   [Desarrollo del servidor](developing-the-server.md)
-   [Desarrollo del cliente](developing-the-client.md)

 

 




