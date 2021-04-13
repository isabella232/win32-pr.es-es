---
title: Administración de cuotas para shells remotos
description: La administración de cuotas permite a los usuarios administrar los recursos del sistema de forma más eficaz.
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1310efd37b913ae0bf8394015f6df792711ac6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357543"
---
# <a name="quota-management-for-remote-shells"></a>Administración de cuotas para shells remotos

La administración de cuotas permite a los usuarios administrar los recursos del sistema de forma más eficaz. Administración remota de Windows (WinRM) ha agregado un conjunto específico de cuotas que proporcionan una mejor calidad de servicio, ayudan a evitar los problemas de denegación de servicio y asignan recursos del servidor a los usuarios simultáneos. El conjunto de cuotas de WinRM se basa en la infraestructura de cuota que se implementa para el servicio Internet Information Services (IIS).

La implementación de cuotas ayudará a evitar la degradación del rendimiento y los problemas de denegación de servicio al hacer lo siguiente:

-   Limitar el número de shells y procesos de Shell que un usuario puede crear
-   Limitar el número máximo de usuarios simultáneos
-   Administrar la cantidad de memoria que se asigna a un shell
-   Establecer un tiempo de espera para los shells inactivos

## <a name="quota-settings"></a>Configuración de cuota

Las siguientes cuotas deben aplicarse para la administración remota de Shell. Estas cuotas se pueden configurar a través de la utilidad WinRM o a través de la configuración de directiva de grupo. Los valores configurados por una directiva de grupo sustituyen a las cuotas establecidas por la utilidad WinRM. Para obtener más información sobre la configuración de directivas de grupo para WinRM, consulte [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).

<dl> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout
</dt> <dd>

Tiempo máximo en milisegundos antes de que se elimine un shell remoto inactivo. El valor predeterminado es 180000 milisegundos. El tiempo mínimo es de 1000 milisegundos.

</dd> <dt>

<span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell
</dt> <dd>

Número máximo de procesos permitidos por Shell, incluidos los procesos secundarios del shell. El valor predeterminado es 25.

</dd> <dt>

<span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB
</dt> <dd>

Cantidad máxima de memoria asignada por Shell, incluidos los procesos secundarios del shell. El valor predeterminado es 1024 MB.

> [!Note]  
> No se admite el comportamiento si MaxMemoryPerShellMB está establecido en un valor que es menor que el valor predeterminado.

 

</dd> <dt>

<span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser
</dt> <dd>

Número máximo de shells por usuario. El valor predeterminado es 30.

</dd> <dt>

<span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers
</dt> <dd>

Número máximo de usuarios simultáneos que pueden abrir shells. El valor predeterminado es 10.

</dd> </dl>

## <a name="deprecated-quotas"></a>Cuotas desusadas

WinRM 2,0 establece la cuota de MaxShellRunTime en solo lectura. Cambiar el valor de esta cuota no tendrá ningún efecto en los shells remotos.

## <a name="retrieving-quota-configuration-information"></a>Recuperando información de configuración de cuota

Para comprobar la configuración de la cuota, escriba **WinRM Get WinRM/config**.

El siguiente fragmento de código es un ejemplo basado en texto de una configuración de WinRM con la configuración de cuota predeterminada.

``` syntax
Config

          ...         

          Winrs

                   AllowRemoteShellAccess = true

                   IdleTimeout = 7200000

                   MaxConcurrentUsers = 10

                   MaxProcessesPerShell = 25

                   MaxMemoryPerShellMB = 1024

                   MaxShellsPerUser = 30
```

## <a name="configuring-shell-quotas"></a>Configuración de cuotas de Shell

Las cuotas se pueden establecer a través de un valor directiva de grupo o manualmente. Para obtener más información sobre las opciones de configuración específicas, vea [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).

**Para establecer una cuota con directiva de grupo**

1.  Abra una ventana de símbolo del sistema como administrador.
2.  En el símbolo del sistema, escriba **gpedit. msc**. Se abre la ventana **Editor de objetos de directiva de grupo** .
3.  Busque el **administración remota de Windows** y los objetos de directiva de grupo de **Shell remoto de Windows** (GPO) en **configuración del equipo \\ plantillas administrativas componentes de \\ Windows**.
4.  En la pestaña **extendido** , seleccione una opción para ver una descripción. Haga doble clic en un valor para editarlo.

**Para establecer una cuota manualmente**

1.  Abra una ventana de símbolo del sistema como administrador.
2.  En el símbolo del sistema, escriba **WinRM Set WinRM/config/Winrs ' @ { ***<Quota>*** = " ***<Value>*** "} '**

Por ejemplo, para aumentar el número máximo de shells por usuario de 5 a 7, escriba **WinRM Set WinRM/config/Winrs ' @ {MaxShellsPerUser = "7"} '**.

 

 




