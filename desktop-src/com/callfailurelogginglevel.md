---
title: CallFailureLoggingLevel
description: Establece el nivel de detalle de las entradas del registro de eventos sobre las llamadas con error a los componentes.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- Valor del Registro CallFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4432f21f333d5aa5f8b3cebbd6f0fa339cf0f13a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369656"
---
# <a name="callfailurelogginglevel"></a>CallFailureLoggingLevel

Establece el nivel de detalle de las entradas del registro de eventos sobre las llamadas con error a los componentes.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG DWORD.**



| Value | Descripción                                                                            |
|-------|----------------------------------------------------------------------------------------|
| 1     | Registre siempre los errores durante una llamada en el proceso del servidor COM.                           |
| 2     | Nunca registre errores durante una llamada en el proceso del servidor COM. Este es el valor predeterminado. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad para las aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




