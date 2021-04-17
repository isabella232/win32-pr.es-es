---
title: Objetos de clase COM y CLSID
description: Un servidor COM se implementa como una clase COM.
ms.assetid: 0073acdf-38a8-4f1a-aa26-379456a95fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbfde2f379c4c7589db4cde283c8c67d720b21d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714483"
---
# <a name="com-class-objects-and-clsids"></a>Objetos de clase COM y CLSID

Un servidor COM se implementa como una clase COM. Una *clase com* es una implementación de un grupo de interfaces en el código que se ejecuta cada vez que interactúa con un objeto determinado. Hay una diferencia importante entre una clase de C++ y una clase COM: en C++, una clase es un tipo, mientras que una clase COM simplemente es una definición del objeto y no incluye ningún tipo, aunque un programador de C++ podría implementarla mediante una clase de C++. COM está diseñado para permitir el uso de una clase por parte de aplicaciones diferentes, incluidas las aplicaciones escritas sin conocimiento de la existencia de esa clase concreta. Por lo tanto, el código de clase para un tipo de objeto determinado existe en una biblioteca dinámica vinculada (DLL) o en otra aplicación ejecutable (EXE).

Cada clase COM se identifica mediante un *CLSID*, un GUID único de 128 bits, que el servidor debe registrar. COM utiliza este CLSID, en la solicitud de un cliente, para asociar datos específicos con el archivo DLL o EXE que contiene el código que implementa la clase, lo que crea una instancia del objeto.

En el caso de los clientes y servidores del mismo equipo, el CLSID del servidor es todo lo que necesita el cliente. En cada equipo, COM mantiene una base de datos (hace uso del registro del sistema en las plataformas de Microsoft Windows y Macintosh) de todos los CLSID de los servidores instalados en el sistema. Se trata de una asignación entre cada CLSID y la ubicación del archivo DLL o EXE que hospeda el código para ese CLSID. COM consulta esta base de datos cada vez que un cliente desea crear una instancia de una clase COM y usar sus servicios, por lo que el cliente nunca necesita conocer la ubicación absoluta del código en el equipo.

En el caso de los sistemas distribuidos, COM proporciona entradas del registro que permiten que un servidor remoto se registre para su uso por parte de un cliente. Mientras que las aplicaciones solo necesitan conocer el CLSID de un servidor, ya que pueden basarse en el registro para encontrar el servidor, COM permite a los clientes invalidar las entradas del registro y especificar las ubicaciones del servidor para sacar el máximo partido de la red. (Vea [localizar un objeto remoto](locating-a-remote-object.md)).

La manera básica de crear una instancia de una clase es a través de un *objeto de clase* com. Esto es simplemente un objeto intermedio que admite funciones comunes a la creación de nuevas instancias de una clase determinada. La mayoría de los objetos de clase usados para crear objetos a partir de un CLSID admiten la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , una interfaz que incluye el método [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) importante. Se implementa una interfaz **IClassFactory** para cada clase de objeto del que se va a crear una instancia. (Para obtener más información acerca de la implementación de **IClassFactory**, vea [implementar IClassFactory](implementing-iclassfactory.md)).

> [!Note]  
> No es necesario que los servidores que admiten otras interfaces de generador de clases personalizadas admitan [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) específicamente. Sin embargo, las llamadas a funciones de activación que no sean [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (como [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)) requieren que el servidor admita **IClassFactory**.

 

Cuando un cliente desea crear una instancia del objeto del servidor, usa el CLSID del objeto deseado en una llamada a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject). (Esta llamada puede ser directa o implícita, a través de una de las funciones auxiliares de creación de objetos). Esta función busca el código asociado al CLSID y crea un objeto de clase, y proporciona un puntero a la interfaz solicitada. (**CoGetClassObject** toma un parámetro *riid* que especifica el puntero de interfaz deseado del cliente).

> [!Note]  
> COM tiene solo algunas funciones en las que se han creado muchos de los demás. El más importante es probablemente [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), que subyace a todas las funciones de creación de instancias.

 

Con este puntero, el autor de la llamada puede crear una instancia del objeto y recuperar un puntero a una interfaz solicitada en el objeto. Normalmente, se trata de una interfaz de inicialización que se usa para activar el objeto (ponerlo en el estado de ejecución) de modo que el cliente pueda realizar cualquier trabajo con el objeto que desee. Con las funciones básicas de COM, el cliente también debe tener cuidado de liberar todos los punteros de objeto.

Otro mecanismo para activar instancias de objeto es a través del moniker de clase. Los monikers de clase se enlazan al objeto de clase de la clase para la que se crean. Para obtener más información, vea [monikers de clase](class-monikers.md).

COM proporciona varias funciones auxiliares que reducen el trabajo de creación de instancias de objeto. Se describen en [funciones auxiliares](instance-creation-helper-functions.md)para la creación de instancias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear un objeto a través de un objeto de clase](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 