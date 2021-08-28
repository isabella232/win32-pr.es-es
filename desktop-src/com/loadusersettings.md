---
title: LoadUserSettings
description: Determina si COM cargará el perfil de usuario para los servidores COM que se ejecutan como identidad de aplicación de usuario de inicio.
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- Valor del Registro LoadUserSettings COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b82bd89015baa4c73c9200013e49c76523951218dfde62bbe39300eefdfe0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731045"
---
# <a name="loadusersettings"></a>LoadUserSettings

Determina si COM cargará el perfil de usuario para los servidores COM que se ejecutan como identidad de aplicación de usuario de inicio.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG DWORD.** Si *el* valor es distinto de cero, COM carga el perfil de la cuenta de usuario con la que inicia el servidor COM. Si *el* valor es cero o no está presente, COM no cargará el perfil de la cuenta de usuario con la que inicia el servidor COM.

Esta configuración se omite si hay una [**entrada RunAs**](runas.md) presente.

 

 




