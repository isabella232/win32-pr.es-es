---
description: El uso de Microsoft Visual Basic entorno de desarrollo integrado (IDE) para la depuración proporciona a los desarrolladores de Visual Basic acceso a herramientas conocidas y facilidad de uso.
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Depuración en el IDE de Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 284e97a766256cd281b3515bdd142d15ff5208e2c1a1555438c428daeca8f3a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548014"
---
# <a name="debugging-in-the-visual-basic-ide"></a>Depuración en el IDE de Visual Basic

El uso de Microsoft Visual Basic entorno de desarrollo integrado (IDE) para la depuración proporciona a los desarrolladores de Visual Basic acceso a herramientas conocidas y facilidad de uso. Aunque a la larga muchos componentes tendrán que depurarse más por completo mediante el entorno de Microsoft Visual C++, una estrategia podría ser depurar primero tanta funcionalidad como sea posible con Visual Basic. Por ejemplo, es posible que desee usar el IDE de Visual Basic para la depuración en COM+ cuando aún no esté depurando multithreading, seguimiento de componentes, llamadas remotas o aislamiento de procesos.

En general, cuando se usa el Visual Basic para la depuración, primero se compila el proyecto y se agrega el archivo DLL a una aplicación COM+. A continuación, establezca la compatibilidad binaria para el proyecto, haciendo referencia al archivo DLL que hizo e inicie el proyecto para comenzar la depuración.

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a>Directrices generales para la depuración en Visual Basic Environment

-   Mientras se depura mediante Visual Basic, COM+ trata los componentes de Visual Basic como si pertenezcan a una aplicación de biblioteca, incluso si los componentes están registrados como pertenecientes a una aplicación de servidor. Dado que se ejecuta como una aplicación de biblioteca, los iconos de componente de la herramienta administrativa Servicios de componentes no giran a medida que se depuran los componentes.
-   Si cambia los atributos de transacción en un componente durante la depuración o realiza un cambio en el código fuente que requiere que Visual Basic genere un nuevo CLSID o ProgID, asegúrese de eliminar y reinstalar la aplicación COM+ que contiene el componente. Si ha establecido la compatibilidad binaria para el componente, se le advertirá de que se han producido cambios.

## <a name="notes-on-debugging-within-a-com-application"></a>Notas sobre la depuración dentro de una aplicación COM+

-   Si realiza cambios en el IDE de Visual Basic en las interfaces del componente, los nombres de clase, los nombres de proyecto, la compatibilidad transaccional u otras configuraciones, puede haber discrepancias entre los datos de configuración en el explorador de Servicios de componentes y la configuración real que se ejecuta en el depurador de Visual Basic.
-   No exporte una aplicación COM+ mientras depura un componente en la aplicación. COM+ tratará el entorno Visual Basic desarrollo como componente.
-   Si ejecuta un componente fuera del depurador y, a continuación, decide iniciar la depuración, es posible que una instancia del componente todavía se esté ejecutando en COM+ al iniciarlo en el depurador. COM+ detectará esta condición e intentará apagar silenciosamente la instancia que controla. Para evitar este problema, quite el componente de la herramienta administrativa Servicios de componentes antes de comenzar la depuración.

**Para depurar mediante el Visual Basic de depuración**

1.  Abra el proyecto de componente en Visual Basic.

2.  Compile el componente y, a continuación, establezca la compatibilidad binaria del proyecto en el componente compilado.

3.  Establezca la propiedad MTSTransactionMode en un valor distinto de 0: NotAnMTSObject. Al iniciar el proyecto, esta configuración le Visual Basic activar el componente en COM+.

4.  En el **menú Project,** haga clic en **Propiedades** y, a continuación, escriba el programa de inicio en la **pestaña** Depuración. El programa de inicio es el ejecutable de cliente que llama a este componente.

    > [!Note]  
    > El programa de inicio debe ser local para el componente que está depurando.

     

5.  Presione la tecla F5 para empezar a depurar el componente.

Después de presionar F5, Visual Basic inicia la aplicación cliente y ejecuta el componente en modo de depuración. Puede colocar puntos de interrupción en el código del componente y establecer las alertas en las variables.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con la depuración de com+ Visual Basic con MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Depuración de componentes Visual Basic compilados](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



