---
title: Creación de un proveedor de Protocolo de escritorio remoto
description: Información sobre cómo crear un proveedor de Protocolo de escritorio remoto. El administrador de protocolos se implementa como un servidor COM y se registra en una ubicación en la que se busca cuando se inicia el servicio Servicios de Escritorio remoto.
ms.assetid: 9a3e6d5c-464f-4227-a06f-16eb8ed1079e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41265a350b4d5c559731a09abc21aa4c81b9b29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685470"
---
# <a name="creating-a-remote-desktop-protocol-provider"></a>Creación de un proveedor de Protocolo de escritorio remoto

Las secciones siguientes contienen información sobre cómo crear un proveedor de Protocolo de escritorio remoto. El administrador de protocolos se implementa como un servidor COM y se registra en una ubicación en la que se busca cuando se inicia el servicio Servicios de Escritorio remoto.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Registro del administrador de protocolos](registering-the-custom-protocol.md)
</dt> <dd>

Debe crear al menos una entrada de valor de registro para el administrador de protocolos para que el servicio de Servicios de Escritorio remoto pueda crear una instancia de ella.

</dd> <dt>

[Secuencia de llamada al método](method-call-sequence.md)
</dt> <dd>

El servicio de Servicios de Escritorio remoto y el proveedor de protocolo se llaman entre sí en secuencias claramente definidas.

</dd> </dl>

-   [Registro del administrador de protocolos](registering-the-custom-protocol.md)
-   [Secuencia de llamada al método](method-call-sequence.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API del proveedor de Protocolo de escritorio remoto](custom-remote-desktop-protocols.md)
</dt> <dt>

[Usar Servicios de Escritorio remoto](using-terminal-services.md)
</dt> </dl>

 

 




