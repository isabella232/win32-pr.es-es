---
title: Shell (COM)
description: Proporciona la impresión del shell de Windows 3,1 y la información abierta del archivo.
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- COM de clave del registro de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acf4a62d72892d1cd25a5f2276e71d52ab7f700
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800661"
---
# <a name="shell-com"></a>Shell (COM)

Proporciona la impresión del shell de Windows 3,1 y la información **abierta del archivo** .

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

 

 




