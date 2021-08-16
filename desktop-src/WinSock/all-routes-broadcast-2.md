---
description: Una difusión general a través de Internet se logra estableciendo los campos sa netnum y sa nodenum en \_ \_ binarios (1).
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: Difusión de todas las rutas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a5f0ba1e900dd390610a3bd3af2f779d523ae4a08973596e7da6b8331acc31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322727"
---
# <a name="all-routes-broadcast"></a>Difusión de todas las rutas

Una difusión general a través de Internet se logra estableciendo los campos **sa \_ netnum** y **sa \_ nodenum** en binarios (1). El proveedor de servicios traduce esta solicitud en un paquete de tipo 20, que los enrutadores IPX reconocen y reenvía. El paquete visita todas las subredes y se puede duplicar varias veces. Los receptores deben controlar varias copias duplicadas del datagrama.

El uso de este tipo de difusión no es popular entre los administradores de red, por lo que su uso debe ser muy limitado. Muchos enrutadores deshabilitan este tipo de difusión, dejando partes de la subred invisibles para el paquete.

 

 



