---
description: Uso de la plantilla de clase DMO
ms.assetid: 5193ad08-aaee-47e3-93eb-a126a66d8f23
title: Uso de la plantilla de clase DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db80017372f11f6c928e0e6a83b591967a84ee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082951"
---
# <a name="using-the-dmo-class-template"></a>Uso de la plantilla de clase DMO

DirectShow incluye una plantilla de clase, [**IMediaObjectImpl**](imediaobjectimpl-class-template.md), para implementar DMOs. La plantilla controla muchas de las tareas de "contabilidad", como la validación de parámetros de entrada. Mediante el uso de la plantilla, puede centrarse en la funcionalidad específica de DMO. Además, la plantilla ayuda a asegurarse de que se crea una implementación sólida. La plantilla se define en el archivo de encabezado Dmoimpl. h, que se encuentra en el directorio de inclusión del SDK.

La plantilla **IMediaObjectImpl** hereda la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) . Para crear un DMO mediante la plantilla, defina una nueva clase que derive de **IMediaObjectImpl**. La plantilla implementa todos los métodos **IMediaObject** . En la mayoría de los casos, la plantilla llama a un método privado correspondiente en la clase derivada. La plantilla proporciona las siguientes características:

-   Comprobación básica de parámetros. Los métodos de plantilla comprueban que los parámetros necesarios no son **null**, que los índices de secuencia están dentro del intervalo y que las marcas son válidas.
-   Tienda. Los métodos de plantilla llaman a dos métodos internos, **Lock** y **Unlock**, para serializar las operaciones en DMO. Esta característica garantiza que DMO es segura para subprocesos.
-   Tipos de medios. La plantilla almacena los tipos de medios establecidos por el cliente y proporciona métodos de descriptor de acceso para los tipos de medios.
-   Difusión. La plantilla impide el streaming hasta que el cliente tenga establecidos tipos de medios para todas las secuencias no opcionales. También garantiza que se llama al método [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) antes de que se inicie el streaming, lo que garantiza que los recursos se asignan.

La clase derivada debe implementar la interfaz **IUnknown** ; la plantilla no proporciona esta interfaz. Puede usar el Active Template Library (ATL) para implementar **IUnknown** o puede proporcionar otra implementación. La plantilla tampoco implementa el mecanismo de bloqueo. La clase derivada debe implementar los métodos **Lock** y **Unlock** . Si crea la clase mediante ATL, puede usar las implementaciones predeterminadas de ATL.

**Declarar la clase derivada**

La plantilla de clase **IMediaObjectImpl** se declara de la siguiente manera:


```C++
template <class _DERIVED_, int NUMBEROFINPUTS, int NUMBEROFOUTPUTS>
class IMediaObjectImpl : public ImediaObject
```



Los tres parámetros de plantilla son \_ derived \_ , NUMBEROFINPUTS y NUMBEROFOUTPUTS. Establezca \_ derived \_ igual al nombre de la clase. Los otros dos parámetros definen el número de flujos de entrada y de salida en DMO. Por ejemplo, para crear una clase DMO denominada CMyDmo que admita un flujo de entrada y dos flujos de salida, use la siguiente declaración:


```C++
class CMyDmo : public IMediaObjectImpl<CMyDmo, 1, 2>
```



En el resto de esta sección se describe cómo la plantilla implementa los distintos métodos en **IMediaObject**.

**Métodos para establecer tipos de medios**

Los métodos siguientes establecen o recuperan los tipos de medios en DMO:

-   **GetInputType**, **GetOutputType**. Estos métodos devuelven los tipos de medios preferidos, por número de secuencia y tipo de índice. La plantilla llama a **InternalGetInputType** o **InternalGetOutputType** en la clase derivada.
-   **SetInputType**, **SetOutputType**. Estos métodos establecen el tipo de medio en una secuencia, prueban un tipo de medio o borran un tipo de medio. Para validar el tipo de medio, la plantilla llama a **InternalCheckInputType** o **InternalCheckOutputType** en la clase derivada. La clase derivada devuelve S \_ OK para aceptar el tipo o DMO \_ E \_ INVALIDTYPE para rechazar el tipo. La plantilla controla el establecimiento o la eliminación del tipo de medio.
-   **GetInputCurrentType**, **GetOutputCurrentType**. Estos métodos devuelven el tipo de archivo multimedia actual para un flujo, o el tipo de DMO \_ E \_ \_ no \_ se establece si no se establece ningún tipo. La plantilla implementa completamente estos métodos.

