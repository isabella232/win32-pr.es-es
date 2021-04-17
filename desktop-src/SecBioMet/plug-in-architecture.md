---
title: Arquitectura de complementos
description: Las unidades biométricas exponen las capacidades de un dispositivo al marco a través de una interfaz estándar que se compone de adaptadores de sensor, motor y almacenamiento.
ms.assetid: d2835413-70a3-45fa-93e2-3fe78097554f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e43af9c0ea5a8db57cc0e0970b5625b1ba118f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488018"
---
# <a name="plug-in-architecture"></a>Arquitectura de complementos

Los dispositivos biométricos se fabrican en una amplia variedad de tipos y configuraciones. El Plataforma de biometría de Windows aborda esta variedad proporcionando una arquitectura extensible que permite a los desarrolladores de terceros crear componentes de complementos personalizados. El componente principal es un objeto de software denominado unidad biométrica. Las unidades biométricas exponen las capacidades de un dispositivo al marco a través de una interfaz estándar que se compone de adaptadores de sensor, motor y almacenamiento. En los temas siguientes se explican las unidades biométricas y sus componentes constituyentes.

## <a name="biometric-unit"></a>Unidad biométrica

El componente central de la arquitectura de complemento de Plataforma de biometría de Windows es la unidad biométrica, un objeto de software que expone las capacidades de un dispositivo biométrico al marco a través de una interfaz estándar.

