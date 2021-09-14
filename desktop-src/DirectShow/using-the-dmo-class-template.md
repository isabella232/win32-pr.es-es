---
description: Uso de la plantilla DMO clase
ms.assetid: 5193ad08-aaee-47e3-93eb-a126a66d8f23
title: Uso de la plantilla DMO clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db80017372f11f6c928e0e6a83b591967a84ee7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891617"
---
# <a name="using-the-dmo-class-template"></a>Uso de la plantilla DMO clase

DirectShow incluye una plantilla de clase, [**IMediaObjectImpl**](imediaobjectimpl-class-template.md), para implementar DDO. La plantilla controla muchas de las tareas de "contabilidad", como validar los parámetros de entrada. Mediante el uso de la plantilla, puede centrarse en la funcionalidad específica de su DMO. Además, la plantilla ayuda a garantizar que se crea una implementación sólida. La plantilla se define en el archivo de encabezado Dmoimpl.h, ubicado en el directorio Include del SDK.

La **plantilla IMediaObjectImpl** hereda la [**interfaz IMediaObject.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) Para crear un DMO mediante la plantilla, defina una nueva clase que derive de **IMediaObjectImpl**. La plantilla implementa todos los métodos **IMediaObject.** En la mayoría de los casos, la plantilla llama a un método privado correspondiente en la clase derivada. La plantilla proporciona las siguientes características:

-   Comprobación básica de parámetros. Los métodos de plantilla comprueban que los parámetros necesarios no son **NULL,** que los índices de flujo están dentro del intervalo y que las marcas son válidas.
-   Bloqueo. Los métodos de plantilla llaman a dos métodos internos, **Lock** y **Unlock,** para serializar las operaciones en el DMO. Esta característica garantiza que el DMO es seguro para subprocesos.
-   Tipos de medios. La plantilla almacena los tipos de medios establecidos por el cliente y proporciona métodos de acceso para los tipos de medios.
-   Streaming. La plantilla evita el streaming hasta que el cliente haya establecido tipos de medios para todas las secuencias no opcionales. También garantiza que se llame al método [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) antes de comenzar el streaming, lo que garantiza que se asignen recursos.

La clase derivada debe implementar la **interfaz IUnknown;** la plantilla no proporciona esta interfaz. Puede usar el Active Template Library (ATL) para implementar **IUnknown** o puede proporcionar alguna otra implementación. La plantilla tampoco implementa el mecanismo de bloqueo. La clase derivada debe implementar los métodos **Lock** **y Unlock.** Si crea la clase mediante ATL, puede usar las implementaciones de ATL predeterminadas.

**Declarar la clase derivada**

La **plantilla de clase IMediaObjectImpl** se declara como sigue:


```C++
template <class _DERIVED_, int NUMBEROFINPUTS, int NUMBEROFOUTPUTS>
class IMediaObjectImpl : public ImediaObject
```



Los tres parámetros de plantilla \_ son \_ DERIVADO, NUMBEROFINPUTS y NUMBEROFOUTPUTS. Establezca \_ DERIVED \_ igual al nombre de la clase. Los otros dos parámetros definen el número de flujos de entrada y de salida en el DMO. Por ejemplo, para crear una clase DMO denominada CMyDmo que admita un flujo de entrada y dos flujos de salida, use la declaración siguiente:


```C++
class CMyDmo : public IMediaObjectImpl<CMyDmo, 1, 2>
```



En el resto de esta sección se describe cómo la plantilla implementa los distintos métodos **en IMediaObject**.

**Métodos para establecer tipos de medios**

Los métodos siguientes establecen o recuperan tipos de medios en el DMO:

-   **GetInputType**, **GetOutputType**. Estos métodos devuelven tipos de medios preferidos, por número de secuencia e índice de tipo. La plantilla llama **a InternalGetInputType** o **InternalGetOutputType** en la clase derivada.
-   **SetInputType**, **SetOutputType**. Estos métodos establecen el tipo de medio en una secuencia, prueban un tipo de medio o borran un tipo de medio. Para validar el tipo de medio, la plantilla llama **a InternalCheckInputType** o **InternalCheckOutputType** en la clase derivada. La clase derivada devuelve S OK para aceptar el tipo o DMO \_ \_ E \_ INVALIDTYPE para rechazar el tipo. La plantilla controla la configuración o el borrado del tipo de medio.
-   **GetInputCurrentType**, **GetOutputCurrentType**. Estos métodos devuelven el tipo de medio actual para una secuencia o DMO \_ E TYPE NOT SET si no se establece ningún \_ \_ \_ tipo. La plantilla implementa completamente estos métodos.

**Métodos informativos**

Los métodos siguientes proporcionan información sobre el DMO.

-   **GetInputMaxLatency**, **SetInputMaxLatency**. Estos métodos recuperan o establecen la latencia máxima. La plantilla llama **a InternalGetInputMaxLatency** **o InternalSetInputMaxLatency** en la clase derivada.
-   **GetInputSizeInfo**, **GetOutputSizeInfo**. Estos métodos devuelven los DMO búfer de la base de datos para una secuencia especificada. Si no se ha establecido ningún tipo de medio en esa secuencia, la plantilla devuelve DMO \_ E \_ TYPE NOT \_ \_ SET. De lo contrario, **llama a InternalGetInputSizeInfo** **o InternalGetOutputSizeInfo** en la clase derivada.
-   **GetInputStreamInfo**, **GetOutputStreamInfo**. Estos métodos devuelven varias marcas que indican cómo el cliente debe dar formato a los datos. La plantilla llama **a InternalGetInputStreamInfo** **o InternalGetOutputStreamInfo** en la clase derivada.
-   **GetStreamCount**. Este método devuelve el número de flujos de entrada y salida. La plantilla implementa este método mediante los parámetros de plantilla.

