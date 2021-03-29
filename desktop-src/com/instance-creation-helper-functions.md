---
title: Funciones auxiliares de creación de instancia
description: Funciones auxiliares de creación de instancia
ms.assetid: 0b9b7bcf-f0f0-42c4-945e-63a532640d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84956f6040aaba13b46dea92bea611a49d5d8de3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078415"
---
# <a name="instance-creation-helper-functions"></a>Funciones auxiliares de creación de instancia

En las versiones anteriores de COM, el mecanismo principal usado para crear una instancia de objeto era la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) . Esta función encapsula el proceso de creación de un objeto de clase, con el fin de crear una nueva instancia y liberar el objeto de clase. Otra función de este tipo es el [**OleCreate**](/windows/desktop/api/ole/nf-ole-olecreate)más específico, la aplicación auxiliar de documento compuesto OLE que crea un objeto de clase y recupera un puntero a un objeto solicitado.

Para suavizar el proceso de creación de instancias en sistemas distribuidos, COM ha introducido cuatro mecanismos de creación de instancia nuevos importantes:

-   Monikers y [ **IClassActivator** de clase](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator)
-   [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)

Un moniker de clase permite identificar la clase de un objeto y se utiliza normalmente con otro moniker, como un moniker de archivo, para indicar la ubicación del objeto. Esto le permite enlazar a un objeto y especificar el servidor que se va a iniciar para ese objeto. Los monikers de clase también se pueden componer a la derecha de monikers que admiten enlaces a la interfaz [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) . Para obtener más información, vea [monikers de clase](class-monikers.md).

[**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) extiende [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para que pueda crear un único objeto sin inicializar asociado al CLSID dado en un equipo remoto especificado. Además, en lugar de solicitar una sola interfaz y obtener un único puntero a esa interfaz, **CoCreateInstanceEx** permite consultar varias interfaces y, si está disponible, recibir punteros a ellas en un solo recorrido de ida y vuelta, lo que permite menos recorridos de ida y vuelta entre máquinas. Esto puede hacer que la interacción remota de objetos sea mucho más eficaz. Para ello, la función utiliza una matriz de estructuras [**multi \_ Qi**](/windows/win32/api/objidlbase/ns-objidlbase-multi_qi) .

La creación de un objeto a través de [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) todavía requiere que el objeto se inicialice a través de una llamada a una de las interfaces de inicialización (como [**IPersistStorage:: Load**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-load)). Las funciones auxiliares [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) y [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) encapsulan la potencia de creación de la instancia de **CoCreateInstanceEx** y la inicialización, la primera de un archivo y la última de un almacenamiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear un objeto a través de un objeto de clase](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 