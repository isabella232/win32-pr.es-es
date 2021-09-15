---
title: Shell (COM)
description: Proporciona Windows de shell 3.1 e información de apertura de archivos.
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- COM de clave del Registro de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acf4a62d72892d1cd25a5f2276e71d52ab7f700
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465699"
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

 

 




