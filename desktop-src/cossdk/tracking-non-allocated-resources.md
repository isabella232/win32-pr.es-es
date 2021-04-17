---
description: Seguimiento de recursos no asignados
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: Seguimiento de recursos no asignados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c9f814e08798b4fbb0f160e0d0e0f8aabebba7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705357"
---
# <a name="tracking-non-allocated-resources"></a>Seguimiento de recursos no asignados

El administrador dispensador puede realizar el seguimiento de un recurso que no está inventariado, en función del conocimiento de la duración del objeto. Cuando se libera un recurso del que se ha realizado un seguimiento, se destruye y, por lo tanto, no se devuelve al inventario. Este modo de solo seguimiento para los recursos que son económicos para crear y destruir es más útil que almacenarlos en el inventario. Este modo también es útil para administrar un dispensador de memoria o para un recurso que es difícil de inventariar porque hay demasiados tipos diferentes.

En el modo de solo seguimiento, un dispensador de recursos crea directamente un recurso solicitado en lugar de solicitar al administrador dispensado que asigne uno de inventario. Antes de devolver este recurso al componente de la aplicación solicitante, el dispensador de recursos indica al administrador dispensador que realice un seguimiento del recurso, lo que garantiza que incluso si el componente no tiene que liberar el recurso, el administrador del dispensador lo hará cuando la duración del componente sea superior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



