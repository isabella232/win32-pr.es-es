---
description: Cualquier lenguaje de scripting, como VBScript, que funcione con objetos ActiveX pueden acceder a datos WMI. Las aplicaciones pueden acceder a WMI en C++, mediante la API COM para WMI o en Visual Basic, mediante la biblioteca de tipos Wbemdisp.tlb y scripting API para WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Crear una aplicación WMI o un script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27e3cffd7e4d9bea4ce36e7c0da77ae5d72cdb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359100"
---
# <a name="creating-a-wmi-application-or-script"></a>Crear una aplicación WMI o un script

Cualquier lenguaje de scripting, como VBScript, que funcione con objetos ActiveX pueden acceder a datos WMI. Las aplicaciones pueden acceder a WMI en C++, mediante la [API COM](com-api-for-wmi.md) para WMI o en Visual Basic, mediante la biblioteca de tipos Wbemdisp.tlb y scripting API para [WMI.](scripting-api-for-wmi.md) [](using-the-wmi-scripting-type-library.md) . Puede obtener datos a través de WMI escribiendo un script, una página de Active Server (ASP) o una aplicación HTML (HTA). También puede usar Windows PowerShell para obtener datos o escribir scripts. Para obtener más información, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) and Tareas iniciales with [Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true). ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contiene cientos de ejemplos de scripting. Para obtener más información sobre los recursos de impresión y en línea, vea [Más información.](further-information.md)

En el procedimiento siguiente se describe cómo conectarse al servicio WMI y al almacén de datos.

**Para conectarse al servicio WMI y al almacén de datos**

1.  Busque el servicio WMI en un equipo específico.
2.  Conectar a uno o varios espacios de nombres WMI.

Estas operaciones son diferentes en C++, Visual Basic, .NET Framework lenguajes o cuando se usa un script. Los scripts Visual Basic aplicaciones deben tener acceso a clases cuyas instancias se suministran con datos de proveedores existentes. Pero las aplicaciones escritas en C++ pueden hacer más. Por ejemplo, una aplicación escrita en C++ puede enviar eventos, pero un script WMI solo puede suscribirse para recibir eventos.

Un proveedor WMI solo se puede escribir en C++ o mediante el .NET Framework. Para obtener más información sobre cómo escribir aplicaciones en C# o Visual Basic .NET, vea [Información general de WMI para .NET.](/previous-versions/bb404655(v=vs.90))

Para obtener más información sobre cómo crear aplicaciones y scripts para WMI, vea:

-   [Creación de una aplicación WMI mediante C++](creating-a-wmi-application-using-c-.md)
-   [Crear un script WMI](creating-a-wmi-script.md)
-   [Creación de un cliente WMI administrado](creating-a-managed-wmi-client.md)

Para realizar la mayoría de las tareas, use las clases [WMI preinstaladas](wmi-classes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de WMI](using-wmi.md)
</dt> </dl>

 

 
