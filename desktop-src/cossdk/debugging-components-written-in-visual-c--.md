---
description: Cuando esté listo para depurar la funcionalidad de COM+ en los componentes de Microsoft Visual C++, puede configurar Visual C++ proyecto o la herramienta administrativa Servicios de componentes para iniciar el depurador.
ms.assetid: 206467ac-108a-49de-a884-66959dc77650
title: Depurar componentes escritos en Visual C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e4b6324cc69531f09612c2af37fa03a036fd4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705270"
---
# <a name="debugging-components-written-in-visual-c"></a>Depurar componentes escritos en Visual C++

Cuando esté listo para depurar la funcionalidad de COM+ en los componentes de Microsoft Visual C++, puede configurar Visual C++ proyecto o la herramienta administrativa Servicios de componentes para iniciar el depurador. Si usa Visual C++, puede depurar con un cliente remoto mediante la depuración Just-in-Time (JIT) y OLE RPC. Si no puede ejecutar el cliente en el depurador o si el cliente se está ejecutando en otro equipo, puede usar la configuración **Inicio de com+ en el depurador** . Lo encontrará en la herramienta administrativa Servicios de componentes como una casilla en la pestaña **Opciones avanzadas** del cuadro de diálogo **propiedades** de la aplicación com+.

Cuando haya terminado la depuración, debe cerrar las aplicaciones COM+ que está depurando. Si se deja de ejecutar un proceso de servidor, es posible que reciba un mensaje de error la próxima vez que intente compilar un archivo DLL cuando el archivo DLL existente todavía esté cargado en la memoria. Para cerrar una aplicación COM+, haga clic con el botón secundario en la aplicación en el árbol de consola y, a continuación, haga clic en **apagar**.

> [!Note]  
> Si utiliza transacciones, es posible que también desee aumentar el tiempo de espera de la transacción, cuyo valor predeterminado es de 60 segundos. También puede especificar un valor de 0, con lo que se especifica de forma eficaz un período de tiempo de espera de transacción infinito. Use la herramienta administrativa Servicios de componentes para cambiar el valor de tiempo de espera de la transacción en la pestaña **Opciones** de la ventana **propiedades de mi PC** .

 

## <a name="debugging-server-application-components-with-visual-c"></a>Depurar componentes de la aplicación de servidor con Visual C++

Al depurar las aplicaciones de servidor COM+, es posible que desee depurar las llamadas remotas cargando tanto el cliente como la aplicación de servidor en el depurador. Con Visual C++, puede depurar las llamadas remotas a los componentes a través de la configuración Just-in-Time (JIT) y OLE RPC. La configuración JIT hace que el componente compilado inicie el depurador de Visual C++ cuando se produce un error. la configuración de OLE RPC permite al depurador pasar del cliente al componente mientras se recorre el código.

Cuando estas características están habilitadas, puede iniciar el cliente en el depurador. Cuando el cliente realiza una llamada al componente, el depurador entrará en el código del componente en el proceso del servidor, incluso si el servidor está en un equipo diferente de la red. Si es necesario, se inicia automáticamente una sesión de depuración en el equipo servidor. Del mismo modo, la ejecución paso a paso después de la instrucción return en el código del componente devolverá la depuración a la siguiente instrucción en el código del cliente.

> [!Note]  
> Es posible que pueda guardar algunos pasos mediante el uso de la configuración **de inicio de com+ en el depurador** . Esto le permite especificar el depurador Visual C++ (u otro) sin tener que realizar una configuración de depuración especial en el entorno de Visual C++. Lo encontrará en la herramienta administrativa Servicios de componentes como una casilla en la pestaña **Opciones avanzadas** del cuadro de diálogo **propiedades** de la aplicación com+. Para obtener más información, vea "depuración sin Visual C++" en este tema.

 

Cuando la aplicación COM+ que contiene el componente es una aplicación de servidor, debe empezar por cerrar la aplicación mediante la herramienta administrativa Servicios de componentes. Para ello, haga clic con el botón secundario en la aplicación COM+ en el árbol de consola y, a continuación, haga clic en **apagar**.

