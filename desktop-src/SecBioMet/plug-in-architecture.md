---
title: Arquitectura de complementos
description: Las unidades biométricas exponen las funciones de un dispositivo al marco de trabajo a través de una interfaz estándar que consta de adaptadores de sensor, motor y almacenamiento.
ms.assetid: d2835413-70a3-45fa-93e2-3fe78097554f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33a82f85387698f7fb80c65525004ac541a1108635ca3d929adda7b0cbb932cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119411074"
---
# <a name="plug-in-architecture"></a>Arquitectura de complementos

Los dispositivos biométricos se fabrica en una amplia variedad de tipos y configuraciones. El Windows Biometric Framework aborda esta variedad proporcionando una arquitectura extensible que permite a los desarrolladores de terceros crear componentes de complemento personalizados. El componente principal es un objeto de software denominado unidad biométrica. Las unidades biométricas exponen las funciones de un dispositivo al marco de trabajo a través de una interfaz estándar que consta de adaptadores de sensor, motor y almacenamiento. Las unidades biométricas y sus componentes constituyentes se tratan en los temas siguientes.

## <a name="biometric-unit"></a>Unidad biométrica

El componente central de la arquitectura del complemento Windows Biometric Framework es la unidad biométrica, un objeto de software que expone las funciones de un dispositivo biométrico al marco a través de una interfaz estándar.

