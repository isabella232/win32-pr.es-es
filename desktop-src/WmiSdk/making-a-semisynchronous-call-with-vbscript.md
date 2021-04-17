---
description: Proporciona la funcionalidad de acceso semisincrónico y un ejemplo de código para crear una llamada de método semisincrónico.
ms.assetid: 3eae38e8-6a63-45c0-99b0-94e25ddbc5a8
ms.tgt_platform: multiple
title: Realización de una llamada semisincrónica con VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e875a269d2cf1cd4e3b40d5c84d42ffb97dc35a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697417"
---
# <a name="making-a-semisynchronous-call-with-vbscript"></a>Realización de una llamada semisincrónica con VBScript

Algunos métodos WMI pueden devolver colecciones grandes, lo que hace que los scripts dejen de responder. En el script, el acceso semisincrónico es el valor predeterminado y Instrumental de administración de Windows (WMI) establece **wbemFlagReturnImmediately** para llamadas que pueden devolver colecciones de objetos grandes como los siguientes métodos [**SWbemServices**](swbemservices.md) : [**instances**](swbemservices-instancesof.md), [**subclasses**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**AssociatorsOf**](swbemservices-associatorsof.md)y [**referenceto**](swbemservices-referencesto.md).

El acceso semisincrónico que usa **wbemFlagReturnImmediately** establecido en el *parámetro IFlags* también es el valor predeterminado para las llamadas que pueden devolver conjuntos de objetos grandes para los siguientes métodos de [**SWbemObject**](swbemobject.md) : [**\_ instancias**](swbemobject-instances-.md), [**subclases \_**](swbemobject-subclasses-.md), [**asociadores \_**](swbemobject-associators-.md)y [**referencias \_**](swbemobject-references-.md).

Para reducir el uso de recursos de memoria de WMI al procesar una gran colección de objetos, incluya el valor de **wbemFlagForwardOnly** en el parámetro *IFlags* . El uso de **wbemFlagForwardOnly** hace que WMI cree un enumerador de solo avance que no permite rebobinar la colección y obtener acceso a los elementos de nuevo.

WMI elimina la memoria de cada objeto, ya que la instrucción **for each** procesa un objeto. No se puede llamar al método **Count** para una colección cuando se estableció la marca **wbemFlagForwardOnly** en la llamada que obtuvo la colección. Tenga en cuenta que el parámetro *IFlags* tiene **wbemFlagReturnImmediately** y **wbemFlagForwardOnly** establecido de forma predeterminada para el método [**cNotificationQuerySWbemServices.Exe**](swbemservices-execnotificationquery.md) .

En el procedimiento siguiente se describe cómo usar VBScript para crear una llamada semisincrónica.

**Para hacer una llamada semisincrónica en VBScript**

1.  Establezca el parámetro *IFlags* en el valor de [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).
2.  Realice la llamada sincrónica normal para [**SWbemServices.ExecQuery**](swbemservices-execquery.md) o [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) con el valor *iFlags* .
3.  Si desea tratar los objetos devueltos por la llamada como una colección, use una sintaxis de enumeración como VBScript **para cada uno**. A medida que se devuelve cada objeto, se procesa como el elemento siguiente de la colección.
4.  Cree un enumerador de solo avance combinando el valor de **wbemFlagReturnImmediately** con el valor de **wbemFlagForwardOnly**. El valor decimal de esta operación OR es 48. Estas constantes se definen en la biblioteca de tipos wbemdisp. tlb para Visual Basic. La mayoría de los lenguajes de scripting usan el valor numérico o definen una constante. Para obtener más información, vea [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).

En el ejemplo de código siguiente se muestra cómo hacer una llamada de método semisincrónico. Para obtener más información, consulte [llamar a un método](calling-a-method.md).


```VB
wbemFlagReturnImmediately = 16
wbemFlagForwardOnly = 32
IFlags = wbemFlagReturnImmediately + wbemFlagForwardOnly
WScript.Echo IFlags
Set objWMIService = GetObject("winmgmts:root\cimv2")
' Query for all the Win32_Process objects on the 
'     local computer and use forward-only enumerator
Set colProcesses = objWMIService.ExecQuery("SELECT Name FROM Win32_Process",,IFlags)
' Receive each object as it arrives
For Each objProcess in colProcesses
    WScript.Echo objProcess.Name
Next
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 

 



