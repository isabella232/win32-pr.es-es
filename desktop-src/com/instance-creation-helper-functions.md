---
title: Funciones auxiliares de creación de instancias
description: Funciones auxiliares de creación de instancias
ms.assetid: 0b9b7bcf-f0f0-42c4-945e-63a532640d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84956f6040aaba13b46dea92bea611a49d5d8de3
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369516"
---
# <a name="instance-creation-helper-functions"></a>Funciones auxiliares de creación de instancias

En versiones anteriores de COM, el mecanismo principal usado para crear una instancia de objeto era la [**función CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Esta función encapsula el proceso de creación de un objeto de clase, usándose para crear una nueva instancia y liberando el objeto de clase. Otra función de este tipo es la clase [**OleCreate**](/windows/desktop/api/ole/nf-ole-olecreate)más específica, el asistente de documentos compuestos OLE que crea un objeto de clase y recupera un puntero a un objeto solicitado.

Para suavizar el proceso de creación de instancias en sistemas distribuidos, COM ha introducido cuatro nuevos mecanismos de creación de instancias importantes:

-   Monikers de clase [ **e IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator)
-   [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)

Un moniker de clase permite identificar la clase de un objeto y normalmente se usa con otro moniker, como un moniker de archivo, para indicar la ubicación del objeto. Esto le permite enlazar a un objeto y especificar el servidor que se va a iniciar para ese objeto. Los monikers de clase también se pueden componer a la derecha de monikers que admiten el enlace a la [**interfaz IClassActivator.**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) Para obtener más información, vea [Class Monikers](class-monikers.md).

[**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) extiende [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para que sea posible crear un único objeto no inicializado asociado al CLSID especificado en un equipo remoto especificado. Además, en lugar de solicitar una sola interfaz y obtener un único puntero a esa interfaz, **CoCreateInstanceEx** permite consultar varias interfaces y (si está disponible) recibir punteros a ellas en un único recorrido de ida y vuelta, lo que permite menos recorridos de ida y vuelta entre máquinas. Esto puede hacer que la interacción remota de objetos sea mucho más eficaz. Para ello, la función usa una matriz de [**estructuras MULTI \_ QI.**](/windows/win32/api/objidlbase/ns-objidlbase-multi_qi)

La creación de un objeto a través de [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) requiere que el objeto se inicialice mediante una llamada a una de las interfaces de inicialización (como [**IPersistStorage::Load).**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-load) Las funciones auxiliares [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) y [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) encapsulan la potencia de creación de instancias de **CoCreateInstanceEx** y la inicialización, la primera desde un archivo y la segunda desde un almacenamiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear un objeto a través de un objeto de clase](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 