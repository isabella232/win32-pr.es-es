---
title: Control
description: Identifica un objeto como un control ActiveX control.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Control de la clave del Registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa6a0b131dd5fc2ba10d9aaeabafd06b19b73bb1e9422c28e5bec45ea43cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120515"
---
# <a name="control"></a>Control

Identifica un objeto como un control ActiveX control.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a>Comentarios

Los contenedores usan esta entrada opcional para rellenar los cuadros de diálogo. El contenedor usa esta subclave para determinar si se debe incluir un objeto en un cuadro de diálogo que muestra ActiveX controles. Un control puede omitir esta entrada si está diseñado para funcionar solo con un contenedor específico y, por tanto, no está pensado para insertarse en otros contenedores.

 

 




