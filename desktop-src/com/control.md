---
title: Control
description: Identifica un objeto como un control ActiveX control.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Control de la clave del Registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3722d85b38399d7e95f226749bda45ccc82d1369
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369576"
---
# <a name="control"></a>Control

Identifica un objeto como un control ActiveX control.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a>Observaciones

Los contenedores usan esta entrada opcional para rellenar los cuadros de diálogo. El contenedor usa esta subclave para determinar si se debe incluir un objeto en un cuadro de diálogo que muestra ActiveX controles. Un control puede omitir esta entrada si está diseñado para funcionar solo con un contenedor específico y, por tanto, no está diseñado para insertarse en otros contenedores.

 

 




