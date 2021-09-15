---
description: Una ruta de acceso de objeto de espacio de nombres describe la ubicación de un espacio de nombres determinado en un servidor. Una ruta de acceso de objeto de espacio de nombres contiene elementos de servidor y espacio de nombres, y tiene formato mediante barras diagonales o anteriores.
ms.assetid: 6d8da19e-0914-4267-870e-c203176b895e
ms.tgt_platform: multiple
title: Describir una ruta de acceso de objeto de espacio de nombres WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586104a1c193f1c229b0fbb27437d22e3686585b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467273"
---
# <a name="describing-a-wmi-namespace-object-path"></a>Describir una ruta de acceso de objeto de espacio de nombres WMI

Una ruta de acceso de objeto de espacio de nombres describe la ubicación de un espacio de nombres determinado en un servidor. Una ruta de acceso de objeto de espacio de nombres contiene elementos de servidor y espacio de nombres, y tiene formato mediante barras diagonales o anteriores.

El elemento server especifica el nombre de red del equipo que hospeda el espacio de nombres, como se muestra en el ejemplo siguiente.

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

El elemento namespace especifica cualquier espacio de nombres válido. Un espacio de nombres se representa con una cadena jerárquica que contiene elementos delimitados por barras diagonales inversas únicas, como root \\ cimv2. No puede usar barras diagonales dentro de los nombres de espacio de nombres.

 

 



