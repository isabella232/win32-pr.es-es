---
title: Detalles de implementación de DVC
description: Esta sección contiene información sobre cómo escribir un módulo de cliente de canal virtual dinámico (DVC).
ms.assetid: 338556d9-e9a7-4926-a09c-8e2ce1627467
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd12ed5d755932777b0ad7fe38382ff1254a323bb78b3de44fbe92f4cff47422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657965"
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

Describe la sintaxis de la entrada del complemento de canal virtual dinámico (DVC) para el cliente Conexión a Escritorio remoto (RDC).

</dd> <dt>

[Iniciar un agente de escucha de DVC](starting-a-dvc-listener.md)
</dt> <dd>

Para establecer una conexión correcta entre dos módulos de canal virtual dinámico (DVC) que se ejecutan en el cliente y el servidor de Conexión a Escritorio remoto (RDC), un agente de escucha dvc debe estar en ejecución y en estado de escucha.

</dd> <dt>

[Aceptación de una conexión](accepting-a-connection.md)
</dt> <dd>

En algún momento, el cliente de canal virtual dinámico (DVC) solicitará una conexión al agente de escucha de DVC.

</dd> <dt>

[Escribir datos mediante un canal DVC](writing-data-by-using-a-dvc-channel.md)
</dt> <dd>

Escribir datos de canal mediante un canal virtual dinámico (DVC) es simétrico tanto para el servidor Escritorio remoto Session Host (Host de sesión de Escritorio remoto) como para el cliente.

</dd> <dt>

[Pruebas y depuración](testing-and-debugging.md)
</dt> <dd>

Hay un agente de escucha de "eco" implementado por el cliente de Conexión a Escritorio remoto (RDC), que siempre está presente y que escucha las conexiones entrantes.

</dd> <dt>

[Ejemplo de complemento de cliente DVC](dvc-client-plug-in-example.md)
</dt> <dd>

Ejemplo de código de C++ que muestra cómo crear un complemento Conexión a Escritorio remoto canal virtual dinámico (DVC) de cliente (RDC).

</dd> <dt>

[Ejemplo de módulo de servidor DVC](dvc-server-component-example.md)
</dt> <dd>

Ejemplo de código de C++ que muestra cómo crear el módulo de canal virtual dinámico (DVC) del lado servidor.

</dd> </dl>

 

 




