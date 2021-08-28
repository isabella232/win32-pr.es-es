---
title: Administración de cuotas para shells remotos
description: La administración de cuotas permite a los usuarios administrar los recursos del sistema de forma más eficaz.
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8cfa177d6f09552238471ff29d81d0ac0b7351
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883212"
---
# <a name="quota-management-for-remote-shells"></a>Administración de cuotas para shells remotos

La administración de cuotas permite a los usuarios administrar los recursos del sistema de forma más eficaz. Windows Administración remota (WinRM) ha agregado un conjunto específico de cuotas que proporcionan una mejor calidad de servicio, ayudan a evitar problemas de denegación de servicio y asignan recursos de servidor a usuarios simultáneos. El conjunto de cuotas de WinRM se basa en la infraestructura de cuota que se implementa para el servicio Internet Information Services (IIS).

La implementación de cuotas ayudará a evitar la degradación del rendimiento y los problemas de denegación de servicio haciendo lo siguiente:

-   Limitar el número de shells y procesos de shell que un usuario puede crear
-   Limitar el número máximo de usuarios simultáneos
-   Administración de la cantidad de memoria que se asigna a un shell
-   Establecimiento de un tiempo de espera para los shells que están inactivos

## <a name="quota-settings"></a>Cuota Configuración

Es necesario aplicar las siguientes cuotas para la administración remota del shell. Estas cuotas se pueden configurar a través de la utilidad winrm o a través directiva de grupo configuración. Configuración configurado por un directiva de grupo reemplaza las cuotas establecidas por la utilidad winrm. Para obtener más información sobre cómo establecer directivas de grupo para WinRM, vea Instalación y configuración [para Windows administración remota.](installation-and-configuration-for-windows-remote-management.md)

<dl> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout
</dt> <dd>

Tiempo máximo en milisegundos antes de que se elimine un shell remoto inactivo. El valor predeterminado es 180 000 milisegundos. El tiempo mínimo es de 1000 milisegundos.

</dd> <dt>

<span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell
</dt> <dd>

Número máximo de procesos permitidos por shell, incluidos los procesos secundarios del shell. El valor predeterminado es 25.

</dd> <dt>

<span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB
</dt> <dd>

Cantidad máxima de memoria asignada por shell, incluidos los procesos secundarios del shell. El valor predeterminado es 1024 MB.

> [!Note]  
> No se admite el comportamiento si MaxMemoryPerShellMB está establecido en un valor menor que el predeterminado.

 

</dd> <dt>

<span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser
</dt> <dd>

Número máximo de shells por usuario. El valor predeterminado es 30.

</dd> <dt>

<span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers
</dt> <dd>

Número máximo de usuarios simultáneos que pueden abrir shells. El valor predeterminado es 10.

</dd> </dl>

## <a name="deprecated-quotas"></a>Cuotas en desuso

WinRM 2.0 establece la cuota MaxShellRunTime en solo lectura. Cambiar el valor de esta cuota no tendrá ningún efecto en los shells remotos.

## <a name="retrieving-quota-configuration-information"></a>Recuperar información de configuración de cuota

Para comprobar los valores de configuración de cuota, escriba **winrm get winrm/config**.

El fragmento de código siguiente es un ejemplo basado en texto de una configuración de WinRM con la configuración de cuota predeterminada.

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

## <a name="configuring-shell-quotas"></a>Configuración de cuotas de shell

Las cuotas se pueden establecer a través de directiva de grupo configuración o manualmente. Para obtener más información sobre opciones de configuración específicas, vea [Instalación y configuración para Windows administración remota.](installation-and-configuration-for-windows-remote-management.md)

**Para establecer una cuota con directiva de grupo**

1.  Abra una ventana de símbolo del sistema como administrador.
2.  En el símbolo del sistema, escriba **gpedit.msc.** Se **abre Editor de objetos de directiva de grupo** ventana de configuración.
3.  Busque el **Windows remote management** and Windows Remote **Shell** directiva de grupo Objects (GPO) en Computer Configuration Plantillas administrativas Windows Components (Componentes de Plantillas administrativas **Windows \\ \\ equipo).**
4.  En la **pestaña Extendido,** seleccione una configuración para ver una descripción. Haga doble clic en una configuración para editarla.

**Para establecer una cuota manualmente**

1.  Abra una ventana de símbolo del sistema como administrador.
2.  En el símbolo del sistema, escriba **winrm set winrm/config/winrs '@{**_&lt; Quota &gt;_*_="_*_&lt; Value &gt;_*_"}"_*

Por ejemplo, para aumentar el número máximo de shells por usuario de 5 a 7, escriba **winrm set winrm/config/winrs '@{MaxShellsPerUser="7"}'.**

 

 




