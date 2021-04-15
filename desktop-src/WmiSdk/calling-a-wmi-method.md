---
title: Cómo llamar a un método WMI
description: El propósito principal de WMI es proporcionar acceso a las clases e instancias que representan los objetos de la red.
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892561785280e78ecf29da1030883994990fc822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546099"
---
# <a name="how-to-call-a-wmi-method"></a>Cómo llamar a un método WMI

El propósito principal de WMI es proporcionar acceso a las clases e instancias que representan los objetos de la red. Los proveedores admiten estas clases e instancias. Por ejemplo, todas las instancias de que representan dispositivos de hardware estándar en su empresa, como [**Win32 \_ PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) o [**la \_ impresora Win32**](/windows/desktop/CIMWin32Prov/win32-printer), son compatibles con el proveedor de Win32. Del mismo modo, puede tener acceso al registro de eventos a través del proveedor de registro de eventos y el registro a través del proveedor del registro.

Los métodos que WMI implementa en interfaces como [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) o objetos de scripting, como [**SWbemServices**](swbemservices.md), son principalmente para obtener y manipular de forma genérica los datos suministrados por cualquier proveedor. Por ejemplo, use [**SWbemServices. instances**](swbemservices-instancesof.md) para obtener todas las instancias [**del \_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) en un subconjunto de equipos empresariales. Después, puede llamar al método de proveedor de Win32 [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) en cada objeto de **\_ proceso de Win32** .

En el ejemplo siguiente, se llama al método [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) como método de automatización en el objeto de proceso. También se podría llamar a un método WMI, como el método [**\_ path**](swbemobject-path-.md) definido para [**SWbemObject**](swbemobject.md) en el objeto **Process** .


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



El proceso real de usar los métodos de WMI es idéntico al uso de cualquier otra interfaz de automatización o COM de Windows. Para obtener más información, consulte [com](../cossdk/component-services-portal.md) y [crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md). Para obtener más información acerca de las interfaces que admite WMI, vea [API de com para WMI](com-api-for-wmi.md) y [API de scripting para WMI](scripting-api-for-wmi.md).

Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 

 
