---
title: ServiceParameters
description: Especifica los parámetros de línea de comandos que se pasarán a un objeto instalado para su uso por COM a través del valor del Registro LocalService.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- Valor del Registro COM de ServiceParameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235de1052df72e88e2093647928ed68ab67451cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063901"
---
# <a name="serviceparameters"></a>ServiceParameters

Especifica los parámetros de línea de comandos que se pasarán a un objeto instalado para su uso por COM a través del valor del Registro [**LocalService.**](localservice.md)

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG SZ.** Esta cadena se pasa al servicio como un argumento de línea de comandos mientras se inicia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**LocalService (Servicio local)**](localservice.md)
</dt> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> </dl>

 

 




