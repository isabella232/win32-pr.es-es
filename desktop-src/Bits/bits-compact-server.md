---
title: BITS Compact Server
description: El Servicio de transferencia inteligente en segundo plano compact server (BITS) es un servidor de archivos HTTP/HTTPS independiente que proporciona la capacidad de transferir un número limitado de archivos grandes de forma asincrónica entre equipos.
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40e2840c24e15379fac11a5a12ed76c225e7be5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974256"
---
# <a name="bits-compact-server"></a>BITS Compact Server

El Servicio de transferencia inteligente en segundo plano compact server (BITS) es un servidor de archivos HTTP/HTTPS independiente que proporciona la capacidad de transferir un número limitado de archivos grandes de forma asincrónica entre equipos. Compact Server se ha creado como un servicio NT y usa HTTP.SYS.

BITS Compact Server está pensado para su uso por parte de clientes empresariales y de pequeñas empresas en las siguientes condiciones:

-   El uso previsto es un máximo de 25 grupos de direcciones URL y cada grupo de direcciones URL admite 3 transferencias de archivos simultáneas.
-   Las transferencias de archivos se producen entre equipos del mismo dominio o dominios de confianza mutua.
-   Las transferencias de archivos no están pensadas para clientes con conexión a Internet.

## <a name="installing-the-bits-compact-server"></a>Instalación de BITS Compact Server

BITS Compact Server es un componente de servidor opcional. Puede usar una de las siguientes opciones para instalar BITS Compact Server:

-   Administrador de servidores

-   Windows PowerShell

-   Administrador de paquetes

**Para instalar BITS Compact Server mediante Administrador del servidor**

1.  En la **sección Resumen de características** de la **Administrador del servidor**, haga clic en **Agregar características.**
2.  En el Asistente para agregar características, **seleccione Servicio de transferencia inteligente en segundo plano (BITS)** y **Compact Server**.
3.  Siga las instrucciones del asistente, incluida la instalación del software necesario si se indica.

Para obtener más información, consulte el **Administrador del servidor** en línea.

**Para instalar BITS Compact Server mediante Windows PowerShell**

1.  En un Windows PowerShell de comandos, escriba el siguiente comando: **Import-Module ServerManager**. Luego, presione Intro.
2.  Escriba el comando siguiente: **Add-WindowsFeature BITS-Compact-Server**. Luego, presione Intro.

En el siguiente ejemplo basado en texto se muestra cómo instalar BITS Compact Server mediante Windows PowerShell cmdlets.

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

Para obtener información sobre el uso de cmdlets, [consulte Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) documentación.

Para obtener más información sobre el cmdlet Import-Module, [vea Import-Module](/previous-versions//dd347701(v=technet.10)) en la biblioteca de Microsoft TechNet. Para obtener ayuda en la línea de comandos, **escriba get-help import-module**.

Para obtener más información sobre el cmdlet Add-WindowsFeature, [vea Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) en la biblioteca de Microsoft TechNet. Para obtener ayuda en la línea de comandos, **escriba get-help Add-WindowsFeature**.

**Para instalar BITS Compact Server mediante Administrador de paquetes**

-   Escriba el siguiente comando: **PkgMgr.exe /iu:LightweightServer**.

> [!Note]  
> La configuración se pierde si se reinicia el servicio Compact Server o si se reinicia el equipo.

 

## <a name="bits-compact-server-remote-management"></a>Administración remota del servidor de BITS Compact

Bits Compact Server con administración remota de BITS permite transferencias de archivos remotas más seguras. La administración remota de BITS usa un proveedor de instrumental de administración de Windows (WMI) para permitir que un administrador del sistema o una aplicación de controlador cree de forma remota trabajos de transferencia de BITS en los clientes y para publicar archivos para hospedar en el servidor de BITS Compact. El proveedor de BITS también se puede usar para permitir que una aplicación use de forma remota el cliente bits junto con bits Compact Server para transferir archivos de un equipo remoto a otro equipo remoto.

Para más información, consulte la documentación [del proveedor de BITS.](/previous-versions/windows/desktop/bitsprov/bits-provider)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedor de BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 