**Para habilitar la depuración RPC en Visual C++**

1.  En Visual C++, en el menú **herramientas** , haga clic en **Opciones**.

2.  En el cuadro de diálogo **Opciones** , en la pestaña **depurar** , active las casillas depuración de **OLE RPC** y **depuración Just-in-Time** .

3.  Haga clic en **OK**.

Para comenzar la depuración, inicie el proyecto de cliente en el depurador.

También puede depurar el componente sin iniciar el cliente en el depurador. En este caso, el componente debe iniciar el depurador por sí mismo. Para ello, el proyecto de componente debe especificar un archivo ejecutable para la sesión de depuración, junto con el identificador de la aplicación COM+.

**Para permitir que un componente de aplicación de servidor inicie el depurador de Visual C++**

1.  En el menú **proyecto** , haga clic en **configuración**.

2.  En el cuadro de diálogo **configuración del proyecto** , en el cuadro **configuración para** , seleccione **depuración de Win32**.

3.  En la pestaña **depurar** , en el cuadro **categoría** , seleccione **General**.

4.  En el cuadro **ejecutable para sesión de depuración** , escriba la ruta de acceso completa de Dllhost.exe, seguido de un argumento que especifique el identificador de la aplicación com+ que contiene el componente.

    > [!Note]  
    > Con la herramienta administrativa Servicios de componentes, encontrará el identificador de la aplicación en la pestaña **General** del cuadro de diálogo **propiedades** de la aplicación com+. El siguiente es un ejemplo:

     

    > [!Note]  
    > C: \\ WinNT \\ system32 \\Dllhost.exe/ProcessId: {applicationID}

     

5.  Haga clic en **OK**.

Ahora puede establecer puntos de interrupción, iniciar el depurador y comenzar a realizar llamadas al componente.

## <a name="debugging-library-application-components-with-visual-c"></a>Depurar componentes de aplicación de biblioteca con Visual C++

Para depurar componentes en una aplicación de biblioteca, debe configurar el proyecto del cliente porque el proceso del cliente hospedará la aplicación de biblioteca.

**Para habilitar la depuración de aplicaciones de biblioteca con Visual C++**

1.  En Visual C++, en el menú **proyecto** , haga clic en **configuración**.

2.  En el cuadro de diálogo **configuración del proyecto** , en el cuadro **configuración de** , haga clic en **depuración de Win32**.

3.  En la pestaña **depurar** , en el cuadro **categoría** , haga clic en **archivos dll adicionales**.

4.  En la lista **módulos** , agregue los archivos DLL del componente en la aplicación de biblioteca. Esto le permite establecer puntos de interrupción antes de que se cargue realmente el archivo DLL.

5.  Haga clic en **OK**.

## <a name="debugging-without-visual-c"></a>Depuración sin Visual C++

Tanto si usa como si no Visual C++ para la depuración, puede usar la configuración **iniciar en el depurador** para especificar el depurador en el que deben ejecutarse los componentes.

**Para especificar un depurador desde la herramienta administrativa Servicios de componentes**

1.  En el árbol de consola, seleccione la aplicación de biblioteca COM+ que contiene los componentes que desea depurar.

2.  Haga clic con el botón secundario en la aplicación y, a continuación, haga clic en **propiedades**.

3.  En el cuadro de diálogo **propiedades** de la aplicación, haga clic en la pestaña **Opciones avanzadas** .

4.  En **depuración**, active la casilla **iniciar en el depurador** .

5.  En el cuadro **ruta de acceso del depurador** , escriba la ruta de acceso al depurador que desee usar. También puede hacer clic en **examinar** para buscar el depurador. A continuación se encuentra un ejemplo: C: \\ WinNT \\ system32 \\Ntsd.exe.

6.  Haga clic en **OK**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depurar componentes escritos en Visual Basic](debugging-components-written-in-visual-basic.md)
</dt> </dl>

 

 



