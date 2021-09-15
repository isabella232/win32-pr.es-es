---
title: Creación de conciliadores de mal estado
description: Un conciliador de mal estado proporciona a Briefcase los medios para conciliar distintas versiones de un documento.
ms.assetid: 86d66291-96ae-40ea-98ef-ef263f25aa82
keywords:
- conciliadores de mal estado
- conciliación
- IReconcilableObject
- IReconcileInitiator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b925e7055e15f6c7a49408aa28d147fb2eef5a7e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567596"
---
# <a name="creating-briefcase-reconcilers"></a>Creación de conciliadores de mal estado

Un conciliador de mal estado proporciona a Briefcase los medios para conciliar distintas versiones de un documento.

-   [Acerca de los conciliadores de minúsculas](#about-briefcase-reconcilers)
    -   [Reconciliación](#reconciliation)
    -   [Creación de un conciliador de mal estado](#creating-a-briefcase-reconciler)
    -   [Interacción del usuario en conciliación](#user-interaction-in-reconciliation)
    -   [Conciliación de objetos incrustados](#reconciling-embedded-objects)
    -   [Residuos](#residues)
-   [Referencia del conciliador de minúsculas](#briefcase-reconciler-reference)
    -   [Interfaces y métodos de conciliador de minúsculas](#briefcase-reconciler-interfaces-and-methods)

## <a name="about-briefcase-reconcilers"></a>Acerca de los conciliadores de minúsculas

Un reconciliador de mal estado combina distintas versiones de entrada de un documento para generar una única versión de salida nueva del documento. Es posible que tenga que crear un conciliador de mal estado para admitir el tipo de documento. En esta información general se describen los conciliadores de minúsculas y se explica cómo crearlos.

Se tratan los temas siguientes:

-   [Reconciliación](#reconciliation)
-   [Creación de un conciliador de mal estado](#creating-a-briefcase-reconciler)
-   [Interacción del usuario en conciliación](#user-interaction-in-reconciliation)
-   [Conciliación de objetos incrustados](#reconciling-embedded-objects)
-   [Residuos](#residues)

### <a name="reconciliation"></a>Reconciliación

Un documento es una colección de información que se puede copiar y cambiar. Un documento tiene versiones diferentes si el contenido de al menos dos copias del documento es diferente. La conciliación genera una única versión de un documento a partir de dos o más versiones iniciales. Normalmente, la versión conciliada es una combinación de información de las versiones iniciales con la información más reciente o más útil conservada.

La conciliación se inicia mediante Un mal estado cuando determina que dos o más copias del mismo documento son diferentes. El mal mal estado, que actúa como iniciador en este contexto, busca e inicia el reconciliador de mal estado asociado al tipo de documento especificado. El conciliador compara los documentos y determina qué partes de los documentos se conservarán. Algunos conciliadores pueden requerir la interacción del usuario para completar la conciliación. Otros podrían completar la conciliación sin la interacción del usuario. El conciliador puede estar contenido dentro de una aplicación o ser una extensión implementada como un archivo DLL.

Algunos conciliadores de minúsculas pueden crear insondaciones. Un objeto es un documento, que normalmente tiene el mismo tipo de archivo que el documento inicial, que contiene información no guardada en la versión combinada. Normalmente, se usan para proporcionar a los autores una manera rápida de determinar qué información de su documento original no está en la versión combinada final. Si un conciliador admite insaseciones, crea un elemento para cada una de las versiones originales del documento. No se crean residuos a menos que el iniciador los solicite.

Algunos conciliadores de mal estado funcionan con el mal estado para permitir que el usuario finalice la conciliación. Se trata de una característica importante para un usuario que podría decidir que la conciliación no debe continuar. Normalmente, un conciliador proporciona un objeto de terminación cuando la conciliación requiere la interacción del usuario y puede ser larga. En algunos entornos, un conciliador podría permitir la conciliación parcial, lo que permite a un usuario suspender temporalmente una conciliación y reanudarla más adelante. Sin embargo, el mal estado del mal estado no admite actualmente la conciliación parcial.

### <a name="creating-a-briefcase-reconciler"></a>Creación de un conciliador de mal estado

Para crear un conciliador de mal estado, implemente las interfaces de conciliación. Como mínimo, un conciliador implementa la [**interfaz IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) y la [interfaz IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) [o IPersistFile.](/windows/win32/api/objidl/nn-objidl-ipersistfile) Como iniciador, Briefcase determina cuándo se necesita la conciliación y llama al método [**IReconcilableObject::Reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) para iniciar la conciliación.

Aunque [**IReconcilableObject::Reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) proporciona un amplio conjunto de funcionalidades de conciliación, un conciliador de mal estado solo lleva a cabo una conciliación mínima en la mayoría de los casos. En concreto, el mal estado de las minúsculas no requiere que el conciliador admita la generación de residuos ni que admita el objeto de terminación. Además, el conciliador lleva a cabo una única conciliación de arriba a abajo y no debe devolver el valor REC E NOTCOMPLETE; es decir, no debe intentar la conciliación \_ \_ parcial.

Briefcase proporciona la [**interfaz IReconcileInitiator.**](ireconcileinitiator.md) El conciliador de minúsculas puede usar el método [**IReconcileInitiator::SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback) para establecer el objeto de terminación. El mal mal estado no usa identificadores de versión y, por tanto, no puede proporcionar versiones anteriores de un documento si un conciliador los solicita mediante los métodos correspondientes de **IReconcileInitiator**.

Los monikers de archivo IReconcilableObject::Reconcile que representan las versiones del documento que se deben conciliar pasan a un archivo [**IReconcilableObject::Reconcile.**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) El conciliador de mal estado obtiene acceso a las versiones mediante el método [IMoniker::BindToObject](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) o [IMoniker::BindToStorage.](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) Por lo general, este último es más rápido y se recomienda. El conciliador debe liberar los objetos o el almacenamiento al que se enlaza.

Cuando el conciliador de mal estado usa [IMoniker::BindToStorage,](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage)se enlaza al almacenamiento que es almacenamiento plano (una secuencia) o almacenamiento estructurado definido por OLE. Si el conciliador espera almacenamiento plano, debe usar IMoniker::BindToStorage para solicitar la [interfaz IStream.](/windows/win32/api/objidl/nn-objidl-istream) Si el conciliador espera almacenamiento estructurado, debe solicitar la [interfaz IStorage.](/windows/win32/api/objidl/nn-objidl-istorage) En ambos casos, debe solicitar acceso directo de solo lectura (sin transacciones) al almacenamiento; Es posible que el acceso de lectura y escritura no esté disponible.

Normalmente, un reconciliador de mal estado mínimo examina directamente el almacenamiento de las otras versiones y trata los objetos incrustados de una manera muy primitiva, como combinar dos versiones del objeto mediante la inclusión de ambas versiones en la versión de salida.

El iniciador busca el conciliador de mal estado adecuado mediante un subconjunto de la lógica implementada por la función [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile) para determinar el tipo de un archivo determinado y, a continuación, busca en el Registro la clase de conciliador asociada al tipo de archivo especificado. El mal minúscula, al igual que otros componentes de Shell, determina el tipo de un archivo únicamente mediante la extensión de nombre de archivo. La extensión de un archivo debe tener un tipo de archivo registrado para que Briefcase invoque un conciliador para el archivo. Debe establecer una entrada del Registro del formulario siguiente al instalar el conciliador.

```
CLSID
   {the file CLSID}
      Roles
         Reconciler
            (Default) = {the reconciler-classid}
```

La clase debe ser de carga rápida, debe designarse MULTIPLEUSE y, a menos que se proporcionan serializadores para la interfaz de conciliación, debe ser un servidor en proceso (contenido en un archivo DLL) en lugar de un servidor local (implementado en un \_ archivo .exe).

### <a name="user-interaction-in-reconciliation"></a>Interacción del usuario en conciliación

Un conciliador de mal estado debe intentar llevar a cabo la conciliación sin la interacción del usuario. Entre más automatizada sea la conciliación, mejor será la percepción del usuario sobre el proceso.

En algunos casos, la intervención del usuario puede ser valiosa. Por ejemplo, un sistema de documentos puede requerir que un usuario revise los cambios antes de aceptar la versión combinada de un documento o puede requerir comentarios del usuario que expliquen los cambios realizados. En estos casos, el iniciador, no el conciliador de mal estado, es responsable de consultar al usuario y llevar a cabo las instrucciones del usuario.

En otros casos, podría ser necesaria la intervención del usuario, por ejemplo, cuando dos versiones se han editado de maneras incompatibles. En tales casos, el iniciador o el conciliador de mal estado deben consultar al usuario para obtener instrucciones sobre cómo resolver el conflicto. En general, ningún iniciador puede confiar en completar una conciliación sin esperar alguna interacción del usuario. Por otro lado, los conciliadores tienen la opción de interactuar con el usuario para resolver conflictos o de requerir al iniciador que lo haga.

### <a name="reconciling-embedded-objects"></a>Conciliación de objetos incrustados

Al conciliar un documento, el propio conciliador de mal estado puede convertirse en un iniciador si detecta un objeto incrustado de un tipo que no puede conciliar. En este caso, el conciliador debe conciliar de forma recursiva cada uno de los objetos incrustados y asumir todas las responsabilidades de un iniciador.

Para llevar a cabo la recursividad, el conciliador de mal estado carga el objeto y las consultas para la interfaz adecuada. El controlador del objeto debe admitir la interfaz . Si algún método de la interfaz devuelve el valor DE OLE \_ E NOTRUNNING, el conciliador debe ejecutar el objeto para llevar a cabo \_ la operación. Dado que el código de los objetos incrustados no siempre está disponible, un conciliador debe proporcionar una solución para esta condición. Por ejemplo, el conciliador podría incluir versiones antiguas y nuevas del objeto incrustado en la versión conciliada. El conciliador no debe intentar conciliar entre vínculos.

El iniciador almacena las versiones del documento que se combinan. En muchos casos, el iniciador tiene acceso al almacenamiento de cada versión y guarda el resultado de la conciliación mediante un almacenamiento similar. Sin embargo, a veces, el iniciador podría tener un objeto en memoria para el que no hay disponible ninguna versión persistente. Esta situación puede producirse cuando se debe conciliar un documento que contiene objetos incrustados abiertos antes de guardarse. En tales casos, el iniciador guarda el resultado de la conciliación en la versión encontrada en la memoria.

El iniciador usa la [interfaz IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) para enlazar (cargar) la versión combinada. El iniciador usa el método [IPersistStorage::Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) si ya se ha creado una versión inicial y usa el método [IPersistStorage::InitNew](/windows/win32/api/objidl/nf-objidl-ipersiststorage-initnew) para la versión inicial. Cuando se carga la versión combinada, el iniciador usa [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para recuperar la dirección de la [**interfaz IReconcilableObject.**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) Esta interfaz proporciona al iniciador acceso al almacenamiento de los residuos existentes y le proporciona una manera de crear almacenamiento para los nuevos resaltes. A continuación, el iniciador dirige la interfaz para llevar a cabo la conciliación. El iniciador consulta realmente la interfaz [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) antes de IPersistStorage. Si el conciliador admite IPersistFile, el iniciador manipula la réplica a través de IPersistFile en lugar de los métodos IPersistStorage. Esto permite la conciliación de archivos que no se almacenan como documentos compuestos.

Una vez completada la conciliación, el iniciador puede guardar la versión combinada mediante la [interfaz IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) [o IPersistFile.](/windows/win32/api/objidl/nn-objidl-ipersistfile) Durante la conciliación, el conciliador de mal estado crea los restos según sea necesario y escribe sus bits persistentes en el almacenamiento. Si la versión combinada es una secuencia, la interfaz [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) pasada a [IPersistStorage::Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) contiene una secuencia denominada "Contents" con su estado de almacenamiento establecido en STATEBITS \_ FLAT. (Puede establecer los bits de estado mediante el [método IStorage::Stat).](/windows/win32/api/objidl/nf-objidl-istorage-stat) Después de la combinación, el iniciador guarda la versión combinada escribiendo los datos de la manera adecuada. Debe asegurarse de que STATEBITS \_ FLAT está establecido según corresponda para el almacenamiento.

### <a name="residues"></a>Residuos

El iniciador indica si desea que se desconvoque estableciendo el parámetro *pstgNewResidues* en una dirección válida al llamar al método [**IReconcilableObject::Reconcile.**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) Si el conciliador no admite la creación de residuos, debe devolver inmediatamente el valor REC E NORESIDUES, a menos que el parámetro dwFlags especifique el valor \_ \_ **RECONCILEF \_ NORESIDUESOK.** 

El conciliador de minúsculas devuelve los restos al iniciador mediante la creación de nuevos elementos de almacenamiento y su copia en la matriz a la que *apunta pstgNewResidues*. En el caso de los depósitos de almacenamiento estructurado, el conciliador copia una interfaz [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) y, en el caso de los residuos de almacenamiento plano, copia una [interfaz IStream](/windows/win32/api/objidl/nn-objidl-istream) o IStorage con la marca FLAT de STATEBITS \_ establecida. El conciliador usa IStorage para crear el almacenamiento necesario, mediante [IStorage::CreateStream](/windows/win32/api/objidl/nf-objidl-istorage-createstream) para crear almacenamiento plano para un residuo que es una secuencia e [IStorage::CreateStorage](/windows/win32/api/objidl/nf-objidl-istorage-createstorage) para crear almacenamiento estructurado.

El iniciador prepara *pstgNewResidues para* que no contenga elementos en la parte no conservada del espacio [de nombres IStorage.](/windows/win32/api/objidl/nn-objidl-istorage) El conciliador de minúsculas coloca cada residuo en un elemento cuyo nombre corresponde al orden de su versión inicial. Por ejemplo, el primer residuo se encuentra en "1", el segundo en "2", y así sucesivamente. Si el propio objeto conciliado genera un residuo, se encuentra en el elemento denominado "0".

El conciliador de mal estado confirma individualmente cada uno de los elementos recién creados, lo que garantiza que el iniciador tenga acceso a la información. Sin embargo, el conciliador no confirma *pstgNewResidues.* El iniciador es responsable de confirmarlo o de desecharlo de otro modo.

## <a name="briefcase-reconciler-reference"></a>Referencia del conciliador de minúsculas

Esta sección contiene información sobre las interfaces de conciliación. Al controlar errores, un método solo puede devolver los valores de error que se definen explícitamente como valores devueltos posibles. Además, el método debe establecer todas las variables cuyas direcciones se pasan como parámetros en **NULL** antes de volver del error.

### <a name="briefcase-reconciler-interfaces-and-methods"></a>Interfaces y métodos de conciliador de minúsculas

-   [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) 
    -   -   [**IReconcilableObject::GetProgressFeedbackMaxEstimate**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-getprogressfeedbackmaxestimate)
        -   [**IReconcilableObject::Reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile)

-   [**IReconcileInitiator**](ireconcileinitiator.md) 
    -   -   [**IReconcileInitiator::SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)
        -   [**IReconcileInitiator::SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback)

-   [**INotifyReplica**](/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica) 
    -   -   [**INotifyReplica::YouAreAReplica**](/windows/desktop/api/reconcil/nf-reconcil-inotifyreplica-youareareplica)

 

 