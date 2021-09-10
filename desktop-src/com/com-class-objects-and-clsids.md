---
title: Objetos de clase COM y CLSID
description: Un servidor COM se implementa como una clase COM.
ms.assetid: 0073acdf-38a8-4f1a-aa26-379456a95fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbfde2f379c4c7589db4cde283c8c67d720b21d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369507"
---
# <a name="com-class-objects-and-clsids"></a>Objetos de clase COM y CLSID

Un servidor COM se implementa como una clase COM. Una *clase COM* es una implementación de un grupo de interfaces en código ejecutado cada vez que se interactúa con un objeto determinado. Hay una distinción importante entre una clase de C++ y una clase COM: en C++, una clase es un tipo, mientras que una clase COM es simplemente una definición del objeto y no lleva ningún tipo, aunque un programador de C++ podría implementarla mediante una clase de C++. COM está diseñado para permitir que distintas aplicaciones utilicen una clase, incluidas las aplicaciones escritas sin conocer la existencia de esa clase en particular. Por lo tanto, el código de clase para un tipo determinado de objeto existe en una biblioteca vinculada dinámica (DLL) o en otra aplicación ejecutable (EXE).

Cada clase COM se identifica mediante un *CLSID*, un GUID único de 128 bits, que el servidor debe registrar. COM usa este CLSID, a petición de un cliente, para asociar datos específicos con el archivo DLL o EXE que contiene el código que implementa la clase , creando así una instancia del objeto .

Para los clientes y servidores del mismo equipo, el CLSID del servidor es todo lo que el cliente necesita. En cada equipo, COM mantiene una base de datos (usa el registro del sistema en las plataformas Microsoft Windows y Macintosh) de todos los CLID para los servidores instalados en el sistema. Se trata de una asignación entre cada CLSID y la ubicación del archivo DLL o EXE que aloja el código de ese CLSID. COM consulta esta base de datos cada vez que un cliente quiere crear una instancia de una clase COM y usar sus servicios, por lo que el cliente nunca necesita conocer la ubicación absoluta del código en el equipo.

Para los sistemas distribuidos, COM proporciona entradas del Registro que permiten que un servidor remoto se registre para que lo use un cliente. Aunque las aplicaciones solo necesitan conocer el CLSID de un servidor, ya que pueden confiar en el Registro para localizar el servidor, COM permite a los clientes invalidar las entradas del Registro y especificar ubicaciones de servidor para aprovechar al máximo la red. (Vea [Buscar un objeto remoto).](locating-a-remote-object.md)

La manera básica de crear una instancia de una clase es a través de un objeto *de clase COM*. Se trata simplemente de un objeto intermedio que admite funciones comunes a la creación de nuevas instancias de una clase determinada. La mayoría de los objetos de clase que se usan para crear objetos a partir de un CLSID admiten la [**interfaz IClassFactory,**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) una interfaz que incluye el [**método CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) importante. Implemente una **interfaz IClassFactory** para cada clase de objeto que ofrezca para crear instancias. (Para obtener más información sobre cómo implementar **IClassFactory,** vea [Implementar IClassFactory).](implementing-iclassfactory.md)

> [!Note]  
> Los servidores que admiten alguna otra interfaz de generador de clases personalizadas no son necesarios para admitir [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) específicamente. Sin embargo, las llamadas a funciones de activación que no son [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (como [**CoCreateInstanceEx)**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)requieren que el servidor admita **IClassFactory**.

 

Cuando un cliente quiere crear una instancia del objeto del servidor, usa el CLSID del objeto deseado en una llamada a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject). (Esta llamada puede ser directa o implícita, a través de una de las funciones auxiliares de creación de objetos). Esta función busca el código asociado al CLSID, crea un objeto de clase y proporciona un puntero a la interfaz solicitada. (**CoGetClassObject** toma un *parámetro riid* que especifica el puntero de interfaz deseado del cliente).

> [!Note]  
> COM tiene solo algunas funciones en las que se han creado muchas de las demás. El más importante de ellos es probablemente [**CoGetClassObject,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)que subyace a todas las funciones de creación de instancias.

 

Con este puntero, el autor de la llamada puede crear una instancia del objeto y recuperar un puntero a una interfaz solicitada en el objeto . Normalmente se trata de una interfaz de inicialización, que se usa para activar el objeto (ponerlo en estado en ejecución) para que el cliente pueda realizar cualquier trabajo con el objeto que quiera. Con las funciones básicas de COM, el cliente también debe tener cuidado para liberar todos los punteros de objeto.

Otro mecanismo para activar instancias de objeto es a través del moniker de clase. Los monikers de clase se enlazan al objeto de clase de la clase para la que se crean. Para obtener más información, vea [Class Monikers](class-monikers.md).

COM proporciona varias funciones auxiliares que reducen el trabajo de creación de instancias de objeto. Se describen en Funciones [auxiliares de creación de instancias](instance-creation-helper-functions.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear un objeto a través de un objeto de clase](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 