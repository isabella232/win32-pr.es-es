---
title: NONREDIST
description: Agrega nombres a la lista de archivos que no se deben exportar cuando las aplicaciones COM+ se empaquetan para su instalación en otros equipos. Tenga en cuenta que se trata de una subclave, no de un valor.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- VALOR DEL Registro NOREDISTA COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d537208ecaf98cec46591966e4ae7d9c205850a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369671"
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

## <a name="remarks"></a>Observaciones

Los archivos que agregue a la lista se representan mediante pares nombre-valor almacenados bajo esta clave. En cada par nombre-valor, el nombre es el nombre del archivo y el valor está reservado.

 

 




