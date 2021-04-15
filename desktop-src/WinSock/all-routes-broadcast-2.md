---
description: Una difusión general a través de Internet se logra estableciendo los \_ campos SA netnum y SA \_ nodenum en binarios (1).
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: Difundir todas las rutas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15830ad4f82a3cc5d93e84762c8c17ed0cfd85bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497476"
---
# <a name="all-routes-broadcast"></a>Difundir todas las rutas

Una difusión general a través de Internet se logra estableciendo los campos **SA \_ netnum** y **SA \_ nodenum** en binarios (1). El proveedor de servicios traduce esta solicitud a un paquete de tipo 20, que los enrutadores IPX reconocen y reenvían. El paquete visita todas las subredes y puede duplicarse varias veces. Los receptores deben controlar varias copias duplicadas del datagrama.

El uso de este tipo de difusión no es popular entre los administradores de red, por lo que su uso debe ser extremadamente limitado. Muchos enrutadores deshabilitan este tipo de difusión y dejan las partes de la subred invisibles para el paquete.

 

 



