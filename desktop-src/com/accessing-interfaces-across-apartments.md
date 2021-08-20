---
title: Acceso a interfaces entre departamentos
description: Acceso a interfaces entre departamentos
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89e82fa29e768328e6c110349627d32e92ab010ce61fdf64141ad3ca7fe9a54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048923"
---
# <a name="accessing-interfaces-across-apartments"></a>Acceso a interfaces entre departamentos

COM proporciona una manera de que cualquier apartamento de un proceso obtenga acceso a una interfaz implementada en un objeto en cualquier otro apartamento del proceso. Esto se realiza a través de la [**interfaz IGlobalInterfaceTable.**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) Esta interfaz tiene tres métodos, que permiten hacer lo siguiente:

-   Registre una interfaz como *una interfaz global* (en todo el proceso).
-   Obtenga un puntero a esa interfaz desde cualquier otro apartamento a través de una cookie.
-   Revoque el registro global de una interfaz.

La interfaz [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) es una manera eficaz de que un proceso almacene un puntero de interfaz en una ubicación de memoria a la que se pueda acceder desde varios departamentos dentro del proceso, como variables para todo el proceso y objetos *ágiles* (objetos sin subprocesos y serializados) que contienen punteros de interfaz a otros objetos.

Un objeto agile no es consciente de la infraestructura COM subyacente en la que se ejecuta. en otras palabras, en qué apartamento, contexto y subproceso se está ejecutando. El objeto puede estar manteniendo en las interfaces que son específicas de un apartamento o contexto. Por esta razón, llamar a estas interfaces desde cualquier lugar donde se ejecute el componente agile podría no funcionar siempre correctamente. La tabla de interfaz global evita este problema al garantizar que se usa un proxy válido (o puntero directo) al objeto, en función de dónde se ejecute el objeto ágil.

> [!Note]  
> La tabla de interfaz global no es portátil a través de los límites de proceso o máquina, por lo que no se puede usar en lugar del mecanismo normal de paso de parámetros.

 

Para obtener información sobre cómo crear y usar una tabla de interfaz global, vea los temas siguientes:

-   [Creación de la tabla de interfaz global](creating-the-global-interface-table.md)
-   [Cuándo usar la tabla de interfaz global](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elección del modelo de subprocesos](choosing-the-threading-model.md)
</dt> <dt>

[Departamentos multiproceso](multithreaded-apartments.md)
</dt> <dt>

[Problemas de subprocesos del servidor en proceso](in-process-server-threading-issues.md)
</dt> <dt>

[Procesos, subprocesos y departamentos](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicación multiproceso y de subproceso único](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Departamentos de un solo subproceso](single-threaded-apartments.md)
</dt> </dl>

 

 