**Métodos informativos**

Los métodos siguientes proporcionan información acerca de DMO.

-   **GetInputMaxLatency**, **SetInputMaxLatency**. Estos métodos recuperan o establecen la latencia máxima. La plantilla llama a **InternalGetInputMaxLatency** o **InternalSetInputMaxLatency** en la clase derivada.
-   **GetInputSizeInfo**, **GetOutputSizeInfo**. Estos métodos devuelven los requisitos de búfer de DMO para una secuencia especificada. Si no se ha establecido ningún tipo de medio en la secuencia, la plantilla devuelve el tipo de DMO \_ E \_ \_ no \_ establecido. De lo contrario, llama a **InternalGetInputSizeInfo** o **InternalGetOutputSizeInfo** en la clase derivada.
-   **GetInputStreamInfo**, **GetOutputStreamInfo**. Estos métodos devuelven varias marcas que indican cómo el cliente debe dar formato a los datos. La plantilla llama a **InternalGetInputStreamInfo** o **InternalGetOutputStreamInfo** en la clase derivada.
-   **GetStreamCount**. Este método devuelve el número de flujos de entrada y salida. La plantilla implementa este método con los parámetros de la plantilla.

**Métodos para la asignación de recursos**

-   El método **AllocateStreamingResources** asigna los recursos que necesita DMO antes de que se inicie la transmisión por secuencias. El método **FreeStreamingResources** libera los mismos recursos. La plantilla llama a **InternalAllocateStreamingResources** y **InternalFreeStreamingResources**, respectivamente.

No es necesario que el cliente de DMO llame a estos métodos, pero la plantilla llama automáticamente a **AllocateStreamingResources** antes de que se inicie el streaming. Por lo tanto, DMO puede suponer que los recursos se han asignado correctamente en el momento en que se llama a **ProcessInput** . DMO debe llamar a **FreeStreamingResources** en su destructor.

Además, cuando la plantilla llama a **InternalAllocateStreamingResources**, establece una marca interna, de modo que no llama a ese método de nuevo hasta que se llama a **InternalFreeStreamingResources**. Esto garantiza que los recursos no se vuelvan a asignar accidentalmente, lo que podría provocar pérdidas de memoria.

**Métodos para el streaming**

Los métodos siguientes se utilizan para transmitir datos por secuencias:

-   **GetInputStatus**. Este método indica si DMO puede aceptar la entrada en este momento. La plantilla llama a **InternalAcceptingInput** en la clase derivada. Si DMO puede aceptar la entrada, la clase derivada devuelve S \_ correcto y la plantilla establece el \_ \_ \_ \_ bit de datos de aceptación de STATUSF de entrada de DMO en el parámetro *dwFlags* . De lo contrario, la clase derivada devuelve S \_ false y la plantilla establece *dwFlags* en cero.
-   **ProcessInput**. Este método procesa un búfer de entrada. La plantilla llama a **AllocateStreamingResources**, que se ha descrito anteriormente. A continuación, llama a **InternalAcceptingInput** en la clase derivada. Si DMO puede aceptar una entrada nueva, la plantilla llama a **InternalProcessInput**.
-   **ProcessOutput**. Este método procesa un conjunto de búferes de salida, un búfer para cada flujo de salida. La plantilla llama a **AllocateStreamingResources** y, a continuación, a **InternalProcessOutput**.
-   **Discontinuidad**. Este método señala una discontinuidad en un flujo de entrada. La plantilla llama a **InternalAcceptingInput** en la clase derivada. Si ese método devuelve S \_ correcto, la plantilla llama a **InternalDiscontinuity** en la clase derivada.
-   **Vaciar**. Este método vacía DMO. La plantilla llama a **InternalFlush** en la clase derivada. DMO debe descartar todos los búferes de entrada que todavía tenga para ser procesados.

