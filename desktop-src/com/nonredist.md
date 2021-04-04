---
title: NONREDIST
description: Agrega nombres a la lista de archivos que no se deben exportar cuando las aplicaciones COM+ se empaquetan para instalarse en otros equipos. Tenga en cuenta que se trata de una subclave, no de un valor.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- Valor del registro nonredit COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d537208ecaf98cec46591966e4ae7d9c205850a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076413"
---
# <a name="nonredist"></a>NONREDIST

Agrega nombres a la lista de archivos que no se deben exportar cuando las aplicaciones COM+ se empaquetan para instalarse en otros equipos. Tenga en cuenta que se trata de una subclave, no de un valor.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a>Observaciones

Los archivos que se agregan a la lista se representan mediante pares de nombre/valor almacenados bajo esta clave. En cada par de nombre y valor, el nombre es el nombre de archivo y el valor está reservado.

 

 




