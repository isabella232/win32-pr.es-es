---
description: La tunelización automática con direcciones compatibles con IPv4 y 6to4 funcionan a través de una ruta para un prefijo que está en el vínculo a la interfaz \# 2. Los 32 bits siguientes al prefijo se extraen y se usan como dirección de destino IPv4 para el paquete encapsulado.
ms.assetid: 92261a1b-2b7f-4a76-b98a-2631dc303618
title: Tunelización automática IPv6 y 6to4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede1179902a7ec3276058e078d56e069603e54a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568133"
---
# <a name="ipv6-automatic-tunneling-and-6to4"></a>Tunelización automática IPv6 y 6to4

La tunelización automática con direcciones compatibles con IPv4 y 6to4 funcionan a través de una ruta para un prefijo que está en el vínculo a la interfaz \# 2. Los 32 bits siguientes al prefijo se extraen y se usan como dirección de destino IPv4 para el paquete encapsulado.

La tunelización automática usa el prefijo ::/96, que está habilitado de forma predeterminada. Se puede deshabilitar quitando la ruta para ::/96.

6to4 usa el prefijo 2002::/16, que no está habilitado de forma predeterminada.

 

 



