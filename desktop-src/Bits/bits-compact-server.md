---
title: Servidor BITS compacto
description: El servidor de Servicio de transferencia inteligente en segundo plano (BITS) Compact es un servidor de archivos HTTP/HTTPS independiente que proporciona la capacidad de transferir un número limitado de archivos grandes de forma asincrónica entre equipos.
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40e2840c24e15379fac11a5a12ed76c225e7be5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904720"
---
# <a name="bits-compact-server"></a>Servidor BITS compacto

El servidor de Servicio de transferencia inteligente en segundo plano (BITS) Compact es un servidor de archivos HTTP/HTTPS independiente que proporciona la capacidad de transferir un número limitado de archivos grandes de forma asincrónica entre equipos. El servidor compacto se compila como un servicio NT y usa HTTP.SYS.

El servidor BITS compacto está diseñado para que lo usen los clientes de empresas y pequeñas empresas en las siguientes condiciones:

-   El uso previsto es un máximo de 25 grupos de direcciones URL, y cada grupo de direcciones URL admite 3 transferencias de archivos simultáneas.
-   Las transferencias de archivos se producen entre equipos en el mismo dominio o en dominios de confianza mutua.
-   Las transferencias de archivos no están destinadas a clientes con conexión a Internet.

## <a name="installing-the-bits-compact-server"></a>Instalación del servidor BITS compacto

El servidor BITS Compact es un componente de servidor opcional. Puede usar una de las siguientes opciones para instalar el servidor BITS compacto:

-   Administrador de servidores

-   Windows PowerShell

-   Administrador de paquetes

**Para instalar el servidor BITS compacto mediante Administrador del servidor**

1.  En la sección **Resumen de características** del **Administrador del servidor**, haga clic en **Agregar características**.
2.  En el Asistente para agregar características, seleccione **servicio de transferencia inteligente en segundo plano (bits)** y **Compact Server**.
3.  Siga las instrucciones del asistente, incluida la instalación del software necesario, si se indica.

Para obtener más información, consulte la ayuda en pantalla de **Administrador del servidor** .

**Para instalar el servidor BITS compacto mediante Windows PowerShell**

1.  En un símbolo del sistema de Windows PowerShell, escriba el siguiente comando: **Import-Module ServerManager**. Luego, presione Intro.
2.  Escriba el comando siguiente: **Add-WINDOWSFEATURE bits-Compact-Server**. Luego, presione Intro.

En el ejemplo de texto siguiente se muestra cómo instalar el servidor BITS compacto mediante cmdlets de Windows PowerShell.

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

Para obtener información sobre el uso de cmdlets, consulte la documentación de [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .

Para obtener más información sobre el cmdlet Import-Module, consulte [Import-Module](/previous-versions//dd347701(v=technet.10)) en la biblioteca de Microsoft TechNet. Para obtener ayuda en la línea de comandos, escriba **Get-Help Import-Module**.

Para obtener más información sobre el cmdlet Add-WindowsFeature, consulte [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) en la biblioteca de Microsoft TechNet. Para obtener ayuda en la línea de comandos, escriba **Get-Help Add-WindowsFeature**.

**Para instalar el servidor BITS compacto mediante el administrador de paquetes**

-   Escriba el siguiente comando: **PkgMgr.exe/IU: LightweightServer**.

> [!Note]  
> La configuración se pierde si se reinicia el servicio del servidor compacto o si se reinicia el equipo.

 

## <a name="bits-compact-server-remote-management"></a>Administración remota del servidor BITS compacto

El servidor BITS compacto con administración remota de BITS permite realizar transferencias de archivos remotas más seguras. La administración remota de BITS usa un proveedor de Instrumental de administración de Windows (WMI) para permitir que un administrador del sistema o una aplicación de controlador cree de forma remota trabajos de transferencia de BITS en los clientes y publique archivos para hospedarlos en el servidor BITS compacto. El proveedor de BITS también se puede usar para permitir que una aplicación use de forma remota el cliente de BITS junto con el servidor BITS compacto para transferir archivos de un equipo remoto a otro equipo remoto.

Para obtener más información, vea la documentación del [proveedor de bits](/previous-versions/windows/desktop/bitsprov/bits-provider) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedor BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 