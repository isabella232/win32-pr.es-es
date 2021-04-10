---
title: Información técnica de COM
ms.assetid: 519c87cc-b442-4187-af2a-124a1e4e8b49
description: 'Más información sobre: información técnica de COM'
keywords:
- Información técnica de COM COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be5dc95ffae5166d86cd8110cab1a6b90e6ffa5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153031"
---
# <a name="com-technical-overview"></a>Información técnica de COM

En este tema se proporciona información general sobre el modelo de objetos componentes (COM) de Microsoft:

-   [Introducción a COM](#introduction-to-com)
-   [Objetos e interfaces](#objects-and-interfaces)
-   [Implementación de interfaz](#interface-implementation)
-   [La interfaz IUnknown](#the-iunknown-interface)
-   [El modelo cliente/servidor](#the-clientserver-model)
-   [Administrador de control de servicios](#service-control-manager)
-   [Reusabilidad](#reusability)
-   [Objetos de almacenamiento y flujo](#storage-and-stream-objects)
-   [Transferencia de datos](#data-transfer)
-   [Comunicación remota](#remoting)
-   [Seguridad](#security)
-   [Temas relacionados](#related-topics)

## <a name="introduction-to-com"></a>Introducción a COM

El modelo de objetos componentes (COM) de Microsoft define un estándar de interoperabilidad binaria para crear bibliotecas de software reutilizables que interactúan en tiempo de ejecución. Puede usar las bibliotecas COM sin el requisito de compilarlas en la aplicación. COM es la base de una serie de productos y tecnologías de Microsoft, como Windows Media Player y Windows Server.

COM define un estándar binario que se aplica a muchos sistemas operativos y plataformas de hardware. En lo que se refiere a la informática de red, COM define un protocolo y un formato de conexión estándar para la interacción entre los objetos que se ejecutan en diferentes plataformas de hardware. COM es independiente del lenguaje de implementación, lo que significa que se pueden crear bibliotecas COM mediante lenguajes de programación diferentes, como C++ y los del .NET Framework.

La especificación COM proporciona todos los conceptos fundamentales que permiten la reutilización de software multiplataforma:

-   Estándar binario para las llamadas de función entre componentes.
-   Aprovisionamiento para agrupaciones fuertemente tipadas de funciones en interfaces.
-   Una interfaz base que proporciona polimorfismo, detección de características y seguimiento de la duración de los objetos.
-   Mecanismo que identifica de forma única los componentes y sus interfaces.
-   Un cargador de componentes que crea instancias de componente a partir de una implementación.

COM tiene varias partes que funcionan conjuntamente para habilitar la creación de aplicaciones que se crean a partir de componentes reutilizables:

-   *Sistema host* que proporciona un entorno en tiempo de ejecución que se ajusta a la especificación com.
-   *Interfaces* que definen contratos de características y *componentes* que implementan interfaces.
-   *Servidores* que proporcionan componentes al sistema y *clientes* que usan las características proporcionadas por los componentes de.
-   Un *registro* que realiza un seguimiento de dónde se implementan los componentes en hosts locales y remotos.
-   *Administrador de control de servicios* que busca componentes en hosts locales y remotos y conecta servidores a los clientes.
-   Un protocolo de *almacenamiento estructurado* que define cómo navegar por el contenido de los archivos en el sistema de archivos del host.

Habilitar la reutilización de código entre hosts y plataformas es fundamental para COM. Una implementación de interfaz reutilizable se denomina *componente*, un *objeto de componente* o un *objeto com*. Un componente implementa una o más interfaces COM.

Puede definir una biblioteca COM personalizada diseñando las interfaces que implementa la biblioteca. Los consumidores de la biblioteca pueden detectar y usar sus características sin tener que conocer los detalles de implementación e implementación de la biblioteca.

## <a name="objects-and-interfaces"></a>Objetos e interfaces

Un objeto COM expone sus características a través de una *interfaz*, que es una colección de funciones miembro. Una interfaz COM define el comportamiento esperado y las responsabilidades de un componente, y especifica un contrato fuertemente tipado que proporciona un conjunto pequeño de operaciones relacionadas. Toda la comunicación entre los componentes COM se produce a través de las interfaces, y todos los servicios que ofrece un componente se exponen a través de su interfaz. Un llamador solo puede tener acceso a las funciones miembro de interfaz. El estado interno no está disponible para un llamador a menos que se exponga en la interfaz.

Las interfaces están fuertemente tipadas. Cada interfaz tiene su propio identificador de interfaz único, denominado IID, que elimina las colisiones que podrían producirse con nombres legibles para el usuario. El IID es un identificador único global (GUID), que es el mismo que el identificador único universal (UUID) definido por el entorno de computación distribuida (DCE) de Open Software Foundation (OSF). Al crear una nueva interfaz, debe crear un nuevo identificador para esa interfaz. Cuando un llamador usa una interfaz, debe utilizar el identificador único. Esta identificación explícita mejora la solidez al eliminar los conflictos de nomenclatura que darían lugar a errores en tiempo de ejecución.

Al definir una nueva interfaz, puede crear una definición de interfaz mediante el lenguaje de definición de interfaz (IDL). A partir de esta definición de interfaz, el compilador IDL de Microsoft genera archivos de encabezado para que los usen las aplicaciones que usan la interfaz y el código fuente para controlar las llamadas a procedimientos remotos. El IDL proporcionado por Microsoft se basa en extensiones simples a DCE IDL, un estándar del sector para la informática distribuida basada en la llamada a procedimiento remoto (RPC). IDL es una herramienta para la comodidad del diseñador de interfaces y no es fundamental para la interoperabilidad COM. Con IDL, no es necesario crear archivos de encabezado manualmente para cada entorno de programación. Para obtener más información, vea [definir interfaces com](defining-com-interfaces.md).

La herencia se usa con moderación en las interfaces COM. COM solo admite la herencia de interfaz para reutilizar un contrato asociado a una interfaz base. COM no admite la herencia selectiva; por consiguiente, si una interfaz hereda de otra, incluye todas las funciones que define la interfaz base. Además, las interfaces solo utilizan la herencia única, en lugar de la herencia múltiple, para obtener funciones de una interfaz base.

## <a name="interface-implementation"></a>Implementación de interfaz

No se puede crear una instancia de una interfaz COM por sí misma. En su lugar, se crea una instancia de una clase que implementa la interfaz. En C++, una interfaz COM se modela como una *clase base abstracta*, lo que significa que la interfaz es una clase de C++ que solo contiene funciones miembro virtuales puras. Una biblioteca de C++ implementa objetos COM heredando las firmas de función miembro de una o varias interfaces, invalidando cada función miembro y proporcionando una implementación para cada función.

Puede usar cualquier lenguaje de programación que admita el concepto de punteros de función para implementar una interfaz COM. Por ejemplo, en C, una interfaz es una estructura que contiene un puntero a una tabla de punteros de función, uno para cada método de la interfaz.

Cuando se implementa una interfaz, la clase debe proporcionar una implementación para cada función de la interfaz. Si la clase no tiene ningún trabajo que hacer en una función de interfaz, la implementación puede ser una sola instrucción return.

Una clase COM se identifica mediante el uso de un identificador de clase (CLSID) de 128 bits único que asocia una clase a una implementación determinada en el sistema de archivos, que para Windows es una DLL o un archivo EXE. Un CLSID es un GUID, lo que significa que ninguna otra clase tiene el mismo CLSID. El uso de identificadores de clase únicos evita los conflictos de nombres entre las clases. Por ejemplo, dos proveedores diferentes pueden escribir una clase denominada CStack, pero ambas clases tienen un CLSID único, por lo que se evita cualquier posibilidad de una colisión.

Puede obtener un nuevo CLSID mediante la función [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) o mediante una herramienta de creación de com, como Visual Studio, que llama a esta función internamente.

## <a name="the-iunknown-interface"></a>La interfaz IUnknown

Todas las interfaces COM heredan de la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . La interfaz **IUnknown** contiene las operaciones com fundamentales para el polimorfismo y la administración de la duración de la instancia. La interfaz **IUnknown** tiene tres funciones miembro, denominadas [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Todos los objetos COM son necesarios para implementar la interfaz **IUnknown** .

La función miembro [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) proporciona el polimorfismo para com. Llame a **QueryInterface** para determinar en tiempo de ejecución si un objeto com admite una interfaz determinada. El objeto COM devuelve un puntero de interfaz en el `ppvObject` parámetro si implementa la interfaz solicitada; en caso contrario, devuelve `NULL` . La función miembro **QueryInterface** habilita la navegación entre todas las interfaces que admite un objeto com.

La duración de una instancia del objeto COM se controla mediante su *recuento de referencias*. [**Las funciones miembro**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) y [](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) controlan el recuento. **AddRef** incrementa el recuento y la **versión** disminuye el recuento. Cuando el recuento de referencias llega a cero, la función miembro **Release** puede liberar la instancia, ya que no la está usando ningún autor de llamada.

## <a name="the-clientserver-model"></a>El modelo cliente/servidor

Una clase COM implementa varias interfaces COM. La implementación de consta de archivos binarios que se ejecutan cuando un llamador interactúa con una instancia de la clase COM. COM permite el uso de una clase en aplicaciones diferentes, incluidas las aplicaciones escritas sin conocimiento de una clase determinada. En una plataforma de Windows, las clases existen en una biblioteca de vínculos dinámicos (DLL) o en otra aplicación (EXE).

En su sistema host, COM mantiene una base de datos de registro de todos los CLSID de los objetos COM instalados en el sistema. La base de datos de registro es una asignación entre cada CLSID y la ubicación del archivo DLL o EXE que hospeda la clase correspondiente. COM consulta esta base de datos cada vez que un llamador desea crear una instancia de una clase COM. El autor de la llamada solo necesita conocer el CLSID para solicitar una nueva instancia de la clase.

La interacción entre un objeto COM y sus llamadores se modela como una relación entre cliente y servidor. El cliente es el autor de la llamada que solicita un objeto COM del sistema y el servidor es el módulo que contiene objetos COM que proporciona servicios a los clientes.

Un cliente COM es cualquier llamador que pase un CLSID al sistema para solicitar una instancia de un objeto COM. La manera más sencilla de crear una instancia es llamar a la función COM, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

La función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) crea una instancia del CLSID especificado y devuelve un puntero de interfaz del tipo solicitado por el cliente. El cliente es responsable de administrar la duración de la instancia llamando a su función de [**versión**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) cuando el cliente ha terminado de usarla. Para crear varios objetos basados en un único CLSID, llame a la función [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) . Para conectarse a un objeto que ya se ha creado y se está ejecutando, llame a la función [**GetActiveObject**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-getactiveobject) .

Un servidor COM proporciona una implementación COM al sistema. Un servidor asocia un CLSID a una clase COM, hospeda la implementación de la clase, implementa un generador de clases para crear instancias de la clase y proporciona la descarga del servidor.

> [!Note]  
> Un servidor COM no es el mismo que el objeto COM que proporciona al sistema.

 

Para habilitar la creación de un objeto COM, un servidor COM debe proporcionar una implementación de la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) . Los clientes pueden llamar al método [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) para solicitar una nueva instancia de un objeto com, pero normalmente dichas solicitudes se encapsulan en la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .

Puede implementar un servidor COM como una biblioteca compartida que se carga en el proceso del cliente en tiempo de ejecución (DLL en plataformas Windows) o como un módulo ejecutable (EXE en plataformas Windows). Para obtener más información, vea [registrar aplicaciones com](registering-com-applications.md).

## <a name="service-control-manager"></a>Administrador de control de servicios

El administrador de control de servicios (SCM) controla la solicitud de cliente para una instancia de un objeto COM. En la siguiente lista se muestra la secuencia de eventos:

-   Un cliente solicita un puntero de interfaz a un objeto COM de la biblioteca COM mediante una llamada a una función como [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con el CLSID del objeto com.
-   La biblioteca COM consulta al SCM para encontrar el servidor que corresponde al CLSID solicitado.
-   El SCM localiza el servidor y solicita la creación del objeto COM del generador de clases proporcionado por el servidor.
-   Si se realiza correctamente, la biblioteca COM devuelve un puntero de interfaz al cliente.

Una vez que el sistema COM conecta un objeto de servidor a un cliente, el cliente y el objeto se comunican directamente. No se ha agregado ninguna sobrecarga por la llamada a través de un tiempo de ejecución intermediario.

Al registrar un servidor COM con el sistema host, puede especificar diferentes maneras para que se active el servidor. La lista siguiente muestra las tres formas en que el SCM puede activar un servidor COM:

-   En proceso: el SCM devuelve la ruta de acceso del archivo DLL que contiene la implementación del servidor de objetos. La biblioteca COM carga el archivo DLL y lo consulta para su puntero de interfaz de generador de clases.
-   Local: el SCM inicia el ejecutable local que registra un generador de clases en el inicio y el puntero de interfaz está disponible para el sistema y los clientes.
-   Remoto: el SCM local adquiere un puntero de interfaz de generador de clases del SCM que se ejecuta en un equipo remoto.

Cuando un cliente solicita un objeto COM, la biblioteca COM se pone en contacto con el SCM en el host local. El SCM busca el servidor COM adecuado, que puede ser local o remoto, y el servidor devuelve un puntero de interfaz al generador de clases del servidor. Cuando el generador de clases está disponible, la biblioteca COM o el cliente pueden utilizar el generador de clases para crear el objeto solicitado. Para obtener más información, vea [implementar IClassFactory](implementing-iclassfactory.md).

## <a name="reusability"></a>Reusabilidad

COM admite la *reutilización de caja negra*, lo que significa que los detalles de implementación de un componente reutilizable no se exponen a los clientes. Para lograr una reutilización de cuadro negro, COM admite dos mecanismos a través de los cuales un objeto puede volver a usar otro. Las dos formas de reutilizar se denominan *contención* y *agregación*. Por Convención, el objeto que se va a reutilizar se denomina el *objeto interno* y el objeto que hace uso del objeto interno se denomina el *objeto externo*.

En la contención, el objeto externo se comporta como un cliente del objeto interno. El objeto externo es un contenedor lógico para el objeto interno y, cuando el objeto externo utiliza los servicios del objeto interno, el objeto externo delega la implementación en las interfaces del objeto interno. Esto significa que el objeto externo se implementa en términos de los servicios del objeto interno. Es posible que el objeto externo no admita las mismas interfaces que el objeto interno y que el objeto externo pueda usar la interfaz de un objeto interno como ayuda para implementar partes de una interfaz diferente en el objeto externo.

En la agregación, el objeto externo expone interfaces del objeto interno como si se hubieran implementado en el objeto externo. Esto resulta útil cuando el objeto externo siempre delegaría cada llamada en una de sus interfaces a la misma interfaz del objeto interno. La agregación es una comodidad que permite que el objeto externo Evite la sobrecarga de implementación adicional.

Para obtener más información, vea [reutilizar objetos](reusing-objects.md).

## <a name="storage-and-stream-objects"></a>Objetos de almacenamiento y flujo

Los objetos COM guardan el estado en un archivo mediante el *almacenamiento estructurado*, que es una forma de almacenamiento persistente que permite la navegación del contenido de un archivo mediante la semántica del sistema de archivos. Tratar el contenido de un archivo de esta manera permite características como el acceso incremental, las transacciones y el uso compartido entre los procesos.

La especificación de almacenamiento persistente COM proporciona dos tipos de elementos de almacenamiento: objetos de almacenamiento y objetos de secuencia. Estos objetos se implementan mediante la biblioteca COM y las aplicaciones de usuario raramente implementan estos elementos de almacenamiento. Los objetos de almacenamiento implementan la interfaz [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) y los objetos de secuencia implementan la interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) .

Un objeto de flujo contiene datos y es conceptualmente similar a un único archivo en un sistema de archivos. Cada flujo tiene derechos de acceso y un único puntero de búsqueda. A través de la interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) , puede leer, escribir, buscar y realizar otras operaciones en los datos subyacentes de la secuencia. Un flujo se denomina mediante una cadena de texto. Puede contener cualquier estructura interna, ya que es un flujo plano de bytes. Además, las funciones de la interfaz **IStream** son similares a las funciones basadas en el identificador de archivo estándar, como las de la biblioteca en tiempo de ejecución de C de ANSI.

Un objeto de almacenamiento es conceptualmente similar a un directorio en un sistema de archivos. Cada almacenamiento puede contener cualquier número de objetos de subalmacenamiento y cualquier número de flujos. Cada almacenamiento tiene sus propios derechos de acceso. A través de la interfaz [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) , puede realizar operaciones como enumerar, mover, copiar, cambiar el nombre, crear y eliminar elementos. Un objeto de almacenamiento no almacena los datos definidos por la aplicación, pero almacena implícitamente los nombres de los elementos (almacenamientos y flujos) que contiene.

Los objetos de almacenamiento y de secuencia se pueden compartir entre los procesos cuando se implementan según la especificación COM en una plataforma de host. Esto permite que los objetos que se ejecutan en proceso o fuera de proceso tengan el mismo acceso incremental al almacenamiento de archivos. Dado que COM se carga en cada proceso por separado, utiliza mecanismos de memoria compartida admitidos por el sistema operativo para comunicar el estado de los elementos abiertos y sus modos de acceso entre los procesos.

Cada objeto de almacenamiento y de secuencia de un archivo estructurado tiene un nombre para identificarlo. El nombre es una cadena que sigue una convención determinada. Para obtener más información, vea [Storage Object naming Conventions](/windows/desktop/Stg/storage-object-naming-conventions). El nombre se pasa a las funciones [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) para especificar en qué elemento del almacenamiento se va a operar. Los nombres de los objetos de almacenamiento raíz son los mismos que los nombres de archivo del sistema de archivos subyacente, y estos nombres deben seguir las convenciones y restricciones del sistema de archivos. Cadenas que se pasan a las funciones relacionadas con el almacenamiento en las que los archivos de nombre se pasan al sistema de archivos sin interpretación o cambios.

Los nombres de los elementos incluidos en los objetos de almacenamiento se administran mediante la implementación del objeto de almacenamiento en cuestión. Todas las implementaciones de objetos de almacenamiento deben admitir nombres de elementos de 32 caracteres de longitud y algunas implementaciones pueden admitir nombres más largos. Los nombres se almacenan con el uso de mayúsculas y minúsculas, pero se comparan sin distinción de mayúsculas y minúsculas. Las aplicaciones que definen los nombres de los elementos de almacenamiento deben elegir nombres que funcionen en cualquier situación.

Puede tener acceso a todos los elementos de un archivo de almacenamiento estructurado mediante las funciones e interfaces implementadas por COM. Esto significa que otras aplicaciones pueden examinar el archivo navegando con las funciones de la interfaz [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) que proporcionan servicios similares al directorio. Además, otras aplicaciones pueden utilizar los datos del archivo, sin tener que ejecutar la aplicación que escribió el archivo. Cuando una aplicación COM tiene acceso a los archivos de almacenamiento estructurado de otra aplicación, se aplican los derechos de acceso estándar de Windows y la aplicación debe tener privilegios suficientes.

Un objeto COM puede leerse y escribirse en el almacenamiento persistente. Un cliente consulta una de las interfaces relacionadas con la persistencia en el objeto COM, según el contexto de la operación. Los objetos COM pueden implementar cualquier combinación de las siguientes interfaces:

-   [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage): el objeto com Lee y escribe su estado persistente en un objeto de almacenamiento. El cliente proporciona el objeto con un puntero [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) a través de esta interfaz. Esta es la única interfaz de persistencia que incluye semántica para el acceso incremental.
-   [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream): el objeto com Lee y escribe su estado persistente en un objeto de secuencia. El cliente proporciona el objeto con un puntero [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) a través de esta interfaz.
-   [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile): el objeto com Lee y escribe su estado persistente directamente en un archivo en el sistema subyacente. Esta interfaz no implica [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) a menos que se tenga acceso al archivo subyacente a través de estas interfaces, pero la interfaz **IPersistFile** no tiene ninguna semántica para los almacenamientos y las secuencias. El cliente proporciona el objeto con un nombre de archivo y llama a las funciones [**Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-save) o [**Load**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-load) .

## <a name="data-transfer"></a>Transferencia de datos

El almacenamiento estructurado proporciona la base para el intercambio de datos entre los objetos y procesos COM, que se denomina *transferencia de datos uniforme*. Antes de implementar COM en OLE 2, la transferencia de datos en Windows se especificaba mediante *protocolos de transferencia*, como el portapapeles y los protocolos de arrastrar y colocar. Cada protocolo de transferencia tenía su propio conjunto de funciones que enlazaron el protocolo a la consulta, y se necesitaba código específico para administrar cada protocolo y procedimiento de intercambio. La transferencia de datos uniforme representa todas las transferencias de datos mediante la interfaz [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , que separa las operaciones comunes de intercambio de datos del Protocolo de transferencia.

La interfaz [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) encapsula las operaciones estándar get y set en datos, consultas y enumeraciones, y notificaciones que detectan cuándo cambian los datos en un objeto. La transferencia de datos uniforme permite descripciones enriquecidas de formatos de datos, así como el uso de medios de almacenamiento diferentes para la transferencia de datos.

Durante la transferencia de datos uniforme, todos los protocolos intercambian un puntero a una interfaz [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) . El servidor es el origen de los datos e implementa un objeto de datos, que se puede usar en cualquier protocolo de intercambio de datos. El cliente consume los datos y solicita datos de un objeto de datos cuando recibe un puntero **IDataObject** de cualquier protocolo. Una vez que se ha producido el intercambio de puntero, ambos lados controlan el intercambio de datos de manera uniforme, a través de la interfaz **IDataObject** .

COM define dos estructuras de datos que permiten la transferencia de datos uniforme. La estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) representa un formato generalizado del portapapeles y la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) representa el medio de transferencia como un identificador de memoria.

El cliente crea una estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) para indicar el tipo de datos que solicita de un origen de datos, y lo usa el origen de datos para describir los formatos que proporciona. El cliente consulta a un origen de datos sus formatos disponibles solicitando su interfaz [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) . Para obtener más información, vea [la estructura FORMATETC](the-formatetc-structure.md).

El cliente crea una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) y la pasa al método [**GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) y el objeto de datos devuelve los datos de la estructura **STGMEDIUM** proporcionada.

La estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) permite a los clientes y a los orígenes de datos elegir el medio de intercambio más eficaz. Por ejemplo, si los datos que se van a intercambiar son muy grandes, el origen de datos puede indicar un medio basado en disco como su formato preferido, en lugar de la memoria principal. Esta flexibilidad permite intercambios de datos eficaces que pueden ser tan rápidos como pasar un puntero a un [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) o una [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Para obtener más información, vea [la estructura STGMEDIUM](the-stgmedium-structure.md).

Un cliente de un origen de datos puede requerir una notificación cuando cambian los datos. COM administra las notificaciones de cambios de datos mediante un objeto de *receptor de notificaciones* , que implementa la interfaz [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) . El objeto de receptor de notificaciones y la interfaz **IAdviseSink** se implementan mediante el cliente, que pasa un puntero **IAdviseSink** al origen de datos. Cuando el origen de datos detecta un cambio en los datos subyacentes, llama a un método **IAdviseSink** para notificar al cliente. Para obtener más información, consulte [notificación de datos](data-notification.md).

## <a name="remoting"></a>Comunicación remota

COM permite el cálculo remoto y distribuido. La *comunicación remota de interfaz* permite que una función miembro devuelva un puntero de interfaz a un objeto com que se encuentra en un proceso diferente o en un equipo host diferente. La infraestructura que realiza la interacción remota de la interfaz es transparente tanto para el cliente como para el servidor de objetos. Ni el cliente ni el servidor necesitan los detalles de implementación de otro para comunicarse a través de una interfaz remota. Un cliente llama a funciones miembro en la misma interfaz para comunicarse con un objeto COM que está en proceso, fuera de proceso en el host local o en un equipo remoto. El cliente no distingue las llamadas locales y remotas en la misma interfaz.

Para comunicarse con un objeto COM, un cliente siempre llama a una implementación en proceso. Si el objeto COM está en proceso, la llamada es directa. Si el objeto COM está fuera de proceso o remoto, COM proporciona una implementación de *proxy* que reenvía la llamada al objeto mediante el protocolo de llamada a procedimiento remoto (RPC).

Un objeto COM siempre recibe llamadas de un cliente a través de una implementación en curso. Si el autor de la llamada está en proceso, la llamada es directa. Si el llamador está fuera de proceso o remoto, COM proporciona una implementación de *código auxiliar* que recibe la llamada a procedimiento remoto del proxy en el proceso del cliente.

El *cálculo de referencias* es el procedimiento para empaquetar la pila de llamadas para su transmisión desde proxy a código auxiliar. La anulación del *cálculo de referencias* es el desempaquetado que se produce en el extremo receptor. Los valores devueltos se calculan y se deserializan del código auxiliar en el proxy. Este tipo de comunicación también se conoce como enviar una llamada *a través de la conexión*.

Cada tipo de datos distinto tiene reglas para la serialización. Los punteros de interfaz también tienen un protocolo de serialización, que se encapsula en la función [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) . En la mayoría de los casos, el cálculo de referencias de la *interfaz estándar*, proporcionado por el sistema, es suficiente, pero un objeto com puede implementar opcionalmente el cálculo de referencias de la *interfaz personalizada* para controlar la creación de proxies de objetos remotos a sí mismo. Para obtener más información, consulte [comunicación entre objetos](inter-object-communication.md).

## <a name="security"></a>Seguridad

COM proporciona dos formas de seguridad de la aplicación. Una es la *seguridad de activación*, que especifica cómo se crean los nuevos objetos, cómo se conectan los clientes a objetos nuevos y existentes, y cómo se protegen determinados servicios públicos, como la tabla de clases y la tabla de objetos en ejecución. La otra es la *seguridad de llamadas*, que especifica cómo funciona la seguridad en una conexión establecida entre un cliente y un objeto com.

El administrador de control de servicios (SCM) aplica automáticamente la seguridad de activación. Cuando el SCM recibe una solicitud para recuperar un objeto COM, comprueba la solicitud en la información de seguridad almacenada en el registro.

Las implementaciones de SCM suelen ofrecer una configuración controlada por el registro para la administración de clases implementadas y para cuentas de usuario específicas en el host. Para obtener más información, vea [seguridad de activación](activation-security.md).

La seguridad de llamada se aplica automáticamente o la aplica la aplicación. Si la aplicación proporciona información de instalación, COM realiza las comprobaciones necesarias para proteger la aplicación.

El mecanismo automático comprueba la seguridad del proceso, pero no los objetos o métodos individuales. Si una aplicación requiere una seguridad más específica, COM proporciona funciones que pueden usar las aplicaciones para realizar su propia comprobación de seguridad.

Los mecanismos automáticos y personalizados se pueden usar juntos, por lo que una aplicación puede pedir a COM que realice la comprobación de seguridad automática y, a continuación, realice sus propias tareas.

Los servicios de seguridad de llamadas COM se dividen en las siguientes categorías:

-   Funciones generales a las que llaman los clientes y los servidores, lo que permite que se inicialice el mecanismo de seguridad automático y que se registren los servicios de autenticación automática. Las API de seguridad de llamadas generales son las funciones [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) y [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) .
-   Interfaces en servidores proxy de cliente, que permiten al cliente controlar la seguridad en las llamadas a interfaces individuales. La interfaz [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) y las funciones [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket), [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)y [**CoCopyProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) proporcionan seguridad de llamada en un objeto remoto.
-   Funciones del lado servidor e interfaces de contexto de llamada, que permiten al servidor recuperar información de seguridad sobre una llamada y suplantar al llamador. La interfaz [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) y las funciones [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)y [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself) proporcionan seguridad de llamadas del lado servidor.

A menudo, el cliente consulta el objeto COM para la interfaz [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) , que se implementa localmente mediante la capa de comunicación remota. El cliente utiliza esta interfaz para controlar la seguridad de los proxies de interfaz individuales en el objeto COM antes de efectuar una llamada en una de las interfaces.

Cuando una llamada llega al servidor, el servidor puede llamar a la función [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para recuperar una interfaz [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) , lo que permite al servidor comprobar la autenticación del cliente y suplantar al cliente, si es necesario. El objeto **IServerSecurity** es válido para la duración de la llamada.

Llame a la función [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para inicializar el nivel de seguridad y establecer los valores especificados como el valor predeterminado de seguridad. Si un proceso no llama a **CoInitializeSecurity**, com lo llama automáticamente la primera vez que se calculan las referencias de una interfaz o se anula su serialización, registrando la seguridad predeterminada del sistema. La función **CoInitializeSecurity** permite al cliente establecer la seguridad de llamada predeterminada para el proceso, lo que evita el uso de [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) en servidores proxy individuales. La función **CoInitializeSecurity** permite a un servidor registrar los servicios de autenticación automática para el proceso. Para obtener más información, consulte Configuración de la [seguridad de Process-Wide con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes y servidores COM](com-clients-and-servers.md)
</dt> <dt>

[Definición de interfaces COM](defining-com-interfaces.md)
</dt> <dt>

[Registro de aplicaciones COM](registering-com-applications.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> <dt>

[Procesos, subprocesos y apartamentos](processes--threads--and-apartments.md)
</dt> </dl>

 

 
