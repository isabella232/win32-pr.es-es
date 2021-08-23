---
title: CallFailureLoggingLevel
description: Establece el nivel de detalle de las entradas del registro de eventos sobre las llamadas con error a los componentes.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- Valor com del Registro CallFailureLoggingLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819d132a8cd0f1741eb3b825a17f02387b200e80f2dba6913821e77f9a0913cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793825"
---
# <a name="callfailurelogginglevel"></a>CallFailureLoggingLevel

Establece el nivel de detalle de las entradas del registro de eventos sobre las llamadas con error a los componentes.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG DWORD.**



| Value | Descripción                                                                            |
|-------|----------------------------------------------------------------------------------------|
| 1     | Registre siempre los errores durante una llamada en el proceso del servidor COM.                           |
| 2     | Nunca registre errores durante una llamada en el proceso del servidor COM. Este es el valor predeterminado. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la seguridad para aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




