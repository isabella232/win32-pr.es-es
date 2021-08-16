---
description: Seguimiento de recursos no asignados
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: Seguimiento de recursos no asignados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb356a7e7243c7e6f856a0dfe165440ff0b909545703032a8442bbcced77649d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305245"
---
# <a name="tracking-non-allocated-resources"></a>Seguimiento de recursos no asignados

El administrador del dispensador puede realizar un seguimiento de un recurso que no está inventariado, en función del conocimiento de la duración del objeto. Cuando se libera un recurso con seguimiento y no asignado, se destruye y, por tanto, no se devuelve al inventario. Este modo de solo seguimiento para los recursos que son económico de crear y destruir es más útil que almacenarlos en el inventario. Este modo también es útil para administrar un dispensador de memoria o para un recurso que es difícil de inventariar porque hay demasiados tipos diferentes.

En el modo de solo seguimiento, un dispensador de recursos crea directamente un recurso solicitado en lugar de pedir al administrador del dispensador que asigne uno del inventario. Antes de devolver este recurso al componente de aplicación solicitante, el dispensador de recursos indica al administrador del dispensador que realice el seguimiento del recurso, lo que garantiza que, aunque el componente no tenga que liberar el recurso, el administrador del dispensador lo hará cuando se haya terminado la duración del componente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del dispensador de recursos com+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



