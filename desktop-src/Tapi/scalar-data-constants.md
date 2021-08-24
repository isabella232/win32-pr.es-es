---
description: Para las constantes de datos escalares extensibles, un proveedor de servicios puede definir nuevos valores en un intervalo especificado.
ms.assetid: 62280b71-9bec-4a9d-abd2-d3e1c2cee43f
title: Constantes de datos escalares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 815288ca4a22da741e5b98257ae50732f818b466404a95712ee74756785fd699
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773315"
---
# <a name="scalar-data-constants"></a>Constantes de datos escalares

Para las constantes de datos escalares extensibles, un proveedor de servicios puede definir nuevos valores en un intervalo especificado. Dado que la mayoría de las constantes de datos son **DWORD,** el intervalo 0x00000000 a 0x7FFFFFFF normalmente se reserva para extensiones futuras comunes, mientras que 0x80000000 a 0xFFFFFFFF está disponible para extensiones específicas del proveedor. La suposición es que un proveedor definiría valores que son extensiones naturales de los tipos de datos definidos por la API.

 

 



