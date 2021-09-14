---
title: Cómo llamar a un método WMI
description: El propósito principal de WMI es proporcionar acceso a clases e instancias que representan objetos en la red.
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892561785280e78ecf29da1030883994990fc822
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358933"
---
# <a name="how-to-call-a-wmi-method"></a>Cómo llamar a un método WMI

El propósito principal de WMI es proporcionar acceso a clases e instancias que representan objetos en la red. Estos proveedores admiten estas clases e instancias. Por ejemplo, todas las instancias que representan dispositivos de hardware estándar en su empresa, como [**Win32 \_ PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) o [**Impresora Win32, \_**](/windows/desktop/CIMWin32Prov/win32-printer)son compatibles con el proveedor win32. De forma similar, puede acceder al registro de eventos a través del proveedor de registro de eventos y del registro a través del proveedor del Registro.

Los métodos que WMI implementa en interfaces como [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) u objetos de scripting como [**SWbemServices**](swbemservices.md), son principalmente para obtener y manipular genéricamente los datos proporcionados por cualquier proveedor. Por ejemplo, use [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) para obtener todas las instancias de [**Proceso win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) en un subconjunto de equipos empresariales. A continuación, puede llamar al método de proveedor [**Win32 GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) en cada **objeto Process \_ de Win32.**

En el ejemplo siguiente, se [**llama al método GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) como método de automatización en el objeto Process. También se puede llamar a un método WMI, como [**el método Path \_**](swbemobject-path-.md) definido para [**SWbemObject**](swbemobject.md) en el **objeto Process.**


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



El proceso real de usar los métodos WMI es idéntico al uso de cualquier otro Windows com o la interfaz de automatización. Para obtener más información, [vea COM](../cossdk/component-services-portal.md) y Crear una aplicación WMI [o script](creating-a-wmi-application-or-script.md). Para obtener más información sobre las interfaces compatibles con WMI, vea [API COM para WMI](com-api-for-wmi.md) y Scripting API para [WMI.](scripting-api-for-wmi.md)

Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 

 
