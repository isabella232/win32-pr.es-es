---
title: Shell (COM)
description: Proporciona Windows de shell 3.1 e información de apertura de archivos.
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- COM de clave del Registro de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acf4a62d72892d1cd25a5f2276e71d52ab7f700
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369479"
---
# <a name="shell-com"></a>Shell (COM)

Proporciona Windows de shell 3.1 e **información de apertura de** archivos.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Shell
         Open
            command = path %1
         Print
            command = path %1
```

## <a name="remarks"></a>Observaciones

Estas entradas deben proporcionar la ruta de acceso y el nombre de archivo de la aplicación.

 

 




