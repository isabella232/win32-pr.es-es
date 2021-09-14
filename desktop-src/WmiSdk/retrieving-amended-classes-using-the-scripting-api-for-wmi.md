---
description: Si usa scripting API para WMI para recuperar o almacenar información de clase localizada, especifique la configuración regional como parte de un moniker.
ms.assetid: 3c64047d-ce3a-4180-8f71-0e66c2e61627
ms.tgt_platform: multiple
title: Recuperación de clases modificadas mediante la API de scripting para WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cef1971232eabdb984ad4321b5cadbdedd8b2be7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063919"
---
# <a name="retrieving-amended-classes-using-the-scripting-api-for-wmi"></a>Recuperación de clases modificadas mediante la API de scripting para WMI

Si usa scripting API para WMI para recuperar o almacenar información de clase localizada, especifique la configuración regional como parte de un moniker. O bien, puede proporcionar el nombre de la configuración regional en el parámetro *strLocale* al [**método SWbemLocator.ConnectServer.**](swbemlocator-connectserver.md) Al leer o escribir clases modificadas, indique que desea usar definiciones de clase localizadas [especificando wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) como marca para el parámetro *iFlags* del método al que se llama. Para PowerShell, puede usar el *parámetro -locale* en [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) para especificar la configuración regional.

En el ejemplo de código siguiente se muestra cómo recuperar una clase localizada mediante un moniker de scripting wmi o el parámetro -locale.


```VB
Set objwbemobject = GetObject("winmgmts:[locale=ms_409]!root/test:myclass")
```


```PowerShell

Get-WmiObject myclass -Namespace &quot;root\test&quot; -Locale &quot;ms_409&quot;
```





En el ejemplo de código siguiente se muestra cómo establecer el parámetro de configuración regional y usar la [marca wbemFlagUseAmendedQualifiers.](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)


```VB
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set service = Locator.ConnectServer(,"root\test", , , "ms_409")
Set objwbemobject = service.Get("myclass", wbemFlagUseAmendedQualifiers)
```



> [!Note]  
> Dado que es posible que la devolución de llamada al receptor no se devuelva en el mismo nivel de autenticación que requiere el cliente, se recomienda usar la comunicación semisincronosa en lugar de la comunicación asincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

 

En la tabla siguiente se enumeran los métodos que aceptan la [marca wbemFlagUseAmendedQualifiers.](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)



| Método sincrónico                                                 | Método asincrónico                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md)   | [**SWbemServices.SubclassesOfAsync**](swbemservices-subclassesofasync.md)   |
| [**SWbemObject.Subclasses\_**](swbemobject-subclasses-.md)        | [**SWbemObject.SubclassesAsync\_**](swbemobject-subclassesasync-.md)        |
| [**SWbemServices.InstancesOf**](swbemservices-instancesof.md)     | [**SWbemServices.InstancesOfAsync**](swbemservices-instancesofasync.md)     |
| [**SWbemObject.Instances\_**](swbemobject-instances-.md)          | [**SWbemObject.InstancesAsync\_**](swbemobject-instancesasync-.md)          |
| [**SWbemServices.ExecQuery**](swbemservices-execquery.md)         | [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)         |
| [**SWbemServices.Get**](swbemservices-get.md)                     | [**SWbemServices.GetAsync**](swbemservices-getasync.md)                     |
| [**SWbemObject.Put\_**](swbemobject-put-.md)                      | [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md)                      |
| [**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)   | [**SWbemServices.ReferencesToAsync**](swbemservices-referencestoasync.md)   |
| [**SWbemObject.References\_**](swbemobject-references-.md)        | [**SWbemObject.ReferencesAsync\_**](swbemobject-referencesasync-.md)        |
| [**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md) | [**SWbemServices.AssociatorsOfAsync**](swbemservices-associatorsofasync.md) |
| [**SWbemObject.Associators\_**](swbemobject-associators-.md)      | [**SWbemObject.AssociatorsAsync\_**](swbemobject-associatorsasync-.md)      |



 

 

 
