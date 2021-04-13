---
title: ActivationFailureLoggingLevel
description: Establece el nivel de detalle de las entradas del registro de eventos sobre las solicitudes con error de inicio y activación de componentes.
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- Valor del registro ActivationFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdd834be35a59dd5d8e207cd679dae68043d70c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419145"
---
# <a name="activationfailurelogginglevel"></a>ActivationFailureLoggingLevel

Establece el nivel de detalle de las entradas del registro de eventos sobre las solicitudes con error de inicio y activación de componentes.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** .



| Value | Descripción                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Use el registro discrecional. Registrar errores de forma predeterminada, pero los clientes pueden invalidar este comportamiento mediante la especificación \_ de CLSCTX ningún \_ \_ registro de errores en [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex). Este es el valor predeterminado. |
| 1     | Registre siempre todos los errores independientemente del cliente especificado.                                                                                                                                                      |
| 2     | Nunca registre ningún error independientemente de lo que haya especificado el cliente.                                                                                                                                                       |



 

Si necesita una aplicación para controlar el registro de eventos, se recomienda establecer este valor en 0 y escribir el código de cliente para invalidarlo cuando sea necesario. Se recomienda encarecidamente no establecer el valor en 2. Si el registro de eventos está deshabilitado, es más difícil diagnosticar los problemas. En el caso de los errores de permisos de restricciones del equipo, en los que COM no tiene los bits CLSCTX, COM tratará un valor de 0 como 1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad de las aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




