---
title: PreferredServerBitness
description: Establece la arquitectura preferida, 32 bits o 64 bits, para este servidor COM.
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- Valor del registro PreferredServerBitness COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a8c5b1504c5a59ca2ab178cd46236335d44ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359444"
---
# <a name="preferredserverbitness"></a>PreferredServerBitness

Establece la arquitectura preferida, 32 bits o 64 bits, para este servidor COM.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** que solo está disponible en las versiones de 64 bits de Windows.



| Value | Descripción                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Haga coincidir la arquitectura de servidor con la arquitectura de cliente. Por ejemplo, si el cliente es de 32 bits, utilice una versión de 32 bits del servidor, si está disponible. De lo contrario, se producirá un error en la solicitud de activación del cliente. |
| 2     | Use una versión de 32 bits del servidor. Si no existe ninguna, se producirá un error en la solicitud de activación del cliente.                                                                                                      |
| 3     | Use una versión de 64 bits del servidor. Si no existe ninguna, se producirá un error en la solicitud de activación del cliente.                                                                                                      |



 

Si este valor no está presente, entonces:

-   Si el equipo que hospeda el servidor está ejecutando Windows XP o Windows Server 2003 sin SP1 o posterior instalado, COM preferirá una versión de 64 bits del servidor si está disponible; en caso contrario, activará una versión de 32 bits del servidor.
-   Si el equipo que hospeda el servidor está ejecutando Windows Server 2003 con SP1 o una versión posterior instalada, COM intentará hacer coincidir la arquitectura de servidor con la arquitectura de cliente. En otras palabras, para un cliente de 32 bits, COM activará un servidor de 32 bits si está disponible; en caso contrario, activará una versión de 64 bits del servidor. Para un cliente de 64 bits, COM activará un servidor de 64 bits si está disponible; en caso contrario, activará un servidor de 32 bits.

El cliente también puede especificar su propia preferencia de arquitectura a través de las \_ marcas de servidor CLSCTX activar \_ 32 \_ bits \_ y CLSCTX \_ activar \_ 64 \_ bits \_ , y esto invalidará las preferencias del servidor. Para obtener más información y un gráfico de posibles interacciones entre las preferencias de la arquitectura de cliente y de servidor, vea [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 