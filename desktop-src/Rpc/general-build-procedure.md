---
title: Procedimiento de compilación general
description: Página de navegación para el proceso de creación de una aplicación cliente/servidor mediante la llamada a procedimiento remoto (RPC).
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b223bf7482cd7cbb65f5b737c90502a6b6dd3de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075597"
---
# <a name="general-build-procedure"></a>Procedimiento de compilación general

El proceso para crear una aplicación cliente/servidor mediante Microsoft RPC es el siguiente:

-   Desarrolle la interfaz.
-   Desarrolle el servidor que implementa la interfaz.
-   Desarrolle el cliente que utiliza la interfaz.

En la ilustración siguiente se muestran estos pasos.

![proceso para crear una aplicación cliente-servidor mediante Microsoft RPC](images/appdev.png)

Es factible y común desarrollar las aplicaciones cliente y servidor simultáneamente. Dado que los programas cliente y servidor dependen de la interfaz, sin embargo, la interfaz entre ellos debe desarrollarse antes de que se desarrollen el cliente y el servidor, tal como se muestra en el diagrama anterior.

En esta sección se describen los pasos necesarios para crear una aplicación cliente/servidor con RPC. La información se presenta en los temas siguientes:

-   [Desarrollo de la interfaz](developing-the-interface.md)
-   [Desarrollo del servidor](developing-the-server.md)
-   [Desarrollo del cliente](developing-the-client.md)

 

 




