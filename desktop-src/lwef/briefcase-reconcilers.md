---
title: Creación de reconciliadores de maletín
description: Un reconciliador de maletín da a mi maletín los medios para conciliar diferentes versiones de un documento.
ms.assetid: 86d66291-96ae-40ea-98ef-ef263f25aa82
keywords:
- reconciliadores de maletín
- conciliación
- IReconcilableObject
- IReconcileInitiator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b925e7055e15f6c7a49408aa28d147fb2eef5a7e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420557"
---
# <a name="creating-briefcase-reconcilers"></a>Creación de reconciliadores de maletín

Un reconciliador de maletín da a mi maletín los medios para conciliar diferentes versiones de un documento.

-   [Acerca de los reconciliadores de maletín](#about-briefcase-reconcilers)
    -   [Conciliación](#reconciliation)
    -   [Creación de un reconciliador de maletín](#creating-a-briefcase-reconciler)
    -   [Interacción del usuario en la conciliación](#user-interaction-in-reconciliation)
    -   [Reconciliar objetos incrustados](#reconciling-embedded-objects)
    -   [Residuos](#residues)
-   [Referencia de reconciliador de maletín](#briefcase-reconciler-reference)
    -   [Interfaces y métodos del reconciliador de maletín](#briefcase-reconciler-interfaces-and-methods)

## <a name="about-briefcase-reconcilers"></a>Acerca de los reconciliadores de maletín

Un reconciliador de maletín combina diferentes versiones de entrada de un documento para generar una única versión de salida nueva del documento. Es posible que tenga que crear un reconciliador de maletín para admitir el tipo de documento. En esta información general se describen los reconciliadores de maletín y se explica cómo crearlos.

Se tratan los temas siguientes:

-   [Conciliación](#reconciliation)
-   [Creación de un reconciliador de maletín](#creating-a-briefcase-reconciler)
-   [Interacción del usuario en la conciliación](#user-interaction-in-reconciliation)
-   [Reconciliar objetos incrustados](#reconciling-embedded-objects)
-   [Residuos](#residues)

### <a name="reconciliation"></a>Conciliación

Un documento es una colección de información que se puede copiar y cambiar. Un documento tiene versiones diferentes si el contenido de al menos dos copias del documento son diferentes. La reconciliación genera una versión única de un documento a partir de dos o más versiones iniciales. Normalmente, la versión reconciliada es una combinación de información de las versiones iniciales con la información más reciente o más útil conservada.

El maletín inicia la conciliación cuando determina que dos o más copias del mismo documento son diferentes. Maletín, que actúa como iniciador en este contexto, localiza e inicia el reconciliador del maletín asociado con el tipo de documento especificado. El reconciliador compara los documentos y determina qué partes de los documentos se deben conservar. Algunos reconciliadores pueden requerir la interacción del usuario para completar la conciliación. Otros pueden completar la reconciliación sin la interacción del usuario. El reconciliador puede estar incluido en una aplicación o ser una extensión implementada como un archivo DLL.

Algunos reconciliadores de Maletin podrían crear residuos. Un residuo es un documento, que normalmente tiene el mismo tipo de archivo que el documento inicial, que contiene información no guardada en la versión combinada. Los residuos se suelen usar para proporcionar a los autores una manera rápida de determinar qué información de su documento original no está en la última versión combinada. Si un reconciliador admite residuos, crea un residuo para cada una de las versiones originales del documento. Los residuos no se crean a menos que el iniciador los solicite.

Algunos reconciliadores de maletín funcionan con el maletín para permitir que el usuario finalice la conciliación. Se trata de una característica importante para un usuario que podría decidir que la reconciliación no debería continuar. Un reconciliador normalmente proporciona un objeto de terminación cuando la reconciliación requiere la interacción del usuario y puede ser prolongada. En algunos entornos, un reconciliador podría permitir la reconciliación parcial, lo que permite a un usuario suspender temporalmente una conciliación y reanudarla más adelante. Sin embargo, el maletín no admite actualmente la conciliación parcial.

### <a name="creating-a-briefcase-reconciler"></a>Creación de un reconciliador de maletín

Puede crear un reconciliador de maletín implementando las interfaces de conciliación. Como mínimo, un reconciliador implementa la interfaz [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) y la interfaz [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) o [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Como iniciador, el maletín determina cuándo se necesita la conciliación y llama al método [**IReconcilableObject:: Reconciliate**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) para iniciar la conciliación.

Aunque [**IReconcilableObject:: Reconciliate**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) proporciona un amplio conjunto de capacidades de conciliación, un reconciliador de maletín solo realiza una conciliación mínima en la mayoría de los casos. En concreto, el maletín no requiere que el reconciliador admita la generación de residuos o que admita el objeto de terminación. Además, el reconciliador realiza una única conciliación de arriba a abajo y no debe devolver el valor de REC \_ E \_ NOTCOMPLETE; es decir, no debe intentar la reconciliación parcial.

El maletín proporciona la interfaz [**IReconcileInitiator**](ireconcileinitiator.md) . El reconciliador del maletín puede usar el método [**IReconcileInitiator:: SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback) para establecer el objeto de finalización. El maletín no utiliza identificadores de versión y, por tanto, no puede proporcionar versiones anteriores de un documento si un reconciliador los solicita usando los métodos correspondientes en **IReconcileInitiator**.

El maletín pasa a [**IReconcilableObject:: reconciliar**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) monikers de archivo que representan las versiones del documento que se va a conciliar. El reconciliador del maletín obtiene acceso a las versiones mediante el método [IMoniker:: BindToObject](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) o [IMoniker:: BindToStorage](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) . Esta última suele ser más rápida y se recomienda. El reconciliador debe liberar cualquier objeto o almacenamiento al que se enlaza.

Cuando el reconciliador del maletín usa [IMoniker:: BindToStorage](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage), se enlaza al almacenamiento que es almacenamiento plano (un flujo) o almacenamiento estructurado definido por OLE. Si el reconciliador espera almacenamiento plano, debe usar IMoniker:: BindToStorage para solicitar la interfaz [IStream](/windows/win32/api/objidl/nn-objidl-istream) . Si el reconciliador espera almacenamiento estructurado, debe solicitar la interfaz [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) . En ambos casos, debe solicitar acceso directo de solo lectura (no transactd) al almacenamiento. es posible que el acceso de lectura y escritura no esté disponible.

Normalmente, un reconciliador de maletín mínimo busca directamente en el almacenamiento de las otras versiones y trata los objetos incrustados de una manera muy primitiva, como la combinación de dos versiones del objeto incluyendo ambas versiones en la versión de salida.

El iniciador ubica el reconciliador del maletín adecuado mediante un subconjunto de la lógica implementada por la función [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile) para determinar el tipo de un archivo determinado y, a continuación, busca en el registro la clase de reconciliador asociada al tipo de archivo especificado. El maletín, al igual que otros componentes de Shell, determina el tipo de un archivo únicamente por la extensión de nombre de archivo. La extensión de un archivo debe tener un tipo de archivo registrado para que el maletín invoque un reconciliador para el archivo. Debe establecer una entrada del registro con el siguiente formato al instalar el reconciliador.

```
CLSID
   {the file CLSID}
      Roles
         Reconciler
            (Default) = {the reconciler-classid}
```

La clase debe ser de carga rápida, debe designarse \_ como MULTIPLEUSE y, a menos que se proporcionen serializadores para la interfaz de conciliación, debe ser un servidor de tipo en curso (contenido en una DLL) en lugar de un servidor local (implementado en un archivo. exe).

### <a name="user-interaction-in-reconciliation"></a>Interacción del usuario en la conciliación

Un reconciliador de maletín debería intentar realizar la reconciliación sin la interacción del usuario. Cuanto más automatizada sea la conciliación, mejor será la percepción del proceso por el usuario.

En algunos casos, la intervención del usuario puede ser valiosa. Por ejemplo, un sistema de documentos podría requerir que un usuario Revise los cambios antes de aceptar la versión combinada de un documento o podría requerir comentarios del usuario en el que se explican los cambios realizados. En estos casos, el iniciador, no el reconciliador del maletín, es responsable de consultar al usuario y llevar a cabo las instrucciones del usuario.

En otros casos, puede ser necesaria la intervención del usuario, por ejemplo, cuando se han editado dos versiones de forma no compatible. En tales casos, el iniciador o el reconciliador del maletín deben consultar al usuario para obtener instrucciones sobre cómo resolver el conflicto. En general, ningún iniciador puede confiar en completar una conciliación sin esperar alguna interacción del usuario. Los reconciliadores, por otro lado, tienen la opción de interactuar con el usuario para resolver conflictos o requerir que el iniciador lo haga.

### <a name="reconciling-embedded-objects"></a>Reconciliar objetos incrustados

Al reconciliar un documento, el propio reconciliador del maletín puede convertirse en iniciador si detecta un objeto incrustado de un tipo que no se puede conciliar. En este caso, el reconciliador necesita reconciliar de forma recursiva cada uno de los objetos incrustados y asumir todas las responsabilidades de un iniciador.

Para llevar a cabo la recursividad, el reconciliador del maletín carga el objeto y las consultas para la interfaz adecuada. El controlador del objeto debe admitir la interfaz. Si algún método de la interfaz devuelve el \_ valor OLE E \_ NOTRUNNING, el reconciliador debe ejecutar el objeto para llevar a cabo la operación. Dado que el código para los objetos incrustados no siempre está disponible, un reconciliador debe proporcionar una solución para esta condición. Por ejemplo, el reconciliador podría incluir versiones antiguas y nuevas del objeto incrustado en la versión reconciliada. El reconciliador no debe intentar conciliar los vínculos.

El iniciador almacena las versiones del documento que se están combinando. En muchos casos, el iniciador tiene acceso al almacenamiento de cada versión y guarda el resultado de la reconciliación con almacenamiento similar. Sin embargo, a veces, el iniciador puede tener un objeto en memoria para el que no hay ninguna versión persistente disponible. Esta situación puede producirse cuando se debe conciliar un documento que contenga objetos incrustados abiertos antes de guardarlo. En tales casos, el iniciador guarda el resultado de la reconciliación en la versión encontrada en la memoria.

El iniciador utiliza la interfaz [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) para enlazar (cargar) la versión combinada. El iniciador usa el método [IPersistStorage:: Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) si ya se ha creado una versión inicial y usa el método [IPersistStorage:: InitNew](/windows/win32/api/objidl/nf-objidl-ipersiststorage-initnew) para la versión inicial. Cuando se carga la versión combinada, el iniciador usa [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para recuperar la dirección de la interfaz [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) . Esta interfaz proporciona al iniciador acceso al almacenamiento de los residuos existentes y le proporciona una manera de crear almacenamiento para los nuevos residuos. A continuación, el iniciador dirige la interfaz para llevar a cabo la conciliación. En realidad, el iniciador consulta la interfaz [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) antes de IPersistStorage. Si el reconciliador admite IPersistFile, el iniciador manipula la réplica a través de IPersistFile en lugar de los métodos de IPersistStorage. Esto permite la reconciliación de archivos que no se almacenan como documentos compuestos.

Una vez completada la conciliación, el iniciador puede guardar la versión combinada mediante la interfaz [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) o [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Durante la conciliación, el reconciliador del maletín crea los residuos según sea necesario y escribe sus bits persistentes en el almacenamiento. Si la versión combinada es una secuencia, la interfaz [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) pasada a [IPersistStorage:: Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) contiene una secuencia denominada "contents" con su estado de almacenamiento establecido en STATEBITS \_ Flat. (Puede establecer los bits de estado mediante el método [IStorage:: Stat](/windows/win32/api/objidl/nf-objidl-istorage-stat) ). Después de la combinación, el iniciador guarda la versión combinada escribiendo los datos de una manera adecuada. Debe asegurarse de que STATEBITS \_ Flat esté establecido según sea adecuado para el almacenamiento.

### <a name="residues"></a>Residuos

El iniciador indica si quiere residuos estableciendo el parámetro *pstgNewResidues* en una dirección válida al llamar al método [**IReconcilableObject:: reconciliate**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) . Si el reconciliador no admite la creación de residuos, debe devolver inmediatamente el valor de REC \_ E \_ noresiduos, a menos que el parámetro *dwFlags* especifique el valor de **\_ NORESIDUESOK de RECONCILEF** .

El reconciliador del maletín devuelve los residuos al iniciador mediante la creación de nuevos elementos de almacenamiento y su copia en la matriz a la que señala *pstgNewResidues*. En el caso de los residuos de almacenamiento estructurado, el reconciliador copia una interfaz [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) y, en el caso de los residuos de almacenamiento plano, copia una interfaz [IStream](/windows/win32/api/objidl/nn-objidl-istream) o IStorage con la \_ marca plana STATEBITS establecida. El reconciliador utiliza IStorage para crear el almacenamiento necesario, mediante [IStorage:: CreateStream (](/windows/win32/api/objidl/nf-objidl-istorage-createstream) para crear almacenamiento plano para un residuo que es una secuencia y [IStorage:: CreateStorage](/windows/win32/api/objidl/nf-objidl-istorage-createstorage) para crear almacenamiento estructurado.

El iniciador prepara *pstgNewResidues* para que no contenga ningún elemento en la parte no reservada del espacio de nombres [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) . El reconciliador del maletín coloca cada residuo en un elemento cuyo nombre corresponde al orden de su versión inicial. Por ejemplo, el primer residuo está contenido en "1", el segundo en "2", etc. Si el propio objeto reconciliado produce un residuo, se encuentra en el elemento denominado "0".

El reconciliador del maletín confirma individualmente cada uno de los elementos recién creados, asegurándose de que el iniciador tenga acceso a la información. Sin embargo, el reconciliador no confirma *pstgNewResidues* . El iniciador es responsable de confirmar esto o de eliminarlo de otro modo.

## <a name="briefcase-reconciler-reference"></a>Referencia de reconciliador de maletín

Esta sección contiene información sobre las interfaces de conciliación. Al controlar los errores, un método solo puede devolver los valores de error que se definen explícitamente como posibles valores devueltos. Además, el método debe establecer todas las variables cuyas direcciones se pasan como parámetros a **null** antes de devolver el error.

### <a name="briefcase-reconciler-interfaces-and-methods"></a>Interfaces y métodos del reconciliador de maletín

-   [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) 
    -   -   [**IReconcilableObject::GetProgressFeedbackMaxEstimate**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-getprogressfeedbackmaxestimate)
        -   [**IReconcilableObject:: reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile)

-   [**IReconcileInitiator**](ireconcileinitiator.md) 
    -   -   [**IReconcileInitiator::SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)
        -   [**IReconcileInitiator::SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback)

-   [**INotifyReplica**](/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica) 
    -   -   [**INotifyReplica::YouAreAReplica**](/windows/desktop/api/reconcil/nf-reconcil-inotifyreplica-youareareplica)

 

 