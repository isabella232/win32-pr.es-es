---
title: NONREDIST
description: Agrega nombres a la lista de archivos que no se deben exportar cuando las aplicaciones COM+ se empaquetan para su instalación en otros equipos. Tenga en cuenta que se trata de una subclave, no de un valor.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- VALOR DEL Registro NOREDISTA COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b303c145ea48a51f72d6ee21078b5f29a6b6d4fabc7184d4a37e980a2bbb2e4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678465"
---
# <a name="nonredist"></a>NONREDIST

Agrega nombres a la lista de archivos que no se deben exportar cuando las aplicaciones COM+ se empaquetan para su instalación en otros equipos. Tenga en cuenta que se trata de una subclave, no de un valor.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a>Comentarios

Los archivos que agregue a la lista se representan mediante pares nombre-valor almacenados bajo esta clave. En cada par nombre-valor, el nombre es el nombre del archivo y el valor está reservado.

 

 




