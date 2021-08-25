---
title: Cadenas incrustadas
description: Las estructuras de información no contendrán cadenas incrustadas. Esto mejora la alineación de las estructuras de información y permite flexibilidad de OEM en las funciones principales.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6121e805a1dbe329cee52a760c809ded21f1740b19adaa3e18eaa5033fd15897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912255"
---
# <a name="embedded-strings"></a>Cadenas incrustadas

Las estructuras de información no contendrán cadenas incrustadas. Esto mejora la alineación de las estructuras de información y permite flexibilidad de OEM en las funciones principales.

Se garantiza que todos los campos de información devueltos en una llamada de enumeración que se puedan usar posteriormente como clave para la llamada a una función de administración de red GetInfo estarán presentes en el búfer de enumeración. Si la cadena de información de longitud variable que especificaría el valor del campo clave no cabe, no se devuelve toda la estructura de longitud fija de la entrada. Otros campos de longitud variable se devolverán como puntero **NULL** para el caso en el que la cadena no cabe.

 

 




