---
title: LoadUserSettings
description: Determina si COM cargará el perfil de usuario para los servidores COM que se ejecutan como identidad de aplicación de usuario de inicio.
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- Valor del Registro COM LoadUserSettings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e14282b00bc2c2d9b989e19480047f115623d55
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249290"
---
# <a name="loadusersettings"></a>LoadUserSettings

Determina si COM cargará el perfil de usuario para los servidores COM que se ejecutan como identidad de aplicación de usuario de inicio.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG DWORD.** Si *el* valor es distinto de cero, COM carga el perfil de la cuenta de usuario con la que inicia el servidor COM. Si *el* valor es cero o no está presente, COM no cargará el perfil de la cuenta de usuario con la que inicia el servidor COM.

Esta configuración se omite si hay una [**entrada RunAs**](runas.md) presente.

 

 




