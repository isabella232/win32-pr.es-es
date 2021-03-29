---
title: Acceso a interfaces entre apartamentos
description: Acceso a interfaces entre apartamentos
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626707daf721aee3b440bb79ba2d1e084d154a98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774796"
---
# <a name="accessing-interfaces-across-apartments"></a>Acceso a interfaces entre apartamentos

COM proporciona una manera para cualquier apartamento de un proceso de obtener acceso a una interfaz implementada en un objeto de cualquier otro apartamento del proceso. Esto se realiza a través de la interfaz [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) . Esta interfaz tiene tres métodos, que le permiten hacer lo siguiente:

-   Registre una interfaz como una interfaz *global* (processwide).
-   Obtiene un puntero a la interfaz de cualquier otro apartamento a través de una cookie.
-   Revocar el registro global de una interfaz.

La interfaz [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) es una manera eficaz de que un proceso almacene un puntero de interfaz en una ubicación de memoria a la que se puede tener acceso desde varios apartamentos dentro del proceso, como variables para todo el proceso y objetos *ágiles* (objetos de cálculo de referencias de subprocesamiento libre) que contienen punteros de interfaz a otros objetos.

Un objeto Agile no es consciente de la infraestructura COM subyacente en la que se ejecuta; en otras palabras, en qué apartamento, contexto y subproceso se está ejecutando. El objeto puede estar reteniendo en interfaces que son específicas de un apartamento o un contexto. Por esta razón, llamar a estas interfaces desde donde se ejecuta el componente ágil podría no funcionar siempre correctamente. La tabla de interfaz global evita este problema garantizando que se usa un proxy válido (o puntero directo) al objeto, en función de dónde se esté ejecutando el objeto Agile.

> [!Note]  
> La tabla de interfaz global no es portable en los límites del proceso o del equipo, por lo que no se puede utilizar en lugar del mecanismo normal de paso de parámetros.

 

Para obtener información sobre la creación y el uso de una tabla de interfaz global, vea los temas siguientes:

-   [Crear la tabla de interfaz global](creating-the-global-interface-table.md)
-   [Cuándo usar la tabla de interfaz global](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elegir el modelo de subprocesos](choosing-the-threading-model.md)
</dt> <dt>

[Apartamentos multiproceso](multithreaded-apartments.md)
</dt> <dt>

[Problemas de subprocesos de servidor en proceso](in-process-server-threading-issues.md)
</dt> <dt>

[Procesos, subprocesos y apartamentos](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicación multiproceso y de un solo subproceso](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartamentos de un solo subproceso](single-threaded-apartments.md)
</dt> </dl>

 

 




