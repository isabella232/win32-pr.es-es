---
description: En este apéndice se muestra una versión reescrita de las aplicaciones de ejemplo Simplec.c y Simple.c que controla correctamente el código de servidor de cliente habilitado para IPv4 o IPv6.IPv CodeIPv6-Enabled 6.
ms.assetid: ffcbd59e-63ea-4df3-9db9-e7d4634eefeb
title: 'Apéndice B: Código fuente independiente de la versión ip'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37daf34b4a7d46a2fb8fc3cbaf5aed6cf7e054a3fb0147de8d86a643a9e4f59f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741612"
---
# <a name="appendix-b-ip-version-agnostic-source-code"></a>Apéndice B: Código fuente independiente de la versión ip

En este apéndice se muestra una versión reescrita de las aplicaciones de ejemplo Simplec.c y Simple.c que controla correctamente IPv4 o IPv6.

-   [Código de cliente habilitado para IPv6](ipv6-enabled-client-code-2.md)
-   [Código de servidor habilitado para IPv6](ipv6-enabled-server-code-2.md)

Este código ejemplifica las directrices establecidas en esta guía de IPv6 y se incluye para proporcionar código fuente que se ha modificado correctamente para agregar compatibilidad con IPv6. Este ejemplo es intencionadamente sencillo, pero proporciona un ejemplo práctica para la revisión y la revisión. En el Apéndice A: Código fuente solo IPv4 se proporciona una versión de este código fuente solo [IPv4.](appendix-a-ipv4-only-source-code-2.md)

Al comparar el código fuente del Apéndice A (solo IPv4) y el Apéndice B (independiente de la versión ip), se obtiene una idea de los cambios necesarios para modificar la aplicación Windows Sockets para agregar compatibilidad con IPv6.

 

 



