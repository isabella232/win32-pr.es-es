---
title: PreferredServerBitness
description: Establece la arquitectura preferida, de 32 o 64 bits, para este servidor COM.
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- Valor del Registro PreferredServerBitness COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a8c5b1504c5a59ca2ab178cd46236335d44ca
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369732"
---
# <a name="preferredserverbitness"></a>PreferredServerBitness

Establece la arquitectura preferida, de 32 o 64 bits, para este servidor COM.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG DWORD** que solo está disponible en versiones de 64 bits de Windows.



| Value | Descripción                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Hacer coincidir la arquitectura del servidor con la arquitectura de cliente. Por ejemplo, si el cliente es de 32 bits, use una versión de 32 bits del servidor, si está disponible. Si no es así, se producirá un error en la solicitud de activación del cliente. |
| 2     | Use una versión de 32 bits del servidor. Si no existe, se producirá un error en la solicitud de activación del cliente.                                                                                                      |
| 3     | Use una versión de 64 bits del servidor. Si no existe, se producirá un error en la solicitud de activación del cliente.                                                                                                      |



 

Si este valor no está presente, entonces:

-   Si el equipo que hospeda el servidor ejecuta Windows XP o Windows Server 2003 sin SP1 o posterior instalado, COM preferirá una versión de 64 bits del servidor si está disponible; De lo contrario, activará una versión de 32 bits del servidor.
-   Si el equipo que hospeda el servidor ejecuta Windows Server 2003 con SP1 o posterior instalado, COM intentará hacer coincidir la arquitectura del servidor con la arquitectura del cliente. En otras palabras, para un cliente de 32 bits, COM activará un servidor de 32 bits si está disponible; De lo contrario, activará una versión de 64 bits del servidor. Para un cliente de 64 bits, COM activará un servidor de 64 bits si está disponible; De lo contrario, activará un servidor de 32 bits.

El cliente también puede especificar su propia preferencia de arquitectura a través de las marcas CLSCTX \_ ACTIVATE \_ 32 BIT SERVER y \_ \_ CLSCTX \_ ACTIVATE \_ 64 \_ BIT SERVER, \_ y estas invalidarán las preferencias del servidor. Para obtener más información y un gráfico de posibles interacciones entre las preferencias de arquitectura de cliente y servidor, vea [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 