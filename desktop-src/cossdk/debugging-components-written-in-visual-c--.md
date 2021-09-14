---
description: Cuando esté listo para depurar la funcionalidad com+ en los componentes de Microsoft Visual C++ Visual C++, puede configurar un proyecto o la herramienta administrativa Servicios de componentes para iniciar el depurador.
ms.assetid: 206467ac-108a-49de-a884-66959dc77650
title: Depuración de componentes escritos en Visual C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e4b6324cc69531f09612c2af37fa03a036fd4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360864"
---
# <a name="debugging-components-written-in-visual-c"></a>Depuración de componentes escritos en Visual C++

Cuando esté listo para depurar la funcionalidad com+ en los componentes de Microsoft Visual C++ Visual C++, puede configurar un proyecto o la herramienta administrativa Servicios de componentes para iniciar el depurador. Si usa Visual C++, puede depurar con un cliente remoto mediante OLE RPC y depuración Just-In-Time (JIT). Si no puede ejecutar el cliente en el depurador o si el cliente se está ejecutando en otro equipo, puede usar la configuración **Iniciar** en el depurador de COM+. Lo encontrará en la herramienta administrativa Servicios de componentes como una casilla de la **pestaña** Avanzadas del cuadro de diálogo Propiedades de **la aplicación** COM+.

Cuando haya terminado de depurar, debe apagar las aplicaciones COM+ que está depurando. Si un proceso de servidor se deja en ejecución, es posible que reciba un mensaje de error la próxima vez que intente compilar un archivo DLL cuando el archivo DLL existente todavía se cargue en memoria. Para apagar una aplicación COM+, haga clic con el botón derecho en la aplicación en el árbol de consola y, a continuación, haga clic **en Apagar.**

> [!Note]  
> Si usa transacciones, es posible que también desee aumentar el tiempo de espera de la transacción, cuyo valor predeterminado es 60 segundos. También puede especificar un valor de 0, especificando de forma eficaz un período de tiempo de espera de transacción infinito. Con la herramienta administrativa Servicios de componentes, cambie  la configuración de tiempo de espera de la transacción en la pestaña Opciones de **la Mi PC propiedades.**

 

## <a name="debugging-server-application-components-with-visual-c"></a>Depuración de componentes de aplicación de servidor con Visual C++

Al depurar aplicaciones de servidor COM+, puede que desee depurar llamadas remotas cargando el cliente y la aplicación de servidor en el depurador. Con Visual C++, puede depurar llamadas remotas a los componentes a través de la configuración Just-In-Time (JIT) y OLE RPC. La configuración JIT hace que el componente compilado inicie el depurador Visual C++ cuando se produce un error; La configuración de OLE RPC permite al depurador pasar del cliente al componente a medida que se pasa por el código.

Cuando estas características están habilitadas, puede iniciar el cliente en el depurador. Cuando el cliente realiza una llamada al componente, el depurador se depura paso a paso por instrucciones en el código del componente en el proceso de servidor, incluso si el servidor está en un equipo diferente en la red. Si es necesario, se inicia automáticamente una sesión de depuración en el equipo servidor. De forma similar, una sola ejecución paso a paso más allá de la instrucción return en el código del componente devolverá la depuración a la siguiente instrucción en el código del cliente.

> [!Note]  
> Es posible que pueda guardar algunos pasos mediante la opción Iniciar en el **depurador** de COM+. Esto le permite especificar el depurador Visual C++ (u otro) sin tener que realizar una configuración de depuración especial en el Visual C++ de depuración. Lo encontrará en la herramienta administrativa Servicios de componentes como una casilla de la **pestaña** Avanzadas del cuadro de diálogo Propiedades de **la aplicación** COM+. Para obtener más información, vea "Depuración sin Visual C++" en este tema.

 

Cuando la aplicación COM+ que contiene el componente es una aplicación de servidor, debe empezar por apagar la aplicación mediante la herramienta administrativa Servicios de componentes. Para ello, haga clic con el botón derecho en la aplicación COM+ en el árbol de consola y, a continuación, haga clic **en Apagar**.

