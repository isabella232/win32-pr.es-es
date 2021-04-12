---
title: ServiceParameters
description: Especifica los parámetros de línea de comandos que se van a pasar a un objeto instalado para que lo use COM mediante el valor del registro LocalService.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- Valor del registro ServiceParameters COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235de1052df72e88e2093647928ed68ab67451cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357144"
---
# <a name="serviceparameters"></a><span data-ttu-id="faa8d-104">ServiceParameters</span><span class="sxs-lookup"><span data-stu-id="faa8d-104">ServiceParameters</span></span>

<span data-ttu-id="faa8d-105">Especifica los parámetros de línea de comandos que se van a pasar a un objeto instalado para que lo use COM mediante el valor del registro [**LocalService**](localservice.md) .</span><span class="sxs-lookup"><span data-stu-id="faa8d-105">Specifies the command-line parameters to be passed to an object installed for use by COM through the [**LocalService**](localservice.md) registry value.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="faa8d-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="faa8d-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a><span data-ttu-id="faa8d-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="faa8d-107">Remarks</span></span>

<span data-ttu-id="faa8d-108">Este es un valor de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="faa8d-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="faa8d-109">Esta cadena se pasa al servicio como un argumento de línea de comandos cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="faa8d-109">This string is passed to the service as a command-line argument as it is being launched.</span></span>

## <a name="related-topics"></a><span data-ttu-id="faa8d-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="faa8d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faa8d-111">**LocalService (Servicio local)**</span><span class="sxs-lookup"><span data-stu-id="faa8d-111">**LocalService**</span></span>](localservice.md)
</dt> <dt>

[<span data-ttu-id="faa8d-112">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="faa8d-112">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 




