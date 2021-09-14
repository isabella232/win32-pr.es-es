---
title: In-Process de subprocesos de servidor
description: In-Process de subprocesos de servidor
ms.assetid: 7bd6f62f-8c91-44bd-9a7f-d47988180eed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9d02af739eac11a6adae62de76be9078ee8e32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060927"
---
# <a name="in-process-server-threading-issues"></a>In-Process de subprocesos de servidor

Un servidor en proceso no llama a [**CoInitialize,**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)o [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) para marcar su modelo de subprocesos. En el caso de los objetos basados en DLL o en proceso que tienen en cuenta los subprocesos, debe establecer el modelo de subprocesos en el Registro. El modelo predeterminado cuando no se especifica un modelo de subprocesos es un único subproceso por proceso. Para especificar un modelo, agregue el valor **ThreadingModel** a la [clave InprocServer32](inprocserver32.md) en el Registro.

Los archivos DLL que admiten la creación de instancias de un objeto de clase deben implementar y exportar las funciones [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) y [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow). Cuando un cliente quiere una instancia de la clase que admite el archivo DLL, una llamada a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (ya sea directamente o a través de una llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) llama a **DllGetClassObject** para obtener un puntero a su objeto de clase cuando el objeto se implementa en un archivo DLL. Por lo tanto, **DllGetClassObject** debe ser capaz de entregar varios objetos de clase o un único objeto seguro para subprocesos (básicamente simplemente usando [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) / [**InterlockedDecrement en**](/windows/desktop/api/winbase/nf-winbase-interlockeddecrement) sus recuentos de referencias internos).

Como su nombre implica, se llama a [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow) para determinar si el archivo DLL que lo implementa está en uso, lo que permite al autor de la llamada descargarlo de forma segura si no lo está. Las llamadas [**a CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) desde cualquier subproceso siempre se enrutan a través del subproceso del apartamento principal para llamar **a DllCanUnloadNow.**

Al igual que otros servidores, los servidores en proceso pueden ser de un solo subproceso, de tipo apartment-thread o free-threaded. Todos los clientes OLE pueden usar estos servidores, independientemente del modelo de subprocesos usado por ese cliente.

Se permiten todas las combinaciones de interoperabilidad del modelo de subprocesos entre clientes y objetos en proceso. La interacción entre un cliente y un objeto en proceso que usan modelos de subprocesamiento diferentes es exactamente igual que la interacción entre los clientes y los servidores fuera de proceso. Para un servidor en proceso, cuando el modelo de subprocesos del cliente y el servidor en proceso difieren, COM debe interponerse entre el cliente y el objeto .

Cuando varios subprocesos de un cliente llaman simultáneamente a un objeto en proceso que admite el modelo de subproceso único, COM no puede permitir que los subprocesos de cliente accedan directamente a la interfaz del objeto. El objeto no se diseñó para dicho acceso. En su lugar, COM debe asegurarse de que las llamadas se sincronizan y solo las realiza el subproceso de cliente que creó el objeto. Por lo tanto, COM crea el objeto en el apartamento principal del cliente y requiere que todos los demás departamentos de cliente accedan al objeto mediante servidores proxy.

Cuando un apartamento de subproceso libre (modelo de apartamento multiproceso) en un cliente crea un servidor en proceso de subprocesos de apartamento, COM gira un subproceso "host" del modelo de apartamento de un solo subproceso en el cliente. Este subproceso host creará el objeto y el puntero de interfaz se serializará de nuevo al apartamento de subproceso libre del cliente. De forma similar, cuando un apartamento de un solo subproceso en un cliente de modelo de apartamento crea un servidor en proceso de subproceso libre, COM gira un subproceso de host de subproceso libre (apartamento multiproceso en el que se creará el objeto y, a continuación, se serializará de nuevo al apartamento de un solo subproceso del cliente).

> [!Note]  
> En general, si diseña una interfaz personalizada en un servidor en proceso, también debe proporcionar el código de serialización para ella para que COM pueda serializar la interfaz entre los departamentos de cliente.

 