**Para habilitar la depuración RPC en Visual C++**

1.  En Visual C++, en el **menú Herramientas,** haga clic en **Opciones.**

2.  En el **cuadro de** diálogo Opciones, en la **pestaña** Depurar , active las casillas **Depuración DE OLE RPC** y Depuración **Just-In-Time.**

3.  Haga clic en **OK**.

Para comenzar la depuración, inicie el proyecto de cliente en el depurador.

También puede depurar el componente sin iniciar el cliente en el depurador. En este caso, el componente debe iniciar el depurador por sí mismo. Para ello, el proyecto de componente debe especificar un archivo ejecutable para la sesión de depuración, junto con el identificador de aplicación COM+.

**Para habilitar un componente de aplicación de servidor para iniciar el depurador Visual C++ servidor**

1.  En el menú **Project,** haga clic **en Configuración**.

2.  En el **Project Configuración** de diálogo, en el **Configuración cuadro** For (Para), seleccione **Win32 Debug (Depurar Win32).**

3.  En la **pestaña Depurar** , en el **cuadro Categoría** , seleccione **General**.

4.  En el cuadro **Ejecutable** para la sesión de depuración, escriba la ruta de acceso completa para Dllhost.exe, seguida de un argumento que especifique el identificador de aplicación de la aplicación COM+ que contiene el componente.

    > [!Note]  
    > Con la herramienta administrativa Servicios de componentes, encontrará el identificador de la  aplicación en la **pestaña General** del cuadro de diálogo Propiedades de la aplicación COM+. El siguiente es un ejemplo:

     

    > [!Note]  
    > C: \\ Winnt \\ System32 \\Dllhost.exe /ProcessID:{applicationID}

     

5.  Haga clic en **OK**.

Ahora puede establecer puntos de interrupción, iniciar el depurador y empezar a realizar llamadas al componente.

## <a name="debugging-library-application-components-with-visual-c"></a>Depurar componentes de aplicación de biblioteca con Visual C++

Para depurar componentes en una aplicación de biblioteca, debe configurar el proyecto del cliente porque el proceso del cliente hospedará la aplicación de biblioteca.

**Para habilitar la depuración de aplicaciones de biblioteca con Visual C++**

1.  En Visual C++, en el menú **Project,** haga clic **en Configuración**.

2.  En el **cuadro Project Configuración** de diálogo, en el cuadro **Configuración para** , haga clic en **Depurar Win32**.

3.  En la **pestaña Depurar** , en el **cuadro Categoría** , haga clic en Archivos **DLL adicionales**.

4.  En la **lista** Módulos, agregue los archivos DLL de componente en la aplicación de biblioteca. Esto le permite establecer puntos de interrupción antes de que el archivo DLL se cargue realmente.

5.  Haga clic en **OK**.

## <a name="debugging-without-visual-c"></a>Depuración sin Visual C++

Independientemente de si usa o no Visual C++ para la  depuración, puede usar la opción Iniciar en el depurador para especificar el depurador en el que se deben ejecutar los componentes.

**Para especificar un depurador desde la herramienta administrativa Servicios de componentes**

1.  En el árbol de consola, seleccione la aplicación de biblioteca COM+ que contiene los componentes que desea depurar.

2.  Haga clic con el botón derecho en la aplicación y, a continuación, haga clic **en Propiedades.**

3.  En el cuadro de diálogo **Propiedades de** la aplicación, haga clic en **la pestaña** Avanzadas.

4.  En **Depuración,** active la casilla **Iniciar** en el depurador.

5.  En el cuadro **Ruta de acceso del** depurador, escriba la ruta de acceso al depurador que desea usar. También puede hacer clic en **Examinar** para buscar el depurador. A continuación se muestra un ejemplo: C: \\ Winnt \\ System32 \\Ntsd.exe.

6.  Haga clic en **OK**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depuración de componentes escritos en Visual Basic](debugging-components-written-in-visual-basic.md)
</dt> </dl>

 

 



