---
description: El tipo de datos GUID es una cadena de texto que representa un identificador de clase (ID). COM debe ser capaz de convertir la cadena en un identificador de clase válido. Todos los GUID deben crearse en mayúsculas.
ms.assetid: 9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8
title: GUID (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297c9995d537f6cf4b9d2ccf35488e27dc35903f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667785"
---
# <a name="guid"></a>GUID

El tipo de datos GUID es una cadena de texto que representa un identificador de clase (ID). COM debe ser capaz de convertir la cadena en un identificador de clase válido. Todos los GUID deben crearse en mayúsculas.

El formato válido para un GUID es {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}, donde X es un dígito hexadecimal (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F).

Tenga en cuenta que las utilidades como GUIDGEN pueden generar GUID que contienen letras minúsculas. Todos deben cambiarse a mayúsculas antes de que el programa de instalación pueda usar el GUID como código de producto válido, código de paquete o código de componente.

 

 