COM ayuda a proteger el acceso a los objetos proporcionados por un archivo DLL de un solo subproceso, ya que requiere acceso desde el mismo apartamento cliente en el que se crearon. Además, el mismo apartamento siempre debe tener acceso a todos los puntos de entrada de DLL (como [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) y [**DllCanUnloadNow)**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)y a los datos globales. COM crea estos objetos en el apartamento principal del cliente, lo que proporciona al apartamento principal acceso directo a los punteros del objeto. Las llamadas de los otros departamentos usan la serialización interproceso para ir desde el proxy al código auxiliar del apartamento principal y, a continuación, al objeto . Esto permite que COM sincronice las llamadas al objeto . Las llamadas entre subprocesos son lentas, por lo que se recomienda volver a escribir estos servidores para admitir varios departamentos.

Al igual que un servidor en proceso de un solo subproceso, el mismo apartamento cliente desde el que se creó debe tener acceso a un objeto proporcionado por un archivo DLL de modelo de apartamento. Sin embargo, los objetos proporcionados por este servidor se pueden crear en varios departamentos del cliente, por lo que el servidor debe implementar sus puntos de entrada (como [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) y [**DllCanUnloadNow)**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)para su uso multiproceso. Por ejemplo, si dos departamentos de un cliente intentan crear dos instancias del objeto en proceso simultáneamente, ambos departamentos pueden llamar a **DllGetClassObject** simultáneamente. **DllCanUnloadNow** debe escribirse para que el archivo DLL no se descargue mientras el código se sigue ejecutando en el archivo DLL.

Si el archivo DLL proporciona solo una instancia del generador de clases para crear todos los objetos, la implementación del generador de clases también debe diseñarse para uso multiproceso, ya que varios departamentos de cliente tendrán acceso a él. Si el archivo DLL crea una nueva instancia del generador de clases cada vez que se llama a [**DllGetClassObject,**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) el generador de clases no debe ser seguro para subprocesos.

Los objetos creados por el generador de clases no deben ser seguros para subprocesos. Una vez creado por un subproceso, siempre se accede al objeto a través de ese subproceso y COM sincroniza todas las llamadas al objeto. El apartamento del modelo de apartamento de un cliente que crea este objeto recibirá un puntero directo al objeto . Los departamentos de cliente que son diferentes del apartamento en el que se creó el objeto deben tener acceso al objeto a través de servidores proxy. Estos servidores proxy se crean cuando el cliente serializa la interfaz entre sus departamentos.

Cuando un valor de **ThreadingModel** de DLL en proceso se establece en "Both", un objeto proporcionado por este archivo DLL se puede crear y usar directamente (sin un proxy) en los departamentos de cliente multiproceso o de subproceso único. Sin embargo, solo se puede usar directamente dentro del apartamento en el que se creó. Para proporcionar el objeto a cualquier otro apartamento, se deben calcular las referencias del objeto. El objeto DLL debe implementar su propia sincronización y varios departamentos de cliente pueden acceder a él al mismo tiempo.

Para acelerar el rendimiento del acceso sin subprocesos a objetos DLL en proceso, COM proporciona la función [**CoCreateFreeThreadedMarsthread.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) Esta función crea un objeto de serialización de subproceso libre que se puede agregar con un objeto de servidor en proceso. Cuando un apartamento de cliente en el mismo proceso necesita acceso a un objeto en otro apartamento, la agregación del serializador de subproceso libre proporciona al cliente un puntero directo al objeto de servidor, en lugar de a un proxy, cuando el cliente serializa la interfaz del objeto en un apartamento diferente. El cliente no necesita realizar ninguna sincronización. Esto solo funciona dentro del mismo proceso; La serialización estándar se usa para una referencia al objeto que se envía a otro proceso.

Un objeto proporcionado por un archivo DLL en proceso que solo admite el subprocesamiento libre es un objeto de subproceso libre. Implementa su propia sincronización y a la que pueden acceder varios subprocesos de cliente al mismo tiempo. Este servidor no serializa interfaces entre subprocesos, por lo que este servidor se puede crear y usar directamente (sin un proxy) solo por los departamentos multiproceso de un cliente. Los departamentos de un solo subproceso que lo crean tendrán acceso a él a través de un proxy.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a interfaces entre departamentos](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Elección del modelo de subprocesos](choosing-the-threading-model.md)
</dt> <dt>

[Departamentos multiproceso](multithreaded-apartments.md)
</dt> <dt>

[Procesos, subprocesos y departamentos](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicación multiproceso y de subproceso único](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Departamentos de un solo subproceso](single-threaded-apartments.md)
</dt> </dl>

 

 