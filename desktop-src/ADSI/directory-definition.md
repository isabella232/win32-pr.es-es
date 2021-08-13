---
title: Definición de directorio
description: El componente de proveedor de ejemplo usa un diseño de directorio relativamente sencillo para aclarar la relación entre los componentes y mostrar los requisitos mínimos necesarios para ser un proveedor adsi.
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8a46ee47bfa280fb9cffce32480fdad3164a648eee59a0c0b2740834b1f21cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691958"
---
# <a name="directory-definition"></a>Definición de directorio

El componente de proveedor de ejemplo usa un diseño de directorio relativamente sencillo para aclarar la relación entre los componentes y mostrar los requisitos mínimos necesarios para ser un proveedor adsi.

El "directorio" del componente de proveedor de ejemplo consta de dos nodos raíz: "Seattle" y "Toronto". Seattle contiene dos subniveles más, "Bellevue" y "Redmond". Cada una de estas entradas contiene varias cuentas de usuario. La entrada "Toronto" no tiene más subniveles, pero contiene directamente varias cuentas de usuario. En la ilustración siguiente se muestran estos dos nodos raíz conectados a una red.

![definición de directorio](images/dssmdo.png)

En términos jerárquicos, el nodo Espacio de nombres contiene "Seattle" y "Toronto". "Seattle" contiene "Bellevue" y "Redmond". "Bellevue" y "Redmond" contienen un conjunto de cuentas de usuario. "Toronto" contiene directamente las cuentas de usuario sin nodos organizativos intermedios.

El componente de proveedor de ejemplo representa esta estructura con solo dos tipos Active Directory objeto: un objeto contenedor y un objeto hoja. "Seattle", "Toronto", "Bellevue" y "Redmond" son objetos de contenedor y cada cuenta de usuario es un objeto hoja.

El componente de proveedor de ejemplo crea una clase de esquema denominada "Unidad organizativa" para un tipo de objeto de contenedor y una clase de esquema denominada "User" para una cuenta de usuario.

Las propiedades de cada clase de esquema, sus métodos y las reglas que rigen las relaciones de contención de estos objetos se definen en [Administración de esquemas](schema-management.md).

 

 




