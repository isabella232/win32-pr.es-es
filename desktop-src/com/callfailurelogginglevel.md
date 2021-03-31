---
title: CallFailureLoggingLevel
description: Establece el nivel de detalle de las entradas del registro de eventos sobre las llamadas con error a los componentes.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- Valor del registro CallFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4432f21f333d5aa5f8b3cebbd6f0fa339cf0f13a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903345"
---
# <a name="callfailurelogginglevel"></a>CallFailureLoggingLevel

Establece el nivel de detalle de las entradas del registro de eventos sobre las llamadas con error a los componentes.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** .



| Value | Descripción                                                                            |
|-------|----------------------------------------------------------------------------------------|
| 1     | Registre siempre los errores durante una llamada en el proceso de servidor COM.                           |
| 2     | Nunca Registre errores durante una llamada en el proceso de servidor COM. Este es el valor predeterminado. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad de las aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




