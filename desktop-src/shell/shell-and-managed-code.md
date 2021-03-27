---
description: Las extensiones en proceso se cargan en los procesos que las desencadenan.
title: Instrucciones para implementar extensiones de In-Process
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FE830DBF-3F18-453c-9A51-91E10559D0E8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e4dc9fd0573f3f98f0ec1110079f95f56a8c42e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003075"
---
# <a name="guidance-for-implementing-in-process-extensions"></a>Instrucciones para implementar extensiones de In-Process

Las extensiones en proceso se cargan en los procesos que las desencadenan. Por ejemplo, una extensión de espacio de nombres de Shell se puede cargar en cualquier proceso que tenga acceso al espacio de nombres del shell, ya sea directa o indirectamente. El espacio de nombres Shell se usa en muchas operaciones de Shell, como la presentación de un cuadro de diálogo de archivo común, el inicio de un documento a través de su aplicación asociada o la obtención del icono que se usa para representar un archivo. Dado que las extensiones en proceso se pueden cargar en procesos arbitrarios, se debe tener cuidado de que no afecten negativamente a la aplicación host u otras extensiones en proceso.

Un tiempo de ejecución de una nota concreta es el *Common Language Runtime (CLR)*, también conocido como *código administrado* o el *.NET Framework*. **Microsoft recomienda no escribir extensiones en proceso administradas en el explorador de Windows o en Windows Internet Explorer y no las considera un escenario admitido.**

En este tema se describen los factores que se deben tener en cuenta al determinar si un tiempo de ejecución distinto del CLR es adecuado para su uso por parte de extensiones en proceso. Algunos ejemplos de otros tiempos de ejecución son Java, Visual Basic, JavaScript/ECMAScript, Delphi y la biblioteca en tiempo de ejecución de C/C++. En este tema también se proporcionan algunos motivos por los que el código administrado no se admite en las extensiones en proceso.

## <a name="version-conflicts"></a>Conflictos de versiones

Un conflicto de versión puede producirse a través de un tiempo de ejecución que no admite la carga de varias versiones en tiempo de ejecución en un único proceso. Las versiones de CLR anteriores a la versión 4,0 se encuentran en esta categoría. Si la carga de una versión de un Runtime impide la carga de otras versiones de ese mismo tiempo de ejecución, se puede producir un conflicto si la aplicación host u otra extensión en proceso utiliza una versión en conflicto. En el caso de un conflicto de versión con otra extensión en proceso, el conflicto puede ser difícil de reproducir porque el error requiere las extensiones en conflicto correctas y el modo de error depende del orden en el que se cargan las extensiones en conflicto.

Considere la posibilidad de usar una extensión en proceso escrita con una versión de CLR anterior a la versión 4,0. Todas las aplicaciones del equipo que utilizan un cuadro de diálogo **abrir** archivo podrían tener el código administrado del cuadro de diálogo y su dependencia CLR del operador cargadas en el proceso de la aplicación. La aplicación o extensión que es la primera vez que se carga una versión anterior a 4,0 de CLR en el proceso de la aplicación restringe qué versiones de CLR se pueden usar posteriormente en ese proceso. Si una aplicación administrada con un cuadro de diálogo **abrir** se basa en una versión en conflicto de CLR, la extensión podría no ejecutarse correctamente y podría producir errores en la aplicación. Por el contrario, si la extensión es la primera que se carga en un proceso y una versión en conflicto de código administrado intenta iniciarse después de eso (quizás una aplicación administrada o una aplicación en ejecución carga el CLR a petición), se produce un error en la operación. Para el usuario, parece que algunas características de la aplicación detienen un funcionamiento aleatorio o la aplicación se bloquea.

Tenga en cuenta que las versiones de CLR iguales o posteriores a la versión 4,0 no suelen ser susceptibles del problema de control de versiones porque están diseñadas para coexistir entre sí y con la mayoría de las versiones anteriores a 4,0 de CLR (con la excepción de la versión 1,0, que no pueden coexistir con otras versiones). Sin embargo, pueden surgir problemas distintos de los conflictos de versión, como se describe en el resto de este tema.

## <a name="performance-issues"></a>Problemas de rendimiento

Pueden surgir problemas de rendimiento con los tiempos de ejecución que imponen una penalización significativa del rendimiento cuando se cargan en un proceso. La reducción del rendimiento puede ser en forma de uso de memoria, uso de CPU, tiempo transcurrido o incluso el consumo de espacio de direcciones. Se sabe que CLR, JavaScript/ECMAScript y Java son tiempos de ejecución de gran impacto. Dado que las extensiones en proceso se pueden cargar en muchos procesos y, a menudo, se realizan en momentos sensibles al rendimiento (por ejemplo, cuando se prepara un menú para mostrar el usuario), los tiempos de ejecución de gran impacto pueden afectar negativamente a la capacidad de respuesta global.

