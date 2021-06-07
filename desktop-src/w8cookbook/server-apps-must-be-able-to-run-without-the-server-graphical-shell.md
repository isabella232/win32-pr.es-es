---
title: Restricciones de Shell gráfico de servidor
description: Las aplicaciones de servidor deben poder ejecutarse sin el Shell gráfico de servidor
ms.assetid: 8F531497-B64D-4E79-AD7A-790EFDC6ADFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2a3002fc2395faba3e07d90a2322c770fe3ee9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443226"
---
# <a name="server-apps-must-be-able-to-run-without-the-server-graphical-shell"></a>Las aplicaciones de servidor deben poder ejecutarse sin el Shell gráfico de servidor

## <a name="platform"></a>Plataforma

**Servidores:** Windows Server 2012 

## <a name="description"></a>Descripción

Shell gráfico de servidor, la característica que incluye Explorador de Windows y Internet Explorer, se instala de forma predeterminada en las instalaciones de "Servidor con una GUI" de Windows Server 2012. La característica Shell gráfico de servidor se puede desinstalar para reducir la superficie de mantenimiento y rendimiento potencial, lo que limita el número de reinicios en los que puede incurrir el servidor, a la vez que permite que las herramientas de administración se ejecuten localmente en el servidor.

Después de que un administrador desinstale el Shell gráfico del servidor, el servidor se encuentra en la configuración de interfaz de servidor mínima:

![configuración de la interfaz gráfica de shell de servidor](images/minimalserverinterface.png)

A continuación, los administradores pueden optar por ejecutar en la configuración de interfaz de servidor mínima (que incluye un conjunto de herramientas de administración local), como valor predeterminado, en lugar de en el servidor con una configuración de GUI. Esto permite la supervisión y administración locales, a la vez que se reduce el uso de recursos y la frecuencia de mantenimiento.

Los administradores pueden volver a instalar el Shell gráfico del servidor más adelante si necesitan la funcionalidad dentro de él. (Los administradores también pueden empezar desde una instalación de Server Core y "compilar" a la configuración de interfaz de servidor mínima mediante la funcionalidad Características a petición).

Las aplicaciones de servidor deben ser capaces de ejecutarse en la configuración de interfaz de servidor mínima para aprovechar el uso reducido de recursos y la superficie de mantenimiento. Esta funcionalidad se puede lograr al permitir que el administrador decida no instalar partes de la aplicación que necesita el Shell gráfico de servidor o detectar la presencia del Shell gráfico de servidor y deshabilitar algunos aspectos de la aplicación.

La interfaz de servidor mínima tiene una superficie reducida de recursos y mantenimiento, ya que muchas API y archivos binarios incluidos en el Shell gráfico de servidor no están disponibles en esta configuración. Si procede, las aplicaciones de servidor también deben permitir la administración remota (preferiblemente a través de Windows PowerShell Remoting) desde otra instalación de Windows Server o cliente de Windows. Esto permite una mejor administración centralizada de una o varias máquinas en la configuración de interfaz de servidor mínima o de máquinas en una configuración de superficie incluso menor, como Server Core.

## <a name="manifestation"></a>Manifestación

Si una aplicación requiere cualquiera de las API o archivos binarios que no están disponibles en la configuración de interfaz de servidor mínima, es posible que no se muestre correctamente en la pantalla o no se pueda usar.

## <a name="mitigation"></a>Mitigación

Los desarrolladores de aplicaciones de servidor deben identificar las partes de sus aplicaciones que requieren cualquiera de las API o binarios quitados e incluir información para el administrador del servidor que identifica las partes de la aplicación que no se ejecutarán correctamente cuando se usa la interfaz de servidor mínima. Si esas partes de la aplicación se pueden instalar opcionalmente o no son absolutamente necesarias para la funcionalidad del producto, la aplicación todavía se puede instalar y ejecutar en la configuración de interfaz de servidor mínima.

Si la aplicación no se puede usar en absoluto sin el Shell gráfico de servidor, esta limitación debe documentarse y se debe indicar al administrador del servidor que instale el Shell gráfico del servidor. (Si se agrega a una instalación de Server Core, puede que sea necesario agregar características mediante características a petición). Además, la aplicación debe comprobar al inicio que todos los archivos necesarios están disponibles, ya que el Shell gráfico del servidor se puede desinstalar en cualquier momento antes o después de la instalación de la aplicación.

## <a name="solution"></a>Solución

Confíe en el conjunto de dependencias más pequeño posible y modularice las aplicaciones para que la funcionalidad principal de la aplicación pueda funcionar sin necesidad de tener instalados componentes de interfaz de usuario más pesados. Desarrolle aplicaciones que no requieran ninguna de las API o archivos binarios quitados y, en su lugar, confíe en la funcionalidad contenida en la interfaz de servidor mínima o Server Core. Esto reducirá los requisitos de mantenimiento y mejorará el rendimiento y la satisfacción del usuario.

Cuando hay partes de una aplicación que podrían agregar una funcionalidad significativa cuando el Shell gráfico de servidor está disponible, los desarrolladores de aplicaciones pueden:

-   Permitir que estas características adicionales que usan el Shell gráfico de servidor se instalen opcionalmente, de modo que se puedan omitir en las instalaciones en una configuración de interfaz de servidor mínima.
-   Detectar la presencia de Shell gráfico de servidor y adaptar el comportamiento de la aplicación

Los desarrolladores de aplicaciones también deben asegurarse de que las aplicaciones de servidor se puedan administrar de forma remota siempre que sea posible y adecuado.

## <a name="detecting-minimal-server-interface-and-server-core"></a>Detección de interfaz de servidor mínima y Server Core

Windows Server instalará un valor del Registro correspondiente para cada nivel de servidor instalado. Puede consultar la existencia de estas claves para determinar si las características Shell gráfico del servidor o Interfaz de servidor mínima están instaladas y habilitadas.

HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Server \\ ServerLevels:



|   &nbsp;         | Server Core | Interfaz de servidor básica | Shell gráfico de servidor |
|------------------|-------------|--------------------------|------------------------|
| ServerCore=1     | X           | X                        | X                      |
| Server-GuiMgmt=1 |             | X                        | X                      |
| ServerGuiShell=1 |             |                          | X                      |



 

Una "X" en la tabla anterior significa que la clave del Registro estará presente cuando se instale la característica correspondiente.

Tenga en cuenta que estos niveles de servidor son aditivos; si el Shell gráfico del servidor está instalado, así como la interfaz mínima del servidor y Server Core. En ese caso, ambas claves del Registro estarán presentes.

## <a name="tests"></a>Pruebas

Inspeccione el código de la aplicación en busca de requisitos que usen cualquiera de las API y los archivos binarios quitados. Después de quitar las instancias de estos archivos binarios de "aplicación principal", pruebe la aplicación en un entorno que no incluya el Shell gráfico del servidor. Herramientas como el Monitor de procesos pueden ayudar con esto.

Si no puede interrumpir completamente el uso de estas API y archivos binarios, asegúrese de que la aplicación produce un error correctamente cuando se ejecuta en la interfaz de servidor mínima o Server Core.

## <a name="resources"></a>Recursos

-   [Documentos existentes de Server Core en MSDN](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 