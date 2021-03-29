---
title: Control
description: Identifica un objeto como un control ActiveX.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Control COM de la clave del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3722d85b38399d7e95f226749bda45ccc82d1369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419143"
---
# <a name="control"></a>Control

Identifica un objeto como un control ActiveX.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a>Observaciones

Los contenedores usan esta entrada opcional para rellenar los cuadros de diálogo. El contenedor usa esta subclave para determinar si se debe incluir un objeto en un cuadro de diálogo que muestre controles ActiveX. Un control puede omitir esta entrada si está diseñada para funcionar solo con un contenedor específico y, por tanto, no está diseñada para insertarse en otros contenedores.

 

 




