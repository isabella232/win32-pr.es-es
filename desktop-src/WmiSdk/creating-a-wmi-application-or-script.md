---
description: Cualquier lenguaje de scripting, como VBScript, que funcione con objetos ActiveX podrá tener acceso a los datos de WMI. Las aplicaciones pueden tener acceso a WMI en C++, mediante la API COM para WMI o en Visual Basic, mediante la biblioteca de tipos Wbemdisp. tlb y la API de scripting para WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Crear una aplicación o un script WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27e3cffd7e4d9bea4ce36e7c0da77ae5d72cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707097"
---
# <a name="creating-a-wmi-application-or-script"></a>Crear una aplicación o un script WMI

Cualquier lenguaje de scripting, como VBScript, que funcione con objetos ActiveX podrá tener acceso a los datos de WMI. Las aplicaciones pueden tener acceso a WMI en C++, mediante la [API com para WMI](com-api-for-wmi.md) o en Visual Basic, mediante la [biblioteca de tipos](using-the-wmi-scripting-type-library.md) Wbemdisp. tlb y la [API de scripting para WMI](scripting-api-for-wmi.md). . Puede obtener datos a través de WMI escribiendo un script, una Active Server página (ASP) o una aplicación HTML (HTA). También puede usar Windows PowerShell para obtener datos o escribir scripts. Para obtener más información, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) y [Introducción con Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true). TechNet ScriptCenter en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contiene cientos de ejemplos de scripting. Para obtener más información sobre los recursos de impresión y en línea, vea [más información](further-information.md).

En el procedimiento siguiente se describe cómo conectarse al servicio WMI y al almacén de datos.

**Para conectarse al servicio WMI y al almacén de datos**

1.  Busque el servicio WMI en un equipo específico.
2.  Conéctese a uno o varios espacios de nombres de WMI.

Estas operaciones son diferentes en C++, Visual Basic, .NET Framework lenguajes o cuando se usa un script. Los scripts y las aplicaciones Visual Basic deben tener acceso a las clases cuyas instancias se proporcionan con los datos de los proveedores existentes. Sin embargo, las aplicaciones escritas en C++ pueden hacer más. Por ejemplo, una aplicación escrita en C++ puede enviar eventos, pero un script de WMI solo puede suscribirse para recibir eventos.

Un proveedor WMI solo se puede escribir en C++ o mediante el .NET Framework. Para obtener más información sobre cómo escribir aplicaciones en C# o Visual Basic .NET, consulte [información general sobre WMI .net](/previous-versions/bb404655(v=vs.90)).

Para obtener más información acerca de la creación de aplicaciones y scripts para WMI, vea:

-   [Crear una aplicación WMI con C++](creating-a-wmi-application-using-c-.md)
-   [Creación de un script de WMI](creating-a-wmi-script.md)
-   [Crear un cliente WMI administrado](creating-a-managed-wmi-client.md)

Para realizar la mayoría de las tareas, utilice las [clases WMI](wmi-classes.md)preinstaladas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar WMI](using-wmi.md)
</dt> </dl>

 

 
