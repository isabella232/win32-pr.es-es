---
description: Una ruta de acceso del objeto de espacio de nombres describe la ubicación de un espacio de nombres determinado en un servidor. Una ruta de acceso de objeto de espacio de nombres contiene elementos de servidor y de espacio de nombres y se le da formato mediante barras diagonales o hacia atrás.
ms.assetid: 6d8da19e-0914-4267-870e-c203176b895e
ms.tgt_platform: multiple
title: Describir una ruta de acceso de objeto de espacio de nombres WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586104a1c193f1c229b0fbb27437d22e3686585b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082448"
---
# <a name="describing-a-wmi-namespace-object-path"></a>Describir una ruta de acceso de objeto de espacio de nombres WMI

Una ruta de acceso del objeto de espacio de nombres describe la ubicación de un espacio de nombres determinado en un servidor. Una ruta de acceso de objeto de espacio de nombres contiene elementos de servidor y de espacio de nombres y se le da formato mediante barras diagonales o hacia atrás.

El elemento Server especifica el nombre de red del equipo que hospeda el espacio de nombres, tal y como se muestra en el ejemplo siguiente.

``` syntax
\\Server\Namespace
```

\- o -

``` syntax
//Server/Namespace
```

Si el servidor es el equipo local, use un solo punto en lugar del nombre del servidor, como se muestra en el ejemplo siguiente.

``` syntax
\\.\Namespace
```

El elemento namespace especifica cualquier espacio de nombres válido. Un espacio de nombres se representa con una cadena jerárquica que contiene elementos delimitados por barras diagonales inversas, como la raíz \\ cimv2. No se pueden usar barras diagonales en los nombres de los espacios de nombres.

 

 



