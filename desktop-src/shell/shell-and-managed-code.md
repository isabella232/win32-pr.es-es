---
description: Las extensiones en proceso se cargan en cualquier proceso que las desencadene.
title: Instrucciones para implementar In-Process de archivos
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FE830DBF-3F18-453c-9A51-91E10559D0E8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 15ccbee300cbfe1b08bc0509472ac3afcaa9ea3db54f6f1e38131cc08d2e8381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858180"
---
# <a name="guidance-for-implementing-in-process-extensions"></a>Instrucciones para implementar In-Process de archivos

Las extensiones en proceso se cargan en cualquier proceso que las desencadene. Por ejemplo, una extensión de espacio de nombres de Shell se puede cargar en cualquier proceso que tenga acceso al espacio de nombres de Shell directa o indirectamente. Muchas operaciones de Shell usan el espacio de nombres de Shell, como la presentación de un cuadro de diálogo de archivo común, el inicio de un documento a través de su aplicación asociada o la obtención del icono utilizado para representar un archivo. Dado que las extensiones en proceso se pueden cargar en procesos arbitrarios, se debe tener cuidado de que no afectan negativamente a la aplicación host ni a otras extensiones en proceso.

Un tiempo de ejecución de una nota determinada es *Common Language Runtime (CLR),* también conocido como *código administrado* o .NET Framework *.* **Microsoft recomienda no escribir extensiones administradas en proceso en Windows Explorer o Windows Internet Explorer y no las considera un escenario compatible.**

En este tema se de abordan los factores que se deben tener en cuenta al determinar si algún tiempo de ejecución distinto de CLR es adecuado para su uso por parte de las extensiones en proceso. Algunos ejemplos de otros entornos de ejecución son Java, Visual Basic, JavaScript/ECMAScript, Del javascript y la biblioteca en tiempo de ejecución de C/C++. En este tema también se proporcionan algunas razones por las que el código administrado no se admite en las extensiones en proceso.

## <a name="version-conflicts"></a>Conflictos de versión

Un conflicto de versión puede surgir a través de un tiempo de ejecución que no admite la carga de varias versiones en tiempo de ejecución dentro de un único proceso. Las versiones de CLR anteriores a la versión 4.0 entran en esta categoría. Si la carga de una versión de un runtime impide la carga de otras versiones de ese mismo runtime, esto puede crear un conflicto si la aplicación host u otra extensión en proceso usa una versión en conflicto. En el caso de un conflicto de versión con otra extensión en proceso, el conflicto puede ser difícil de reproducir porque el error requiere las extensiones en conflicto correctas y el modo de error depende del orden en el que se cargan las extensiones en conflicto.

Considere una extensión en proceso escrita con una versión de CLR anterior a la versión 4.0. Todas las aplicaciones del equipo  que usan un cuadro de diálogo Abrir archivo podrían tener el código administrado del cuadro de diálogo y su dependencia CLR correspondiente cargada en el proceso de la aplicación. La aplicación o extensión que se va a cargar primero una versión anterior a la 4.0 de CLR en el proceso de la aplicación restringe las versiones de CLR que ese proceso puede usar posteriormente. Si una aplicación  administrada con un cuadro de diálogo Abrir se basa en una versión en conflicto de CLR, la extensión podría no ejecutarse correctamente y podría provocar errores en la aplicación. Por el contrario, si la extensión es la primera en cargarse en un proceso y una versión en conflicto del código administrado intenta iniciarse después de eso (quizás una aplicación administrada o una aplicación en ejecución carga CLR a petición), se produce un error en la operación. Para el usuario, parece que algunas características de la aplicación dejan de funcionar aleatoriamente o que la aplicación se bloquea de forma insotente.

Tenga en cuenta que las versiones de CLR iguales o posteriores a la versión 4.0 no suelen ser susceptibles al problema de control de versiones porque están diseñadas para coexistir entre sí y con la mayoría de las versiones anteriores a la 4.0 de CLR (a excepción de la versión 1.0, que no pueden coexistir con otras versiones). Sin embargo, pueden surgir problemas distintos de los conflictos de versión, como se describe en el resto de este tema.

## <a name="performance-issues"></a>Problemas de rendimiento

Pueden surgir problemas de rendimiento con los tiempos de ejecución que imponen una reducción significativa del rendimiento cuando se cargan en un proceso. La penalización del rendimiento puede ser en forma de uso de memoria, uso de CPU, tiempo transcurrido o incluso consumo de espacio de direcciones. Se sabe que CLR, JavaScript/ECMAScript y Java son entornos de ejecución de alto impacto. Dado que las extensiones en proceso se pueden cargar en muchos procesos y a menudo se realizan en momentos sensibles al rendimiento (por ejemplo, al preparar un menú para que se muestre el usuario), los tiempos de ejecución de alto impacto pueden afectar negativamente a la capacidad de respuesta general.

