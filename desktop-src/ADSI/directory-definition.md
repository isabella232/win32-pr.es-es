---
title: Definición de directorio
description: El componente de proveedor de ejemplo usa un diseño de directorio relativamente sencillo para clarificar la relación entre los componentes y mostrar los requisitos mínimos necesarios para ser un proveedor ADSI.
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6156f2e1ab89b34f009f1a86e5de011c20cf9503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903064"
---
# <a name="directory-definition"></a>Definición de directorio

El componente de proveedor de ejemplo usa un diseño de directorio relativamente sencillo para clarificar la relación entre los componentes y mostrar los requisitos mínimos necesarios para ser un proveedor ADSI.

El "directorio" del componente de proveedor de ejemplo consta de dos nodos raíz: "Seattle" y "Toronto". Seattle contiene dos subnivels más, "Bellevue" y "Redmond". Cada una de estas entradas contiene varias cuentas de usuario. La entrada "Toronto" no tiene más subniveles, pero contiene directamente varias cuentas de usuario. En la siguiente ilustración se muestran estos dos nodos raíz conectados a una red.

![definición de directorio](images/dssmdo.png)

En términos jerárquicos, el nodo de espacio de nombres contiene "Seattle" y "Toronto". "Seattle" contiene "Bellevue" y "Redmond". "Bellevue" y "Redmond" contienen un conjunto de cuentas de usuario. "Toronto" contiene directamente las cuentas de usuario sin nodos intermedios de la organización.

El componente de proveedor de ejemplo representa esta estructura con solo dos tipos de objeto Active Directory: un objeto contenedor y un objeto hoja. "Seattle", "Toronto", "Bellevue" y "Redmond" son objetos contenedores y cada cuenta de usuario es un objeto hoja.

El componente proveedor de ejemplo crea una clase de esquema denominada "unidad organizativa" para un tipo de objeto contenedor y una clase de esquema denominada "usuario" para una cuenta de usuario.

Las propiedades de cada clase de esquema, sus métodos y las reglas que rigen las relaciones de contención de estos objetos se definen en la [Administración de esquemas](schema-management.md).

 

 




