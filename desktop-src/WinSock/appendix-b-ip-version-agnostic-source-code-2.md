---
description: En este apéndice se muestra una versión reescrita de las aplicaciones de ejemplo Simplec. c y simple. c que administran correctamente el código del servidor CodeIPv6-Enabled del cliente de IPv4 o IPv6.
ms.assetid: ffcbd59e-63ea-4df3-9db9-e7d4634eefeb
title: 'Apéndice B: código fuente independiente de la versión de IP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333e344376695122ebcd650ebf2595d70afbf7ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907962"
---
# <a name="appendix-b-ip-version-agnostic-source-code"></a>Apéndice B: código fuente independiente de la versión de IP

En este apéndice se muestra una versión reescrita de las aplicaciones de ejemplo Simplec. c y simple. c que controla correctamente IPv4 o IPv6.

-   [Código de cliente habilitado para IPv6](ipv6-enabled-client-code-2.md)
-   [Código de servidor habilitado para IPv6](ipv6-enabled-server-code-2.md)

Este código ejemplifica las directrices establecidas en esta guía de IPv6 y se incluye para proporcionar el código fuente que se ha modificado correctamente para agregar compatibilidad con IPv6. Este ejemplo es deliberadamente sencillo, pero proporciona un ejemplo práctico para el uso y la revisión. Una versión solo IPv4 de este código fuente se proporciona en el [Apéndice A: código fuente solo IPv4](appendix-a-ipv4-only-source-code-2.md).

Al comparar el código fuente del Apéndice A (solo IPv4) y el Apéndice B (independiente de la versión IP), se obtiene una idea de los cambios necesarios para modificar la aplicación de Windows Sockets para agregar compatibilidad con IPv6.

 

 