Un entorno de ejecución de alto impacto que consume recursos significativos puede provocar un error en el proceso de host u otra extensión en proceso. Por ejemplo, un entorno de ejecución de alto impacto que consume cientos de megabytes de espacio de direcciones para su montón puede dar lugar a que la aplicación host no pueda cargar un conjunto de datos grande. Además, dado que las extensiones en proceso se pueden cargar en varios procesos, el consumo elevado de recursos en una sola extensión puede multiplicarse rápidamente en un consumo elevado de recursos en todo el sistema.

Si un tiempo de ejecución permanece cargado o sigue consumiendo recursos incluso cuando se ha descargado la extensión que usa ese tiempo de ejecución, ese tiempo de ejecución no es adecuado para su uso en una extensión.

## <a name="issues-specific-to-the-net-framework"></a>Problemas específicos de la .NET Framework

En las secciones siguientes se de abordan ejemplos de problemas encontrados con el uso de código administrado para extensiones. No son una lista completa de todos los posibles problemas que pueda encontrar. Los problemas que se deban a continuación son los motivos por los que el código administrado no se admite en las extensiones y los puntos que se deben tener en cuenta al evaluar el uso de otros entornos de ejecución.

### <a name="re-entrancy"></a>Volver a participar

Cuando CLR bloquea un subproceso de apartamento de un solo subproceso (STA), por ejemplo, debido a [](https://msdn.microsoft.com/library/c5kehkcz(v=VS.71).aspx) una instrucción Monitor.Enter, WaitHandle.WaitOne o un bloqueo controlado, CLR, en su configuración estándar, entra en un bucle de mensajes anidado mientras espera. Se prohíbe que muchos métodos de extensión procesen mensajes, y esta reenencia imprevisible e inesperada puede dar lugar a un comportamiento anómalo que es difícil de reproducir y diagnosticar.

### <a name="the-multithreaded-apartment"></a>El apartamento multiproceso

CLR crea contenedores *que se pueden llamar en tiempo de ejecución* para objetos del Modelo de objetos componentes (COM). Estos mismos contenedores que se pueden llamar en tiempo de ejecución se destruyen más adelante por el finalizador de CLR, que forma parte del contenedor multiproceso (MTA). Mover el proxy del STA al MTA requiere serialización, pero no todas las interfaces usadas por las extensiones se pueden serializar.

### <a name="non-deterministic-object-lifetimes"></a>Duraciones de objetos no deterministas

CLR tiene garantías de duración de objetos más débiles que el código nativo. Muchas extensiones tienen requisitos de recuento de referencias en objetos e interfaces, y el modelo de recolección de elementos no utilizados empleado por CLR no puede cumplir estos requisitos.

-   Si un objeto CLR obtiene una referencia a un objeto COM, la referencia de objeto COM que mantiene el contenedor al que se puede llamar en tiempo de ejecución no se libera hasta que el contenedor al que se puede llamar en tiempo de ejecución se recopila como elementos no utilizados. El comportamiento de la versión no determinista puede estar en conflicto con algunos contratos de interfaz. Por ejemplo, el método [**IPersistPropertyBag::Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768206(v=vs.85)) requiere que el objeto no conserve ninguna referencia al bolsa de propiedades cuando el **método Load** vuelva.
-   Si se devuelve una referencia de objeto CLR al código nativo, el contenedor al que se puede llamar en tiempo de ejecución vuelve a hacer referencia al objeto CLR cuando se realiza la llamada final del contenedor al que se puede llamar en tiempo de ejecución a [**Release,**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pero el objeto CLR subyacente no se finalizará hasta que se recolecte como elemento no utilizados. La finalización no determinista puede estar en conflicto con algunos contratos de interfaz. Por ejemplo, los controladores de miniaturas deben liberar todos los recursos inmediatamente cuando su recuento de referencias cae a cero.

## <a name="acceptable-uses-of-managed-code-and-other-runtimes"></a>Usos aceptables de código administrado y otros entornos de ejecución

Es aceptable usar código administrado y otros tiempos de ejecución para implementar extensiones fuera de proceso. Entre los ejemplos de extensiones de Shell fuera de proceso se incluyen los siguientes:

-   Controladores de vista previa
-   Acciones basadas en la línea de comandos, como las registradas en **subclaves de** \\ *comandos* del verbo \\  de shell.
-   Objetos COM implementados en un servidor local, para puntos de extensión de Shell que permiten la activación fuera de proceso.

Algunas extensiones se pueden implementar como extensiones en proceso o fuera de proceso. Puede implementar estas extensiones como extensiones fuera de proceso si no cumplen estos requisitos para las extensiones en proceso. En la lista siguiente se muestran ejemplos de extensiones que se pueden implementar como extensiones en proceso o fuera de proceso:

-   [**IExecuteCommand asociado**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexecutecommand) a una **entrada DelegateExecute** registrada en una **subclave de** comando de \\ *verbo* \\ **de** shell.
-   [**IDropTarget asociado**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) al CLSID registrado en una **subclave** \\  \\ **DropTarget** del verbo de shell.
-   [**IExplorerCommandState asociado**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) a una **entrada CommandStateHandler** registrada en una **subclave** \\ *de verbo* de shell.

 

 
