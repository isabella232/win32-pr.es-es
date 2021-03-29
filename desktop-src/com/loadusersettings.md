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
# <a name="loadusersettings"></a><span data-ttu-id="ca3bf-104">LoadUserSettings</span><span class="sxs-lookup"><span data-stu-id="ca3bf-104">LoadUserSettings</span></span>

<span data-ttu-id="ca3bf-105">Determina si COM cargará el perfil de usuario para los servidores COM que se ejecutan como la identidad de la aplicación de inicio.</span><span class="sxs-lookup"><span data-stu-id="ca3bf-105">Determines whether COM will load the user profile for COM servers running as the launching user application identity.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="ca3bf-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="ca3bf-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a><span data-ttu-id="ca3bf-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca3bf-107">Remarks</span></span>

<span data-ttu-id="ca3bf-108">Se trata de un valor de **Registro \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ca3bf-108">This is a **REG\_DWORD** value.</span></span> <span data-ttu-id="ca3bf-109">Si el *valor* es distinto de cero, com carga el perfil de la cuenta de usuario con la que se inicia el servidor com.</span><span class="sxs-lookup"><span data-stu-id="ca3bf-109">If *value* is nonzero, COM loads the profile of the user account with which it launches the COM server.</span></span> <span data-ttu-id="ca3bf-110">Si el *valor* es cero o no está presente, com no cargará el perfil de la cuenta de usuario con la que se inicia el servidor com.</span><span class="sxs-lookup"><span data-stu-id="ca3bf-110">If *value* is zero or not present, COM will not load the profile of the user account with which it launches the COM server.</span></span>

<span data-ttu-id="ca3bf-111">Este valor se omite si hay una entrada [**runas**](runas.md) .</span><span class="sxs-lookup"><span data-stu-id="ca3bf-111">This setting is ignored if a [**RunAs**](runas.md) entry is present.</span></span>

 

 




