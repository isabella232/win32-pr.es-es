---
description: La tunelización automática con direcciones compatibles con IPv4 y 6to4 funcionan a través de una ruta para un prefijo que está en el vínculo a la interfaz \# 2. Los bits 32 que siguen al prefijo se extraen y se usan como una dirección de destino IPv4 para el paquete encapsulado.
ms.assetid: 92261a1b-2b7f-4a76-b98a-2631dc303618
title: Tunelización automática IPv6 y 6to4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede1179902a7ec3276058e078d56e069603e54a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715141"
---
# <a name="ipv6-automatic-tunneling-and-6to4"></a>Tunelización automática IPv6 y 6to4

La tunelización automática con direcciones compatibles con IPv4 y 6to4 funcionan a través de una ruta para un prefijo que está en el vínculo a la interfaz \# 2. Los bits 32 que siguen al prefijo se extraen y se usan como una dirección de destino IPv4 para el paquete encapsulado.

La tunelización automática usa el prefijo::/96, que está habilitado de forma predeterminada. Puede deshabilitarse quitando la ruta de::/96.

6to4 usa el prefijo 2002::/16, que no está habilitado de forma predeterminada.

 

 



