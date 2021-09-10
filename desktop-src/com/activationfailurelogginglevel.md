---
title: ActivationFailureLoggingLevel
description: Establece el nivel de detalle de las entradas del registro de eventos sobre las solicitudes con error para el inicio y la activación de componentes.
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- Valor del Registro ACTIVATIONFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdd834be35a59dd5d8e207cd679dae68043d70c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369615"
---
# <a name="activationfailurelogginglevel"></a>ActivationFailureLoggingLevel

Establece el nivel de detalle de las entradas del registro de eventos sobre las solicitudes con error para el inicio y la activación de componentes.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG DWORD.**



| Value | Descripción                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Use el registro discrecional. Errores de registro de forma predeterminada, pero los clientes pueden invalidar este comportamiento especificando CLSCTX \_ NO FAILURE LOG en \_ \_ [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex). Este es el valor predeterminado. |
| 1     | Registre siempre todos los errores independientemente de lo que haya especificado el cliente.                                                                                                                                                      |
| 2     | No registre nunca ningún error independientemente de lo que haya especificado el cliente.                                                                                                                                                       |



 

Si necesita una aplicación para controlar el registro de eventos, se recomienda establecer este valor en 0 y escribir el código de cliente para invalidarlo cuando sea necesario. Se recomienda encarecidamente no establecer el valor en 2. Si el registro de eventos está deshabilitado, es más difícil diagnosticar problemas. Para los errores de permisos de restricciones de máquina, donde COM no tiene los bits CLSCTX, COM tratará un valor de 0 como 1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad para las aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




