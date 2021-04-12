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
# <a name="serviceparameters"></a>ServiceParameters

Especifica los parámetros de línea de comandos que se van a pasar a un objeto instalado para que lo use COM mediante el valor del registro [**LocalService**](localservice.md) .

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a>Observaciones

Este es un valor de **reg \_ SZ** . Esta cadena se pasa al servicio como un argumento de línea de comandos cuando se inicia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**LocalService (Servicio local)**](localservice.md)
</dt> <dt>

[Registrar servidores COM](registering-com-servers.md)
</dt> </dl>

 

 