**Métodos para la asignación de recursos**

-   El **método AllocateStreamingResources** asigna los recursos que necesita DMO antes de comenzar el streaming. El **método FreeStreamingResources** libera los mismos recursos. La plantilla llama **a InternalAllocateStreamingResources** e **InternalFreeStreamingResources,** respectivamente.

No es necesario que el DMO llame a estos métodos, pero la plantilla llama automáticamente a **AllocateStreamingResources** antes de que se inicie el streaming. Por lo tanto, DMO puede suponer que los recursos se han asignado correctamente en el momento en que se llama a **ProcessInput.** El DMO debe llamar **a FreeStreamingResources** en su destructor.

Además, cuando la plantilla llama a **InternalAllocateStreamingResources**, establece una marca interna para que no vuelva a llamar a ese método hasta que llame a **InternalFreeStreamingResources**. Esto garantiza que los recursos no se vuelvan a asignar accidentalmente, lo que podría provocar pérdidas de memoria.

**Métodos de streaming**

Los métodos siguientes se usan para transmitir datos:

-   **GetInputStatus**. Este método indica si el DMO puede aceptar la entrada en este momento. La plantilla llama **a InternalAcceptingInput** en la clase derivada. Si el DMO puede aceptar la entrada, la clase derivada devuelve S OK y la plantilla establece el bit DMO INPUT STATUSF ACCEPT DATA en el \_ \_ parámetro \_ \_ \_ *dwFlags.* De lo contrario, la clase derivada devuelve S \_ FALSE y la plantilla establece *dwFlags* en cero.
-   **ProcessInput**. Este método procesa un búfer de entrada. La plantilla llama **a AllocateStreamingResources**, descrito anteriormente. A continuación, **llama a InternalAcceptingInput** en la clase derivada. Si el DMO puede aceptar una nueva entrada, la plantilla llama a **InternalProcessInput**.
-   **ProcessOutput**. Este método procesa un conjunto de búferes de salida, un búfer para cada flujo de salida. La plantilla llama **a AllocateStreamingResources** y, a **continuación, a InternalProcessOutput.**
-   **Discontinuidad.** Este método indica una discontinuidad en un flujo de entrada. La plantilla llama **a InternalAcceptingInput** en la clase derivada. Si ese método devuelve S \_ OK, la plantilla llama **a InternalDiscontinuity** en la clase derivada.
-   **Vacíe**. Este método vacía el DMO. La plantilla llama **a InternalFlush** en la clase derivada. El DMO debe descartar los búferes de entrada que aún se mantienen para procesarse.

La plantilla no proporciona ninguna compatibilidad directa con la [**interfaz IMediaObjectInPlace.**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace)

**Métodos de bloqueo**

El bloqueo se usa para proteger DMO estado de la aplicación en un entorno multiproceso. En un proyecto ATL, el [**método IMediaObject::Lock**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-lock) provoca un conflicto de nombres con **el** método Lock atl. Para resolver el conflicto, la plantilla cambia el nombre del **método IMediaObject** a **DMOLock.** Al compilar la clase derivada, defina FIX LOCK NAME antes de \_ incluir el archivo de encabezado \_ Dmo.h:


```C++
#define FIX_LOCK_NAME
#include <dmo.h>
```



Esta directiva hace que el preprocesador sustituya **DMOLock** por **Lock** en la declaración de la **interfaz IMediaObject.** Las aplicaciones todavía pueden invocar el método con el nombre **Lock**, porque el orden de vtable no cambia. El **método DMOLock** llama **a Lock** o **Unlock** en la clase derivada. Si usa ATL para implementar la clase derivada, estos métodos ya están definidos por ATL, por lo que no es necesario ningún código adicional. Si no usa ATL, debe proporcionar los métodos **Lock** y **Unlock** en la clase derivada.

La plantilla bloquea automáticamente el DMO en cada uno de los **métodos IMediaObject.** Es posible que la clase derivada tenga que bloquear el DMO dentro de otros métodos públicos que implementa (por ejemplo, si admite **IMediaObjectInPlace**). La plantilla de clase también proporciona una clase auxiliar interna, [**IMediaObjectImpl::LockIt**](imediaobjectimpl-lockit.md), que es útil para bloquear y desbloquear el DMO.

**Resumen**

Para los siguientes **métodos IMediaObject,** la plantilla llama a un método correspondiente con la misma firma en la clase derivada. La clase derivada debe implementar cada uno de los métodos que se muestran en la segunda columna.



| IMediaObject (método)            | Método de clase derivada                   |
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



 

Para los métodos **IMediaObject** restantes, no hay una correspondencia uno a uno entre los métodos de plantilla y los métodos de clase derivada. En la tabla siguiente se resumen los métodos totalmente implementados por la plantilla y qué métodos llaman a otros métodos en la clase derivada.



| IMediaObject (método)                   | Método de clase derivada                                                             |
|---------------------------------------|----------------------------------------------------------------------------------|
| **GetInputCurrentType**               | Totalmente implementado                                                                |
| **GetOutputCurrentType**              | Totalmente implementado                                                                |
| **GetStreamCount**                    | Totalmente implementado                                                                |
| **GetInputStatus**                    | [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))        |
| **Bloqueo** (implementado como **DMOLock)** | [**Bloquear,**](/previous-versions/ms809100(v=msdn.10)) [ **Desbloquear**](/previous-versions/ms809101(v=msdn.10)) |
| **SetInputType**                      | [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))        |
| **SetOutputType**                     | [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Plantilla de clase IMediaObjectImpl**](imediaobjectimpl-class-template.md)
</dt> <dt>

[Escribir un DMO](writing-a-dmo.md)
</dt> </dl>

 

 
