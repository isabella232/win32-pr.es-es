---
description: Depuración y seguimiento de instalaciones y Windows Sockets 2.
ms.assetid: eb29fc21-92d6-4471-860a-fd1c531686f6
title: Depuración y seguimiento de instalaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0617aa8fc18e90b0c3e366a7ab14f1457cb26471865bfcc97682801a858565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741372"
---
# <a name="debug-and-trace-facilities"></a>Depuración y seguimiento de instalaciones

Windows Los desarrolladores de aplicaciones de Sockets 2 deben aislar los errores en:

-   Aplicación.
-   El *archivo Ws2 \_32.dll* o uno de los archivos DLL de compatibilidad de correcciones de compatibilidad.
-   Proveedor de servicios.

Windows Sockets 2 aborda esta necesidad a través de varios componentes y características:

-   Compatibilidad integrada con el seguimiento de Winsock en Windows Vista y versiones posteriores.
-   Una versión de depuración especialmente ideada del32.dll *Ws2 \_* en Windows Vista.
-   Una instalación de depuración y seguimiento primitiva independiente para su uso en Windows Server 2003 y Windows XP.

## <a name="winsock-tracing-using-event-tracing-for-windows"></a>Seguimiento de Winsock mediante seguimiento de eventos para Windows

La compatibilidad integrada con el seguimiento de Winsock mediante seguimiento de eventos para Windows (ETW) se incluye en Windows Vista y versiones posteriores. Este es el método preferido para realizar el seguimiento de llamadas winsock en Windows Vista y versiones posteriores. El seguimiento de Winsock con ETW es ligero y funciona en versiones comerciales de Windows. No se requiere software ni componentes adicionales. Esta característica solo debe habilitarse en Windows Vista y versiones posteriores. Para obtener información más detallada, consulte los temas [de seguimiento de Winsock.](winsock-tracing.md)

## <a name="using-a-debug-version-of-ws2_32dll"></a>Usar una versión de depuración de Ws2 \_32.dll

La combinación de una versión de depuración de *Ws2 \_32.dll* en el seguimiento de Windows Vista y Winsock permite supervisar todas las llamadas a procedimientos a través de la API o SPI de Windows Sockets 2 y, en cierta medida, controlar.

Si una versión del Kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista está instalada en la ubicación predeterminada, las versiones de depuración del32.dllde *Ws2 \_ para* varias arquitecturas se encuentran en la carpeta siguiente:

**C: \\ Archivos de programa sdk de Microsoft Windows \\ \\ \\ v6.0 \\ NoRedist**

Se debe usar una versión comprobada del32.dll *Ws2 \_* que coincida con la versión de Windows y el Service Pack en el que se está probando. Tenga en cuenta que es posible que se hayan aplicado revisiones de seguridad que actualizaron el32.dll *Ws2 \_* en el sistema de prueba. El SDK Windows para Windows Vista y las suscripciones anteriores de DVD/CD del Kit de desarrollo de software de plataforma (SDK) incluyen compilaciones activadas para las distintas versiones de Windows. Debe usar la misma versión comprobada de la versión *32.dllWs2 \_* que la versión comercial que se usó en el sistema que se está probando. Tenga en cuenta también que el comportamiento que se ejecuta en una compilación activada no será el mismo que el de una compilación comercial.

**Nota**  El SDK Windows para Windows Server 2008 y versiones posteriores ya no incluye versiones de depuración especiales de *Ws2 \_32.dll*. En su lugar, los desarrolladores deben usar el seguimiento de Winsock mediante ETW, ya que esta característica no requiere compilaciones de depuración.

## <a name="winsock-debug-and-trace-facility-on-windows-server-2003-and-windows-xp"></a>Instalación de depuración y seguimiento de Winsock en Windows Server 2003 y Windows XP

Las versiones anteriores de Windows anteriores a Windows 8 y Windows Server 2012 admiten una instalación de depuración y seguimiento primitiva independiente que se incluye como ejemplo con el SDK de Windows y el SDK de plataforma anterior. La instalación de depuración y seguimiento solo debe usarse en Windows Server 2003 y Windows XP donde no se admite el seguimiento de Winsock.

Si el SDK Windows para Windows 7 está instalado en la ubicación predeterminada, esta característica primitiva de seguimiento de Winsock se instala en la carpeta siguiente:

**C: \\ Archivos de programa Sdk de Microsoft Windows archivos de ejemplo \\ \\ \\ v7.0 \\ \\ NetDs \\ winsock dt \\ \_ dll**

El *DbgSpec.doc* de esta carpeta proporciona documentación sobre esta instalación de seguimiento primitivo. El código de ejemplo de la carpeta \_ dt dll debe compilarse para usar esta utilidad. Los desarrolladores pueden usar el código fuente para desarrollar versiones del archivo DLL de depuración o seguimiento que satisfagan sus necesidades específicas.

Tenga en cuenta que esta característica primitiva de seguimiento de Winsock solo funcionará con la versión de depuración de *Ws2 \_32.dll* instalado. Por lo tanto, deberá obtener una versión comprobada de la32.dll *Ws2 \_* que coincida con la versión de Windows y el Service Pack en el que está probando.

Una limitación de esta instalación de seguimiento de dt dll primitiva es que el código de ejemplo usa un bloqueo \_ global (sección crítica) para cada llamada de función Winsock. Por lo tanto, esta instalación no es útil para tratar las condiciones de carrera. El código de ejemplo tendría que reescribirse considerablemente para que esta instalación de seguimiento sea útil para tratar con la mayoría de los problemas reales de Winsock (reemplazando los bloqueos globales). Este código de ejemplo permite a los desarrolladores realizar un seguimiento de las llamadas a procedimientos, devoluciones de procedimientos, valores de parámetro y valores devueltos.

Los desarrolladores pueden usar este mecanismo primitivo para realizar un seguimiento de las llamadas a procedimientos, las devoluciones de procedimientos, los valores de parámetro y los valores devueltos. Los valores de parámetro y los valores devueltos se pueden modificar en la llamada a procedimiento o en la devolución de procedimiento. Si lo desea, se puede evitar o redirigir una llamada a procedimiento. Con el acceso a este nivel de información y control, un desarrollador puede aislar mejor un problema en la aplicación, *Ws2 \_32.dll* o proveedor de servicios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> </dl>

 

 



