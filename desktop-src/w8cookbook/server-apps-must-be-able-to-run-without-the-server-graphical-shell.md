---
title: Restricciones de Shell gráfico de servidor
description: Las aplicaciones de servidor deben poder ejecutarse sin el shell gráfico de servidor
ms.assetid: 8F531497-B64D-4E79-AD7A-790EFDC6ADFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7666ae07a28d798a36d249bf37ab2d7719b9fba0
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "104421555"
---
# <a name="server-apps-must-be-able-to-run-without-the-server-graphical-shell"></a>Las aplicaciones de servidor deben poder ejecutarse sin el shell gráfico de servidor

## <a name="platform"></a>Plataforma

**Servidores** : Windows Server 2012 

## <a name="description"></a>Descripción

Shell gráfico de servidor, la característica que incluye el explorador de Windows e Internet Explorer, se instala de forma predeterminada en las instalaciones "servidor con una GUI" de Windows Server 2012. La característica Shell gráfico de servidor se puede desinstalar con el fin de reducir el potencial de mantenimiento y de rendimiento, lo que limita el número de reinicios que puede tener el servidor y, al mismo tiempo, permite que las herramientas de administración se ejecuten localmente en el servidor.

Después de que un administrador desinstale el shell gráfico de servidor, el servidor se encuentra en la configuración de interfaz de servidor básica:

![configuración de la interfaz de Shell gráfico de servidor](images/minimalserverinterface.png)

Los administradores pueden optar por ejecutarse en la configuración de interfaz de servidor básica (que incluye un conjunto de herramientas de administración locales), como valor predeterminado, en lugar de en el servidor con una configuración de GUI. Esto permite la supervisión y administración locales, a la vez que reduce tanto el uso de recursos como la frecuencia de mantenimiento.

Los administradores pueden volver a instalar el shell gráfico de servidor más adelante si necesitan la funcionalidad incluida en él. (Los administradores también pueden iniciar desde una instalación Server Core y "compilar" en la configuración de interfaz de servidor básica mediante la funcionalidad de características a petición).

Las aplicaciones de servidor deben ser capaces de ejecutarse en la configuración de interfaz de servidor básica para aprovechar el uso de recursos reducido y la superficie de servicio. Esta capacidad se puede lograr permitiendo al administrador elegir no instalar partes de la aplicación que necesita el shell gráfico de servidor, o detectando la presencia del shell gráfico de servidor y deshabilitando algunos aspectos de la aplicación.

La interfaz de servidor básica tiene una superficie de mantenimiento y recursos reducida porque muchas API y archivos binarios que se incluyen en el shell gráfico de servidor no están disponibles en esta configuración. Cuando corresponda, las aplicaciones de servidor también deben permitir la administración remota (preferiblemente a través de la comunicación remota de Windows PowerShell) desde otra instalación de cliente de Windows o Windows Server. Esto permite una mejor administración centralizada de uno o más equipos en la configuración de interfaz de servidor básica, o de máquinas en una configuración de superficie incluso inferior como Server Core.

## <a name="manifestation"></a>Manifestación

Si una aplicación requiere alguna de las API o archivos binarios que no están disponibles en la configuración de la interfaz de servidor básica, es posible que no se muestre correctamente en la pantalla o que no se pueda usar.

## <a name="mitigation"></a>Mitigación

Los desarrolladores de aplicaciones de servidor deben identificar las partes de sus aplicaciones que requieran cualquiera de las API o archivos binarios quitados e incluir información para el administrador del servidor que identifique las partes de la aplicación que no se ejecutarán correctamente cuando se use la interfaz de servidor básica. Si las partes de la aplicación se pueden instalar opcionalmente o no son absolutamente necesarias para la funcionalidad del producto, la aplicación se puede instalar y ejecutar con la configuración de la interfaz de servidor mínima.

Si no se puede usar la aplicación sin el shell gráfico de servidor, esta limitación debe estar documentada y se debe indicar al administrador del servidor que instale el shell gráfico de servidor. (Si se agrega a una instalación Server Core, esto podría requerir agregar características mediante características a petición). Además, la aplicación debe comprobar en el inicio que todos los archivos necesarios están disponibles, ya que el shell gráfico de servidor se puede desinstalar en cualquier momento antes o después de la instalación de la aplicación.

## <a name="solution"></a>Solución

Confíe en el conjunto de dependencias más pequeño posible y modular las aplicaciones para que la funcionalidad de la aplicación principal pueda funcionar sin necesidad de instalar componentes de interfaz de usuario más pesados. Desarrolle aplicaciones que no requieran ninguna de las API o archivos binarios quitados y confíe en la funcionalidad contenida en la interfaz de servidor básica o Server Core. Esto reducirá los requisitos de mantenimiento a la vez que mejora el rendimiento y la satisfacción del usuario.

Cuando hay partes de una aplicación que pueden agregar una funcionalidad importante cuando el shell gráfico de servidor está disponible, los desarrolladores de aplicaciones pueden:

-   Permite que se instalen de forma opcional estas características adicionales, por lo que se pueden omitir las instalaciones en una configuración de interfaz de servidor básica.
-   Detección de la presencia del shell gráfico de servidor y adaptación del comportamiento de la aplicación

Los desarrolladores de aplicaciones también deben asegurarse de que las aplicaciones de servidor se puedan administrar de forma remota siempre que sea posible y adecuadas.

## <a name="detecting-minimal-server-interface-and-server-core"></a>Detección de la interfaz de servidor mínima y Server Core

Windows Server instalará un valor de registro correspondiente para cada nivel de servidor instalado. Puede consultar la existencia de estas claves para determinar si las características Shell gráfico de servidor o interfaz de servidor mínima están instaladas y habilitadas.

HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Server \\ ServerLevels:



|                  | Server Core | Interfaz de servidor básica | Shell gráfico de servidor |
|------------------|-------------|--------------------------|------------------------|
| ServerCore = 1     | X           | X                        | X                      |
| Server-GuiMgmt = 1 |             | X                        | X                      |
| ServerGuiShell = 1 |             |                          | X                      |



 

Una "X" en la tabla anterior significa que la clave del registro estará presente cuando se instale la característica correspondiente.

Tenga en cuenta que estos niveles de servidor son aditivos; Si el shell gráfico de servidor está instalado, se trata de la interfaz de servidor básica y Server Core. En ese caso, las dos claves del registro estarán presentes.

## <a name="tests"></a>Pruebas

Inspeccione el código de la aplicación para conocer los requisitos que usan cualquiera de las API y los archivos binarios quitados. Una vez que haya quitado todas las instancias de de los archivos binarios de "aplicación principal", pruebe la aplicación en un entorno que no incluya el shell gráfico de servidor. Las herramientas como el monitor de procesos pueden ayudarle con esto.

Si no puede interrumpir por completo el uso de estas API y binarios, asegúrese de que la aplicación no funciona correctamente cuando se ejecuta en la interfaz de servidor básica o Server Core.

## <a name="resources"></a>Recursos

-   [Documentos existentes de Server Core en MSDN](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 