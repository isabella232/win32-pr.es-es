---
title: Varios controles en un archivo DLL
description: Varios controles en un archivo DLL
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e11c91faa26420f37df330ad7f1d9eff4587f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075154"
---
# <a name="multiple-controls-in-one-dll"></a>Varios controles en un archivo DLL

Un solo archivo DLL. ocx puede incluir cualquier número de controles ActiveX, lo que simplifica la distribución y el uso de un conjunto de controles relacionados.

Si envía varios controles a un solo archivo DLL, asegúrese de incluir el nombre del proveedor en cada nombre de control del paquete. La inclusión de los nombres de los proveedores en cada nombre de control permitirá a los usuarios identificar fácilmente los controles dentro de un paquete. Por ejemplo, si envía un archivo DLL que implementa tres controles, Con1, Con2 y Con3, los nombres de los controles deben ser:

-   *El nombre de la empresa* Control Con1

-   *El nombre de la empresa* Control Con2

-   *El nombre de la empresa* Control Con3

 

 