Un único sensor físico está asociado a cada unidad biométrica. El sensor captura datos biométricos y también puede, según sus funcionalidades de hardware, realizar otras operaciones biométricas, como la coincidencia de plantillas y el almacenamiento. Los sensores que no admiten la incorporación de coincidencias o almacenamiento requieren módulos de software adicionales para realizar estas funciones. Para obtener más información, vea [Adaptadores](/previous-versions//dd401508(v=vs.85)).

En la ilustración siguiente se muestra cómo fluyen los datos a través de una unidad biométrica. Básicamente, el flujo de datos forma un tipo de canalización. La entrada inicial a la canalización es una muestra biométrica capturada por un sensor físico. El motor intenta hacer coincidir el ejemplo con las plantillas que ya existen en el almacén de plantillas o, si no se encuentra ninguna coincidencia, compila una nueva plantilla a partir de ejemplos físicos repetidos y guarda la plantilla en el almacén.

![datos que fluyen a través de una unidad biométrica](images/biometricunit-dataflow.png)

## <a name="biometric-unit-life-cycle"></a>Ciclo de vida de la unidad biométrica

### <a name="creation"></a>Creación

Cuando se inicia Windows Biometric Service o cuando recibe una notificación de hardware del administrador de Plug and Play, busca cualquier hardware que admita la interfaz conocida GUID \_ DEVINTERFACE \_ BIOMETRIC \_ READER (E2B5183A-99EA-4cc3-AD6B-80CA8D715B80). Para cada dispositivo biométrico, lo ha detectado:

-   Abre un identificador para el dispositivo.
-   Consulta las funcionalidades del dispositivo mediante una Windows de control del controlador biométrico.
-   Abre la clave del Registro del dispositivo e intenta buscar información sobre los complementos de adaptador asociados.
-   Abre la Windows registro de Biometric Service y busca información sobre los complementos globales que deben invalidar los valores específicos del dispositivo encontrados en el paso anterior.
-   Crea una unidad biométrica para representar el dispositivo y pasa la unidad a un proveedor de servicios biométricos.

### <a name="configuration"></a>Configuración

Después de que un proveedor de servicios biométricos (BSP) acepte una unidad biométrica, la configura y la asigna a un grupo de sensores. Para más información, consulte [Grupos de sensores.](sensor-pools.md) La unidad se configura cargando los adaptadores adecuados, conectándose a un almacén de plantillas y cambiando posiblemente el modo de funcionamiento. Una unidad biométrica se puede configurar para funcionar en uno de estos dos modos:

-   En el modo básico, la unidad actúa como un dispositivo de captura simple. No usa el procesamiento ni el almacenamiento incorporados, sino que se basa completamente en adaptadores de software para obtener compatibilidad adicional. Debe poder generar ejemplos en un formato estándar. Por ejemplo, los lectores de huellas digitales deben generar muestras que cumplan con ANSI INCITS 381-2004. El propósito del modo básico es admitir la interoperabilidad entre componentes de distintos proveedores.
-   En el modo avanzado, la unidad biométrica usa funciones de procesamiento y almacenamiento incorporadas. Debe exponer las interfaces estándar, pero puede generar y procesar ejemplos en cualquier formato deseado.

Cuando una unidad biométrica se mueve de un grupo de sensores a otro, sus adaptadores se descargan y se reconfiguran para el nuevo grupo de sensores. La identidad de la unidad biométrica sigue siendo constante; solo cambian la configuración de hardware y los complementos del adaptador.

### <a name="shut-down"></a>Apagar

Cuando el Windows biométrico se cierra o cuando el administrador de Plug and Play le notifica que se ha quitado una unidad, el servicio elimina todas las unidades biométricas.

## <a name="adapters"></a>Adaptadores

Los componentes de software de complemento denominados adaptadores conectan una unidad biométrica a su hardware subyacente y suministran cualquier funcionalidad que pueda faltar en el hardware del sensor. Hay tres tipos de adaptadores que puede crear:

-   Un adaptador de sensor encapsula un dispositivo biométrico y proporciona una interfaz estándar para configurar el sensor, capturar muestras y controlar el flujo de datos biométricos al motor de procesamiento.
-   Un adaptador de motor genera plantillas biométricas a partir de ejemplos capturados, coincide con las plantillas existentes e indexa plantillas.
-   Un adaptador de almacenamiento administra las bases de datos de plantilla.

Los adaptadores se pueden cargar y descargar en tiempo de ejecución. Esto permite que Windows Biometric Service vuelva a configurar dinámicamente una unidad biométrica conectándolo a un conjunto diferente de adaptadores.

Por último, cada una de las interfaces del sensor, motor y adaptador de almacenamiento expone dos métodos, **ControlUnit** y **ControlUnitPrivileged,** que permiten a las aplicaciones cliente acceder a las funcionalidades de adaptador personalizadas definidas por el proveedor. Esto permite al proveedor definir un conjunto casi ilimitado de operaciones de control para un dispositivo. Además, al elegir qué función implementar, un proveedor puede optar por hacer que algunas operaciones de control estén disponibles para los usuarios sin privilegios y, al mismo tiempo, restringir otras operaciones a usuarios con privilegios.

Para obtener más información sobre cómo crear adaptadores, vea Crear complementos [de adaptador.](creating-adapter-plug-ins.md)

## <a name="adapter-performance-requirements"></a>Requisitos de rendimiento del adaptador

Dado que el objetivo es una respuesta rápida en general, el rendimiento de un adaptador no se especifica en términos de límites de tiempo en rutinas específicas. En su lugar, el rendimiento se especifica como un conjunto de requisitos para la experiencia general del usuario.

Hay dos requisitos:

-   Cualquier interacción entre el usuario y el sistema operativo que implique biometría debe completarse en un plazo de dos segundos. Ese intervalo mide la hora de inicio a fin que el usuario percibe desde el momento en que se tocan o deslizan el dedo del sensor hasta el momento en que ocurre algo visible en la pantalla del dispositivo. (Por ejemplo, durante el desbloqueo, no debe haber más de un retraso de dos segundos entre que el usuario toque o desvía el sensor de huella digital y la pantalla de bloqueo que confirma la identidad del usuario).
-   Para la apariencia inicial de los iconos de credenciales en la pantalla de inicio de sesión o bloqueo, se permite un poco más de tiempo (tres segundos, máximo), pero se prefiere más pronto que tarde. En concreto, el icono bio debe estar visible en pantalla en los tres segundos siguientes a la apariencia del panel de bloqueo o inicio de sesión.

Estos números no son arbitrarios. Numerosos estudios han demostrado que los seres humanos tienden a experimentar todo lo que sucede en un intervalo de dos segundos como parte del momento "ahora". Si el evento A y el evento B se suceden en dos segundos entre sí, los usuarios perciben que esos eventos son simultáneos. Si los eventos se separan por más de tres segundos, los usuarios creen que hay un retraso: creen que algo "está tardando demasiado". Por lo tanto, se trata de un problema de humedad humana con cable duro.

 

 