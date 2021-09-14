---
title: Cadenas incrustadas
description: Las estructuras de información no contendrán cadenas incrustadas. Esto mejora la alineación de las estructuras de información y permite la flexibilidad de OEM en las funciones principales.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c71ed50971661f9ad06855024ecba2796f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069417"
---
# <a name="embedded-strings"></a>Cadenas incrustadas

Las estructuras de información no contendrán cadenas incrustadas. Esto mejora la alineación de las estructuras de información y permite la flexibilidad de OEM en las funciones principales.

Se garantiza que todos los campos de información devueltos en una llamada de enumeración que se puedan usar posteriormente como clave para la llamada a una función de administración de red GetInfo estarán presentes en el búfer de enumeración. Si no cabe la cadena de información de longitud variable que especificaría el valor del campo clave, no se devuelve toda la estructura de longitud fija de la entrada. Otros campos de longitud variable se devolverán como puntero **NULL** para el caso en el que la cadena no cabe.

 

 