La plantilla no proporciona ninguna compatibilidad directa para la interfaz [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) .

**Métodos para bloquear**

El bloqueo se utiliza para proteger el estado de DMO en un entorno multiproceso. En un proyecto ATL, el método [**IMediaObject:: Lock**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-lock) produce un conflicto de nombres con el método de **bloqueo** de ATL. Para resolver el conflicto, la plantilla cambia el nombre del método **IMediaObject** a **DMOLock**. Al compilar la clase derivada, defina \_ el \_ nombre del bloqueo de corrección antes de incluir el archivo de encabezado DMO. h:


```C++
#define FIX_LOCK_NAME
#include <dmo.h>
```



Esta directiva hace que el preprocesador sustituya **DMOLock** por **Lock** en la declaración de la interfaz **IMediaObject** . Las aplicaciones pueden seguir invocando el método mediante el **bloqueo** de nombre, porque el orden vtable no cambia. El método **DMOLock** llama a **Lock** o **Unlock** en la clase derivada. Si usa ATL para implementar la clase derivada, ATL ya define estos métodos, por lo que no es necesario ningún código adicional. Si no usa ATL, debe proporcionar los métodos **Lock** y **Unlock** en la clase derivada.

La plantilla bloquea automáticamente DMO en cada uno de los métodos **IMediaObject** . La clase derivada podría necesitar bloquear DMO dentro de otros métodos públicos que implementa (por ejemplo, si es compatible con **IMediaObjectInPlace**). La plantilla de clase también proporciona una clase auxiliar interna, [**IMediaObjectImpl:: LockIt**](imediaobjectimpl-lockit.md), que es útil para bloquear y desbloquear DMO.

**Resumen**

En el caso de los siguientes métodos **IMediaObject** , la plantilla llama a un método correspondiente con la misma firma en la clase derivada. La clase derivada debe implementar cada uno de los métodos que se muestran en la segunda columna.



| Método IMediaObject            | Método de clase derivada                   |
|--------------------------------|----------------------------------------|
| **AllocateStreamingResources** | **InternalAllocateStreamingResources** |
| **Discontinuidad**              | **InternalDiscontinuity**              |
| **Vaciar**                      | **InternalFlush**                      |
| **FreeStreamingResources**     | **InternalFreeStreamingResources**     |
| **GetInputMaxLatency**         | **InternalGetInputMaxLatency**         |
| **GetInputSizeInfo**           | **InternalGetInputSizeInfo**           |
| **GetInputStreamInfo**         | **InternalGetInputStreamInfo**         |
| **GetInputType**               | **InternalGetInputType**               |
| **GetOutputSizeInfo**          | **InternalGetOutputSizeInfo**          |
| **GetOutputStreamInfo**        | **InternalGetOutputStreamInfo**        |
| **GetOutputType**              | **InternalGetOutputType**              |
| **ProcessInput**               | **InternalProcessInput**               |
| **ProcessOutput**              | **InternalProcessOutput**              |
| **SetInputMaxLatency**         | **InternalSetInputMaxLatency**         |



 

En el resto de métodos **IMediaObject** , no hay una correspondencia uno a uno entre los métodos de plantilla y los métodos de clase derivada. En la tabla siguiente se resumen los métodos que se implementan por completo en la plantilla y los métodos que llaman a otros métodos en la clase derivada.



| Método IMediaObject                   | Método de clase derivada                                                             |
|---------------------------------------|----------------------------------------------------------------------------------|
| **GetInputCurrentType**               | Totalmente implementado                                                                |
| **GetOutputCurrentType**              | Totalmente implementado                                                                |
| **GetStreamCount**                    | Totalmente implementado                                                                |
| **GetInputStatus**                    | [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))        |
| **Bloqueo** (implementado como **DMOLock**) | [**Bloquear**](/previous-versions/ms809100(v=msdn.10)), [ **desbloquear**](/previous-versions/ms809101(v=msdn.10)) |
| **SetInputType**                      | [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))        |
| **SetOutputType**                     | [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Plantilla de clase IMediaObjectImpl**](imediaobjectimpl-class-template.md)
</dt> <dt>

[Escritura de DMO](writing-a-dmo.md)
</dt> </dl>

 

 
