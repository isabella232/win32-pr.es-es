---
title: Varios controles en un archivo DLL
description: Varios controles en un archivo DLL
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b571f307f3438ca8f8ce0a0a716af2042884520cd07746f8e6fa8c1739fae22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130067"
---
# <a name="multiple-controls-in-one-dll"></a>Varios controles en un archivo DLL

Un solo archivo DLL .ocx puede contenedorar cualquier número de controles ActiveX, lo que simplifica la distribución y el uso de un conjunto de controles relacionados.

Si envía varios controles en un solo archivo DLL, asegúrese de incluir el nombre del proveedor en cada nombre de control del paquete. Incluir los nombres de los proveedores en cada nombre de control permitirá a los usuarios identificar fácilmente los controles dentro de un paquete. Por ejemplo, si envía un archivo DLL que implementa tres controles, Con1, Con2 y Con3, los nombres de control deben ser:

-   *Nombre de la empresa* Con1 Control

-   *Nombre de la empresa* Con2 Control

-   *Nombre de la empresa* Con3 Control

 

 




