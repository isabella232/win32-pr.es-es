---
description: En el caso de las constantes de datos de marca de bits extensible, un proveedor de proveedor de servicios puede definir nuevos valores para los bits especificados.
ms.assetid: bf3ca2b0-a9fb-4e63-87de-6d5cbe5cd746
title: Constantes de datos de Bit-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238627505bf414ed0ab94ff2f5c35197705c91d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687252"
---
# <a name="bit-flag-data-constants"></a>Constantes de datos de Bit-Flag

En el caso de las constantes de datos de marca de bits extensible, un proveedor de proveedor de servicios puede definir nuevos valores para los bits especificados. Dado que la mayoría de las constantes de marcador de bits son **DWORD** s, un número específico de los bits inferiores normalmente se reserva para las extensiones comunes, mientras que los bits superiores restantes están disponibles para las extensiones específicas del proveedor. Las marcas de bits comunes se asignan a partir de cero bits hacia arriba y las extensiones específicas del proveedor deben asignarse desde el bit 31 hacia abajo. Este esquema proporciona la máxima flexibilidad a la hora de asignar posiciones de bits a extensiones comunes, en lugar de extensiones específicas del proveedor. Se espera que un proveedor defina nuevos valores que son extensiones naturales de las marcas de bits definidas por la API.

Las estructuras de datos extensibles tienen un campo de tamaño variable que se reserva para uso específico del dispositivo. Dado que el campo tiene un tamaño de variable, el proveedor de servicios decide la cantidad de información e interpretación del campo. Se espera que un proveedor que define un campo específico del dispositivo realice estas extensiones naturales de la estructura de datos original definida por la API.

 

 