Un solo sensor físico está asociado a cada unidad biométrica. El sensor captura los datos biométricos y puede, en función de sus capacidades de hardware, realizar otras operaciones biométricas, como la coincidencia de plantillas y el almacenamiento. Los sensores que no admiten la búsqueda de coincidencias o almacenamiento requieren módulos de software adicionales para realizar estas funciones. Para obtener más información, consulte [adaptadores](/previous-versions//dd401508(v=vs.85)).

En la ilustración siguiente se muestra cómo fluyen los datos a través de una unidad biométrica. Esencialmente, el flujo de datos forma un tipo de canalización. La entrada inicial para la canalización es un ejemplo biométrico capturado por un sensor físico. El motor intenta hacer coincidir el ejemplo con las plantillas que ya existen en el almacén de plantillas o, si no se encuentra ninguna coincidencia, crea una nueva plantilla a partir de muestras físicas repetidas y guarda la plantilla en el almacén.

![flujo de datos a través de una unidad biométrica](images/biometricunit-dataflow.png)

## <a name="biometric-unit-life-cycle"></a>Ciclo de vida de unidad biométrica

### <a name="creation"></a>Creación

Cuando se inicia el servicio biométrico de Windows o cuando recibe una notificación de hardware del administrador de Plug and Play, examina si hay hardware que admita el DEVINTERFACE biométrico de GUID de interfaz Well-Known \_ \_ \_ (E2B5183A-99EA-4cc3-AD6B-80CA8D715B80). Para cada dispositivo biométrico detectado, entonces:

-   Abre un identificador para el dispositivo.
-   Consulta las capacidades del dispositivo mediante una interfaz de control de controlador biométrico de Windows.
-   Abre la clave del registro del dispositivo e intenta buscar información sobre los complementos de adaptador asociados.
-   Abre la clave del registro del servicio biométrico de Windows y busca información sobre los complementos globales que deben invalidar los valores específicos del dispositivo que se encuentran en el paso anterior.
-   Crea una unidad biométrica para representar el dispositivo y la pasa a un proveedor de servicios biométricos.

### <a name="configuration"></a>Configuración

Después de que un proveedor de servicios biométricos (BSP) acepte una unidad biométrica, configura la unidad y la asigna a un grupo de sensores. Para obtener más información, consulte [grupos de sensores](sensor-pools.md). La unidad se configura mediante la carga de los adaptadores adecuados, la conexión a un almacén de plantillas y, posiblemente, el cambio del modo de funcionamiento. Una unidad biométrica puede configurarse para funcionar en uno de los dos modos siguientes:

-   En el modo básico, la unidad actúa como un dispositivo de captura simple. No utiliza el procesamiento incorporado ni el almacenamiento, sino que se basa completamente en los adaptadores de software para ofrecer soporte adicional. Debe ser capaz de generar ejemplos en un formato estándar. Por ejemplo, los lectores de huellas digitales deben generar ejemplos que cumplan con ANSI INCITS 381-2004. El propósito del modo básico es admitir la interoperabilidad entre los componentes de distintos proveedores.
-   En el modo avanzado, la unidad biométrica usa funciones de almacenamiento y procesamiento incorporadas. Debe exponer las interfaces estándar, pero puede generar y procesar los ejemplos en cualquier formato que desee.

Cuando una unidad biométrica se mueve de un grupo de sensores a otro, sus adaptadores se descargan y se reconfiguran para el nuevo grupo de sensores. La identidad de la unidad biométrica permanece constante. solo cambian los complementos de configuración de hardware y adaptador.

### <a name="shut-down"></a>Apagar

Cuando el servicio biométrico de Windows se cierra o cuando el administrador de Plug and Play le notifica que se ha quitado una unidad, el servicio elimina todas las unidades biométricas.

## <a name="adapters"></a>Adaptadores

Los componentes de software complementarios denominados adaptadores conectan una unidad biométrica a su hardware subyacente y proporcionan cualquier funcionalidad que pueda faltar en el hardware del sensor. Hay tres tipos de adaptadores que puede crear:

-   Un adaptador de sensor encapsula un dispositivo biométrico y proporciona una interfaz estándar para configurar el sensor, capturar ejemplos y controlar el flujo de datos biométricos al motor de procesamiento.
-   Un adaptador de motor genera plantillas biométricas a partir de ejemplos capturados, coincide con ejemplos con plantillas existentes e indexa plantillas.
-   Un adaptador de almacenamiento administra las bases de datos de plantilla.

Los adaptadores se pueden cargar y descargar en tiempo de ejecución. Esto permite al servicio biométrico de Windows volver a configurar dinámicamente una unidad biométrica conectándola a un conjunto de adaptadores diferente.

Por último, cada una de las interfaces de sensor, motor y adaptador de almacenamiento exponen dos métodos, **ControlUnit** y **ControlUnitPrivileged**, que permiten a las aplicaciones cliente obtener acceso a las capacidades del adaptador personalizado definidas por el proveedor. Esto permite al proveedor definir un conjunto casi ilimitado de operaciones de control para un dispositivo. Además, al elegir la función que se va a implementar, un proveedor puede optar por hacer que algunas operaciones de control estén disponibles para los usuarios sin privilegios y restringir otras operaciones a usuarios con privilegios.

Para obtener más información acerca de cómo crear adaptadores, vea [crear complementos de adaptador](creating-adapter-plug-ins.md).

## <a name="adapter-performance-requirements"></a>Requisitos de rendimiento del adaptador

Dado que el objetivo es la respuesta rápida en general, el rendimiento de un adaptador no se especifica en cuanto a los límites de tiempo de rutinas específicas. En su lugar, el rendimiento se especifica como un conjunto de requisitos para la experiencia global del usuario.

Existen dos requisitos:

-   Cualquier interacción entre el usuario y el sistema operativo que implique la biometría debe completarse en un plazo de dos segundos. Este intervalo mide la hora de inicio a fin que el usuario percibe desde el momento en que tocan o deslizan el sensor hasta el momento en que se produce algo visible en la pantalla del dispositivo. (Por ejemplo, durante el desbloqueo, no debe haber más de un retraso de dos segundos entre el toque del usuario o el deslizamiento del sensor de huellas digitales y la pantalla de bloqueo que confirma la identidad del usuario).
-   En el aspecto inicial de los iconos de credenciales de la pantalla de inicio de sesión o de bloqueo, se permite un poco más de tiempo (tres segundos, máximo), pero aún se prefiere en lugar de más tarde. En concreto, el icono de bio debe estar visible en la pantalla en un plazo de tres segundos a partir de la apariencia del panel de bloqueo o de inicio de sesión.

Estos números no son arbitrarios. Muchos estudios han demostrado que los seres humanos tienden a experimentar todo lo que ocurre dentro de un intervalo de dos segundos como parte del momento "ahora". Si el evento A y el evento B se producen en dos segundos entre sí, los usuarios perciben esos eventos como simultáneos. Si los eventos se separan en más de unos tres segundos, los usuarios piensan que hay un retraso, creo que algo está "tardando demasiado tiempo". Por lo tanto, se trata de un problema de psicología humano cableado.

 

 