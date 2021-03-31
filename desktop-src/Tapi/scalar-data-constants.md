---
description: En el caso de las constantes de datos escalares extensibles, un proveedor de proveedores de servicios puede definir nuevos valores en un intervalo especificado.
ms.assetid: 62280b71-9bec-4a9d-abd2-d3e1c2cee43f
title: Constantes de datos escalares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3187d2064501727614dfcbf0b8e11c136fea13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819422"
---
# <a name="scalar-data-constants"></a>Constantes de datos escalares

En el caso de las constantes de datos escalares extensibles, un proveedor de proveedores de servicios puede definir nuevos valores en un intervalo especificado. Dado que la mayoría de las constantes de datos son **DWORD** s, el intervalo de 0X00000000 a 0x7FFFFFFF normalmente se reserva para las extensiones futuras comunes, mientras que 0X80000000 a 0xFFFFFFFF está disponible para las extensiones específicas del proveedor. La suposición es que un proveedor definiría valores que son extensiones naturales de los tipos de los tipos de los que la API define.

 

 



