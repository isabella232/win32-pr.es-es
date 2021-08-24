---
title: ServiceParameters
description: Especifica los parámetros de línea de comandos que se pasarán a un objeto instalado para su uso por COM a través del valor del Registro LocalService.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- Valor com del Registro ServiceParameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103b55269b700beaf5c85e3408e3597e63fb9140e4dc79fe4bb895ff6767bfc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129967"
---
# <a name="serviceparameters"></a>ServiceParameters

Especifica los parámetros de línea de comandos que se pasarán a un objeto instalado para su uso por COM a través del valor del Registro [**LocalService.**](localservice.md)

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG SZ.** Esta cadena se pasa al servicio como un argumento de línea de comandos mientras se inicia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**LocalService (Servicio local)**](localservice.md)
</dt> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> </dl>

 

 




