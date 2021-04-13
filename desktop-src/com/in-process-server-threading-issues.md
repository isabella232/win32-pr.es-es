---
title: Problemas de subprocesos de In-Process Server
description: Problemas de subprocesos de In-Process Server
ms.assetid: 7bd6f62f-8c91-44bd-9a7f-d47988180eed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9d02af739eac11a6adae62de76be9078ee8e32
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "104421608"
---
# <a name="in-process-server-threading-issues"></a>Problemas de subprocesos de In-Process Server

Un servidor en proceso no llama a [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize), [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)o [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) para marcar su modelo de subprocesos. En el caso de objetos basados en archivos DLL o en proceso que reconocen subprocesos, debe establecer el modelo de subprocesos en el registro. El modelo predeterminado cuando no se especifica un modelo de subprocesos es de un solo subproceso por proceso. Para especificar un modelo, agregue el valor **ThreadingModel** a la clave [InProcServer32](inprocserver32.md) en el registro.

Los archivos DLL que admiten la creación de instancias de un objeto de clase deben implementar y exportar las funciones [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) y [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow). Cuando un cliente desea una instancia de la clase que admite el archivo DLL, una llamada a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (ya sea directamente o a través de una llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) llama a **DllGetClassObject** para obtener un puntero a su objeto de clase cuando el objeto se implementa en un archivo dll. Por lo tanto, **DllGetClassObject** debe ser capaz de proporcionar varios objetos de clase o un solo objeto seguro para subprocesos (básicamente, simplemente usando [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) / [**InterlockedDecrement**](/windows/desktop/api/winbase/nf-winbase-interlockeddecrement) en sus recuentos de referencias internas).

Como su nombre implica, se llama a [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow) para determinar si el archivo DLL que implementa está en uso, lo que permite que el llamador lo descargue de forma segura si no lo está. Las llamadas a [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) desde cualquier subproceso siempre enrutan a través del subproceso del apartamento principal para llamar a **DllCanUnloadNow**.

Al igual que otros servidores, los servidores en proceso pueden ser de un solo subproceso, de subproceso controlado o de subprocesamiento libre. Los clientes OLE pueden utilizar estos servidores, independientemente del modelo de subprocesos utilizado por ese cliente.

Todas las combinaciones de interoperabilidad del modelo de subprocesos se permiten entre clientes y objetos en proceso. La interacción entre un cliente y un objeto en proceso que usa diferentes modelos de subprocesos es exactamente igual que la interacción entre los clientes y los servidores fuera de proceso. En el caso de un servidor en proceso, cuando el modelo de subprocesos del cliente y el servidor en proceso difieren, COM debe interposese a sí mismo entre el cliente y el objeto.

Cuando se llama a un objeto en proceso que admite el modelo de un solo subproceso simultáneamente por varios subprocesos de un cliente, COM no puede permitir que los subprocesos del cliente accedan directamente al interfaceâ del objeto "el objeto no se diseñó para dicho acceso. En su lugar, COM debe asegurarse de que las llamadas se sincronizan y solo las realiza el subproceso de cliente que creó el objeto. Por lo tanto, COM crea el objeto en el apartamento principal del cliente y requiere que todos los demás apartamentos de cliente tengan acceso al objeto mediante el uso de servidores proxy.

Cuando un apartamento de subprocesamiento libre (modelo de Apartamento multiproceso) de un cliente crea un servidor en proceso de subproceso controlado, COM pone en marcha un subproceso "host" de modelo de apartamento de un solo subproceso en el cliente. Este subproceso de host creará el objeto y el puntero de interfaz se calculará de nuevo en el contenedor de subprocesos libres del cliente. Del mismo modo, cuando un apartamento de un solo subproceso en un cliente de modelo de Apartamento crea un servidor en proceso de subprocesamiento libre, COM pone en marcha un subproceso de host de subprocesamiento libre (Apartamento multiproceso en el que se creará el objeto y, a continuación, volverá a calcular las referencias al apartamento de un solo subproceso del cliente).

> [!Note]  
> En general, si diseña una interfaz personalizada en un servidor de proceso, también debe proporcionar el código de cálculo de referencias para que COM pueda calcular las referencias de la interfaz entre apartamentos de cliente.

 