Un tiempo de ejecución de gran impacto que consume recursos significativos puede producir un error en el proceso de host o en otra extensión en proceso. Por ejemplo, un tiempo de ejecución de gran impacto que consume cientos de megabytes de espacio de direcciones para su montón puede dar lugar a que la aplicación host no pueda cargar un conjunto de resultados grande. Además, dado que las extensiones en proceso se pueden cargar en varios procesos, el consumo elevado de recursos en una única extensión puede multiplicar rápidamente a un alto consumo de recursos en todo el sistema.

Si un Runtime permanece cargado o sigue consumiendo recursos incluso cuando se ha descargado la extensión que usa ese Runtime, ese tiempo de ejecución no es apto para su uso en una extensión.

## <a name="issues-specific-to-the-net-framework"></a>Problemas específicos del .NET Framework

En las secciones siguientes se describen ejemplos de problemas encontrados con el uso de código administrado para extensiones. No se trata de una lista completa de todos los posibles problemas que pueden surgir. Los problemas descritos aquí son los motivos por los que no se admite el código administrado en las extensiones y los puntos que se deben tener en cuenta al evaluar el uso de otros runtimes.

### <a name="re-entrancy"></a>Volver a entrar

Cuando CLR bloquea un subproceso de apartamento de un solo subproceso (STA), por ejemplo, debido a un monitor. Enter, WaitHandle. WaitOne o una instrucción [**Lock**](https://msdn.microsoft.com/library/c5kehkcz(v=VS.71).aspx) , CLR, en su configuración estándar, escribe un bucle de mensajes anidado mientras espera. Muchos métodos de extensión están prohibidos para el procesamiento de mensajes, y esta reentrada imprevisible e inesperada puede dar lugar a un comportamiento anómalo que es difícil de reproducir y diagnosticar.

### <a name="the-multithreaded-apartment"></a>Apartamento multiproceso

CLR crea *contenedores RCW (Runtime Callable wrappers* ) para objetos del modelo de objetos componentes (com). Los mismos contenedores a los que se puede llamar en tiempo de ejecución se destruyen más adelante por el finalizador de CLR, que forma parte del contenedor multiproceso (MTA). Mover el proxy del STA al MTA requiere serialización, pero no se pueden calcular las referencias de todas las interfaces utilizadas por las extensiones.

### <a name="non-deterministic-object-lifetimes"></a>Duración de los objetos no deterministas

CLR tiene garantías de duración de objetos más débiles que el código nativo. Muchas extensiones tienen requisitos de recuento de referencias en objetos e interfaces, y el modelo de recolección de elementos no utilizados que emplea CLR no puede cumplir estos requisitos.

-   Si un objeto CLR obtiene una referencia a un objeto COM, la referencia de objeto COM retenida por el contenedor al que se puede llamar en tiempo de ejecución no se libera hasta que el contenedor al que se puede llamar en tiempo de ejecución se recolecta como elemento no utilizado. El comportamiento de la versión no determinista puede entrar en conflicto con algunos contratos de interfaz. Por ejemplo, el método [**IPersistPropertyBag:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768206(v=vs.85)) requiere que el objeto no retenga ninguna referencia al contenedor de propiedades cuando se devuelva el método **Load** .
-   Si se devuelve una referencia de objeto CLR a código nativo, el contenedor al que se puede llamar en tiempo de ejecución renuncia a su referencia al objeto CLR cuando se realiza la llamada final del contenedor al que se puede llamar en [**tiempo de ejecución**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) , pero el objeto CLR subyacente no se finaliza hasta que no se recolecta como elemento no utilizado. La finalización no determinista puede entrar en conflicto con algunos contratos de interfaz. Por ejemplo, se requieren controladores de miniaturas para liberar todos los recursos inmediatamente cuando su recuento de referencias desciende a cero.

## <a name="acceptable-uses-of-managed-code-and-other-runtimes"></a>Usos aceptables de código administrado y otros runtimes

Es aceptable usar código administrado y otros tiempos de ejecución para implementar extensiones fuera de proceso. Entre los ejemplos de extensiones de Shell fuera de proceso se incluyen los siguientes:

-   Controladores de vista previa
-   Acciones basadas en la línea de comandos, como las registradas en  \\  \\ subclaves de **comando** Verb del shell.
-   Objetos COM implementados en un servidor local, para los puntos de extensión de Shell que permiten la activación fuera de proceso.

Algunas extensiones se pueden implementar como extensiones en proceso o fuera de proceso. Puede implementar estas extensiones como extensiones fuera de proceso si no cumplen estos requisitos para las extensiones en proceso. La lista siguiente muestra ejemplos de extensiones que se pueden implementar como extensiones en proceso o fuera de proceso:

-   [**IExecuteCommand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexecutecommand) asociado a una entrada **DelegateExecute** registrada en una  \\  \\ subclave del **comando** Verb del shell.
-   [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) asociado al CLSID registrado en una  \\  \\ subclave **DropTarget** de verbo de Shell.
-   [**IExplorerCommandState**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) asociado a una entrada **CommandStateHandler** registrada en una  \\ subclave *Verb* del shell.

 

 
