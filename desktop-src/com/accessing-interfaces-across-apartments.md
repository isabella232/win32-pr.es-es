---
title: Acceso a interfaces entre departamentos
description: Acceso a interfaces entre departamentos
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626707daf721aee3b440bb79ba2d1e084d154a98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060964"
---
# <a name="accessing-interfaces-across-apartments"></a>Acceso a interfaces entre departamentos

COM proporciona una manera de que cualquier apartamento de un proceso obtenga acceso a una interfaz implementada en un objeto en cualquier otro apartamento del proceso. Esto se realiza a través de [**la interfaz IGlobalInterfaceTable.**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) Esta interfaz tiene tres métodos, que permiten hacer lo siguiente:

-   Registre una interfaz como *una interfaz global* (en todo el proceso).
-   Obtenga un puntero a esa interfaz desde cualquier otro apartamento a través de una cookie.
-   Revocar el registro global de una interfaz.

La interfaz [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) es una manera eficaz de que un proceso almacene un puntero de interfaz en una ubicación  de memoria a la que se puede acceder desde varios departamentos dentro del proceso, como variables de todo el proceso y objetos ágiles (objetos serializados y de subproceso libre) que contienen punteros de interfaz a otros objetos.

Un objeto ágil no es consciente de la infraestructura COM subyacente en la que se ejecuta. es decir, en qué apartamento, contexto y subproceso se está ejecutando. El objeto puede estar manteniendo en interfaces que son específicas de un apartamento o contexto. Por este motivo, llamar a estas interfaces desde cualquier lugar donde se ejecute el componente agile podría no funcionar siempre correctamente. La tabla de interfaz global evita este problema al garantizar que se usa un proxy válido (o puntero directo) al objeto, en función de dónde se ejecute el objeto ágil.

> [!Note]  
> La tabla de interfaz global no es portátil a través de los límites del proceso o de la máquina, por lo que no se puede usar en lugar del mecanismo normal de paso de parámetros.

 

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

 

 




