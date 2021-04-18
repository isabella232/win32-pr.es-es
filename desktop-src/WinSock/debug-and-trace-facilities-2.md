---
description: Funciones de depuración y seguimiento, y Windows Sockets 2.
ms.assetid: eb29fc21-92d6-4471-860a-fd1c531686f6
title: Funciones de depuración y seguimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7288c6b4d72a7a375ee16da23a25b0a04a46df91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696387"
---
# <a name="debug-and-trace-facilities"></a>Funciones de depuración y seguimiento

Los desarrolladores de aplicaciones de Windows Sockets 2 necesitan aislar errores en:

-   Aplicación.
-   *Ws2 \_32.dll* o uno de los archivos dll de correcciones de compatibilidad (shim).
-   Proveedor de servicios.

Windows Sockets 2 se ocupa de esta necesidad a través de varios componentes y características:

-   Compatibilidad integrada con el seguimiento de Winsock en Windows Vista y versiones posteriores.
-   Una versión de depuración especialmente diseñada *del \_32.dllWs2* en Windows Vista.
-   Una función de depuración y seguimiento primitiva independiente para su uso en Windows Server 2003 y Windows XP.

## <a name="winsock-tracing-using-event-tracing-for-windows"></a>Seguimiento de Winsock con seguimiento de eventos para Windows

La compatibilidad integrada con el seguimiento de Winsock mediante el seguimiento de eventos para Windows (ETW) se incluye en Windows Vista y versiones posteriores. Este es el método preferido para realizar el seguimiento de llamadas Winsock en Windows Vista y versiones posteriores. El seguimiento de Winsock con ETW es ligero y funciona en versiones comerciales de Windows. No se requieren software ni componentes adicionales. Esta característica solo debe estar habilitada en Windows Vista y versiones posteriores. Para obtener información más detallada, consulte los temas de [seguimiento de Winsock](winsock-tracing.md) .

## <a name="using-a-debug-version-of-ws2_32dll"></a>Usar una versión de depuración de Ws2 \_32.dll

La combinación de una versión de depuración del *\_32.dllWs2* en Windows Vista y el seguimiento de Winsock permite supervisar todas las llamadas a procedimientos a través de la API o el SPI de Windows Sockets 2 y, en cierta medida, controlarlas.

Si una versión del kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista se instala en la ubicación predeterminada, las versiones de depuración de la *\_32.dllWs2* para varias arquitecturas se encuentran en la siguiente carpeta:

**C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 6.0 \\ noredir**

Debe usarse una versión comprobada del *\_32.dllWs2* que coincida con la versión de Windows y el Service Pack que se está probando. Tenga en cuenta que es posible que se hayan aplicado revisiones de seguridad que actualizaron el *\_32.dllWs2* en el sistema de prueba. Los Windows SDK para Windows Vista y las suscripciones de DVD/CD del kit de desarrollo de software (SDK) de la plataforma anterior incluyen compilaciones comprobadas para las distintas versiones de Windows. Debe usar la misma versión comprobada de la *\_32.dllWs2* como la versión comercial que se usó en el sistema que se está probando. Tenga en cuenta también que el comportamiento que se ejecuta en una compilación comprobada no será el mismo que cuando se ejecuta con una compilación comercial.

**Nota:**  El Windows SDK para Windows Server 2008 y versiones posteriores ya no incluye versiones de depuración especiales del *\_32.dllWs2*. En su lugar, los desarrolladores deben usar el seguimiento de Winsock mediante ETW, ya que esta característica no requiere compilaciones de depuración.

## <a name="winsock-debug-and-trace-facility-on-windows-server-2003-and-windows-xp"></a>Winsock Debug and Trace Facility en Windows Server 2003 y Windows XP

Las versiones anteriores de Windows anteriores a Windows 8 y Windows Server 2012 admiten una característica de depuración y seguimiento de primitivos independiente que se incluye como ejemplo con el Windows SDK y el SDK de la plataforma anterior. La característica de depuración/seguimiento solo se debe usar en Windows Server 2003 y Windows XP, donde no se admite el seguimiento de Winsock.

Si el Windows SDK para Windows 7 está instalado en la ubicación predeterminada, esta característica de seguimiento de Winsock primitivo se instala en la siguiente carpeta:

**C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ NetDs \\ Winsock \\ DT \_ dll**

El archivo *DbgSpec.doc* de esta carpeta proporciona documentación sobre esta utilidad de seguimiento primitivo. El código de ejemplo de la \_ carpeta DT dll se debe compilar para usar esta utilidad. Los desarrolladores pueden usar el código fuente para desarrollar versiones del archivo DLL de depuración y seguimiento que satisfagan sus necesidades específicas.

Tenga en cuenta que esta característica de seguimiento de Winsock simple solo funcionará con la versión de depuración de *Ws2 \_32.dll* instalado. Por lo tanto, tendrá que obtener una versión comprobada de la *\_32.dllWs2* que coincida con la versión de Windows y el Service Pack en el que está probando.

Una limitación de esta utilidad de \_ seguimiento DT dll de DT es que el código de ejemplo utiliza un bloqueo global (sección crítica) para cada llamada de función de Winsock. Por lo tanto, esta utilidad no es útil para tratar las condiciones de carrera. El código de ejemplo debe reescribirse sustancialmente para que esta utilidad de seguimiento resulte útil para solucionar la mayoría de los problemas reales de Winsock (reemplazando los bloqueos globales). Este código de ejemplo permite a los desarrolladores realizar un seguimiento de las llamadas a procedimientos, las devoluciones de procedimientos, los valores de parámetros y los valores devueltos.

Los desarrolladores pueden utilizar este mecanismo primitivo para realizar el seguimiento de las llamadas a procedimientos, las devoluciones de procedimientos, los valores de parámetros y los valores devueltos. Los valores de parámetro y los valores devueltos se pueden modificar en la llamada de procedimiento o el procedimiento devuelto. Si lo desea, se puede impedir o redirigir una llamada a un procedimiento. Con acceso a este nivel de información y control, un desarrollador puede aislar mejor un problema en la aplicación, *Ws2 \_32.dll* o proveedor de servicios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> </dl>

 

 



