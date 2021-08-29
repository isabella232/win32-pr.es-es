---
title: Shell (COM)
description: Proporciona Windows de shell 3.1 e información de apertura de archivos.
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- COM de clave del Registro de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ebbc83642896aa22f33b315e26097760f7311ec93d938cb0440a10e0aae049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129907"
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

## <a name="remarks"></a>Comentarios

Estas entradas deben proporcionar la ruta de acceso y el nombre de archivo de la aplicación.

 

 




