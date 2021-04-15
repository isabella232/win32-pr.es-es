---
title: Detalles de implementación de DVC
description: Esta sección contiene información sobre cómo escribir un módulo de cliente de canal virtual dinámico (DVC).
ms.assetid: 338556d9-e9a7-4926-a09c-8e2ce1627467
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876722736a95b45918d8a5b9e229f4f9eda5840b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676137"
---
# <a name="dvc-implementation-details"></a>Detalles de implementación de DVC

Esta sección contiene información sobre cómo escribir un módulo de cliente de canal virtual dinámico (DVC).

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Escritura de un módulo DVC de cliente](writing-a-client-dvc-component.md)
</dt> <dd>

Para escribir un módulo de cliente de canal virtual dinámico (DVC), primero debe implementar y registrar un complemento de cliente Conexión a Escritorio remoto (RDC).

</dd> <dt>

[Registro del complemento DVC](dvc-plug-in-registration.md)
</dt> <dd>

Describe la sintaxis de la entrada del complemento de canal virtual dinámico (DVC) del cliente Conexión a Escritorio remoto (RDC).

</dd> <dt>

[Inicio de un agente de escucha de DVC](starting-a-dvc-listener.md)
</dt> <dd>

Para establecer una conexión correcta entre dos módulos de canal virtual dinámico (DVC) que se ejecutan en el cliente y servidor de Conexión a Escritorio remoto (RDC), un agente de escucha de DVC debe estar en ejecución y en un estado de escucha.

</dd> <dt>

[Aceptación de una conexión](accepting-a-connection.md)
</dt> <dd>

En algún momento, el cliente del canal virtual dinámico (DVC) solicitará una conexión con el agente de escucha de DVC.

</dd> <dt>

[Escribir datos mediante un canal de DVC](writing-data-by-using-a-dvc-channel.md)
</dt> <dd>

Escritorio remoto la escritura de datos del canal mediante el uso de un canal virtual dinámico (DVC) es simétrica tanto para el servidor host de sesión de escritorio remoto (host de sesión de RD) como para el cliente.

</dd> <dt>

[Pruebas y depuración](testing-and-debugging.md)
</dt> <dd>

Hay un agente de escucha de "Eco" implementado por el cliente Conexión a Escritorio remoto (RDC), que siempre está presente y escuchando conexiones entrantes.

</dd> <dt>

[Ejemplo de complemento de cliente de DVC](dvc-client-plug-in-example.md)
</dt> <dd>

Código de ejemplo de C++ que muestra cómo crear un complemento de canal virtual dinámico (DVC) del cliente Conexión a Escritorio remoto (RDC).

</dd> <dt>

[Ejemplo del módulo de servidor DVC](dvc-server-component-example.md)
</dt> <dd>

Código de ejemplo de C++ que muestra cómo crear el módulo de canal virtual dinámico (DVC) del lado servidor.

</dd> </dl>

 

 