COM ayuda a proteger el acceso a los objetos proporcionados por un archivo DLL de un solo subproceso, ya que requiere acceso desde el mismo contenedor de cliente en el que se crearon. Además, el mismo apartamento siempre debe tener acceso a todos los puntos de entrada de DLL (como [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) y [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)) y a los datos globales. COM crea estos objetos en el apartamento principal del cliente, lo que permite que el apartamento principal tenga acceso directo a los punteros del objeto. Las llamadas de los otros apartamentos usan el cálculo de referencias entre subprocesos para pasar del proxy al código auxiliar del apartamento principal y, a continuación, al objeto. Esto permite a COM sincronizar las llamadas al objeto. Las llamadas entre subprocesos son lentas, por lo que se recomienda volver a escribir estos servidores para admitir varios apartamentos.

Al igual que un servidor en proceso de un solo subproceso, un objeto proporcionado por un archivo DLL de modelo de apartamento debe ser accesible desde el mismo contenedor de cliente desde el que se creó. Sin embargo, los objetos proporcionados por este servidor se pueden crear en varios apartamentos del cliente, por lo que el servidor debe implementar sus puntos de entrada (como [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) y [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)) para el uso multiproceso. Por ejemplo, si dos apartamentos de un cliente intentan crear simultáneamente dos instancias del objeto en curso, ambos apartamentos pueden llamar simultáneamente a **DllGetClassObject** . Se debe escribir **DllCanUnloadNow** para que el archivo dll no se descargue mientras el código todavía se está ejecutando en el archivo dll.

Si el archivo DLL proporciona solo una instancia del generador de clases para crear todos los objetos, la implementación del generador de clases también se debe diseñar para uso multiproceso, ya que será accesible mediante varios apartamentos de cliente. Si el archivo DLL crea una nueva instancia del generador de clases cada vez que se llama a [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) , el generador de clases no necesita ser seguro para subprocesos.

Los objetos creados por el generador de clases no necesitan ser seguros para subprocesos. Una vez creado por un subproceso, siempre se obtiene acceso al objeto a través de ese subproceso y COM sincroniza todas las llamadas al objeto. El apartamento del modelo de apartamento de un cliente que crea este objeto obtendrá un puntero directo al objeto. Los apartamentos de cliente que son diferentes del apartamento en el que se creó el objeto deben tener acceso al objeto a través de servidores proxy. Estos proxy se crean cuando el cliente calcula las referencias de la interfaz entre sus apartamentos.

Cuando un valor **ThreadingModel** de dll en proceso se establece en "both", un objeto proporcionado por este archivo dll se puede crear y usar directamente (sin un proxy) en apartamentos de cliente de un solo subproceso o multiproceso. Sin embargo, solo se puede utilizar directamente dentro del apartamento en el que se creó. Para asignar el objeto a cualquier otro apartamento, se deben calcular las referencias del objeto. El objeto DLL debe implementar su propia sincronización y se puede tener acceso a ellos mediante varios apartamentos de cliente al mismo tiempo.

Para acelerar el rendimiento del acceso de subprocesamiento libre a objetos DLL en proceso, COM proporciona la función [**CoCreateFreeThreadedMarshaler**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) . Esta función crea un objeto de cálculo de referencias de subprocesamiento libre que se puede Agregar con un objeto de servidor en proceso. Cuando un apartamento de cliente en el mismo proceso necesita tener acceso a un objeto de otro apartamento, la agregación del contador de referencias de subprocesamiento libre proporciona al cliente un puntero directo al objeto de servidor, en lugar de a un proxy, cuando el cliente calcula las referencias de la interfaz del objeto a un apartamento diferente. El cliente no necesita realizar ninguna sincronización. Esto solo funciona dentro del mismo proceso. el cálculo de referencias estándar se utiliza para una referencia al objeto que se envía a otro proceso.

Un objeto proporcionado por una DLL en proceso que solo admite subprocesos libres es un objeto de subprocesamiento libre. Implementa su propia sincronización y se puede tener acceso a ella mediante varios subprocesos de cliente al mismo tiempo. Este servidor no calcula las referencias de interfaces entre subprocesos, por lo que este servidor se puede crear y usar directamente (sin un proxy) mediante apartamentos multiproceso en un cliente. Los apartamentos de un solo subproceso que lo crean tendrán acceso a él a través de un proxy.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a interfaces entre apartamentos](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Elegir el modelo de subprocesos](choosing-the-threading-model.md)
</dt> <dt>

[Apartamentos multiproceso](multithreaded-apartments.md)
</dt> <dt>

[Procesos, subprocesos y apartamentos](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicación multiproceso y de un solo subproceso](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartamentos de un solo subproceso](single-threaded-apartments.md)
</dt> </dl>

 

 