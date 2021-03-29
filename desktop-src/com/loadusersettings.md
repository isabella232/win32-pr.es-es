---
title: LoadUserSettings
description: Determina si COM cargará el perfil de usuario para los servidores COM que se ejecutan como la identidad de la aplicación de inicio.
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- Valor del registro LoadUserSettings COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e14282b00bc2c2d9b989e19480047f115623d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994424"
---
# <a name="loadusersettings"></a>LoadUserSettings

Determina si COM cargará el perfil de usuario para los servidores COM que se ejecutan como la identidad de la aplicación de inicio.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** . Si el *valor* es distinto de cero, com carga el perfil de la cuenta de usuario con la que se inicia el servidor com. Si el *valor* es cero o no está presente, com no cargará el perfil de la cuenta de usuario con la que se inicia el servidor com.

Este valor se omite si hay una entrada [**runas**](runas.md) .

 

 




