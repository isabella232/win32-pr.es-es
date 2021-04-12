---
description: El uso del entorno de desarrollo integrado (IDE) de Microsoft Visual Basic para la depuración proporciona a los desarrolladores de Visual Basic acceso a herramientas conocidas y facilidad de uso.
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Depuración en el IDE de Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74574fdb289e1ad334337f17943c6961b95bf288
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423271"
---
# <a name="debugging-in-the-visual-basic-ide"></a>Depuración en el IDE de Visual Basic

El uso del entorno de desarrollo integrado (IDE) de Microsoft Visual Basic para la depuración proporciona a los desarrolladores de Visual Basic acceso a herramientas conocidas y facilidad de uso. Aunque es posible que sea necesario depurar muchos componentes por completo con el entorno de Microsoft Visual C++, una estrategia podría ser primero depurar tanta funcionalidad como sea posible con Visual Basic. Por ejemplo, es posible que desee usar el IDE de Visual Basic para la depuración en COM+ cuando aún no esté depurando multithreading, seguimiento de componentes, llamadas remotas o aislamiento de procesos.

En general, cuando se usa el entorno de Visual Basic para la depuración, primero se compila el proyecto y se agrega el archivo DLL a una aplicación COM+. A continuación, establezca la compatibilidad binaria para el proyecto, haciendo referencia al archivo DLL que ha creado e inicie el proyecto para comenzar la depuración.

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a>Directrices generales para la depuración en el entorno de Visual Basic

-   Durante la depuración mediante Visual Basic, COM+ trata los componentes de Visual Basic como si pertenecieran a una aplicación de biblioteca, incluso si los componentes se registran como pertenecientes a una aplicación de servidor. Dado que se ejecuta como una aplicación de biblioteca, los iconos de componente de la herramienta administrativa Servicios de componentes no giran cuando se depuran los componentes.
-   Si cambia atributos de transacción en un componente durante la depuración o realiza un cambio en el código fuente que requiere Visual Basic para generar un nuevo CLSID o ProgID, asegúrese de eliminar y volver a instalar la aplicación COM+ que contiene el componente. Si ha establecido la compatibilidad binaria para el componente, se le advertirá de que se han producido cambios.

## <a name="notes-on-debugging-within-a-com-application"></a>Notas sobre la depuración en una aplicación COM+

-   Si realiza cambios en el IDE de Visual Basic en las interfaces del componente, los nombres de clase, los nombres de proyecto, la compatibilidad transaccional u otra configuración, puede que haya discrepancias entre los datos de configuración en el explorador de servicios de componentes y la configuración real que se ejecuta en el depurador de Visual Basic.
-   No exporte una aplicación COM+ mientras depura un componente en la aplicación. COM+ tratará el entorno de desarrollo de Visual Basic como componente.
-   Si está ejecutando un componente fuera del depurador y, a continuación, decide iniciar la depuración, es posible que una instancia del componente siga ejecutándose en COM+ al iniciarlo en el depurador. COM+ detectará esta condición e intentará apagar de forma silenciosa la instancia que controla. Para evitar este problema, quite el componente de la herramienta administrativa Servicios de componentes antes de comenzar la depuración.

**Para depurar mediante el entorno de Visual Basic**

1.  Abra el proyecto de componente en Visual Basic.

2.  Compile el componente y, a continuación, establezca la compatibilidad binaria en el proyecto con el componente compilado.

3.  Establezca la propiedad MTSTransactionMode en un valor distinto de 0-NotAnMTSObject. Al iniciar el proyecto, esta configuración solicita Visual Basic para activar el componente dentro de COM+.

4.  En el menú **proyecto** , haga clic en **propiedades** y, a continuación, escriba el programa de inicio en la pestaña **depuración** . El programa de inicio es el ejecutable de cliente que llama a este componente.

    > [!Note]  
    > El programa de inicio debe ser local para el componente que está depurando.

     

5.  Presione la tecla F5 para empezar a depurar el componente.

Después de presionar F5, Visual Basic inicia la aplicación cliente y ejecuta el componente en modo de depuración. Puede colocar puntos de interrupción en el código del componente y establecer inspecciones en las variables.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con la depuración de Visual Basic COM+ en contraste con MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Depurar componentes Visual Basic compilados](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



