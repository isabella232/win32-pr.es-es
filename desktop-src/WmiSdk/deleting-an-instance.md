---
description: La eliminación de una instancia es el comando de eliminación más común que es probable que se realice en WMI.
ms.assetid: 95ba3e9c-1397-41fe-a080-c03a98aafd42
ms.tgt_platform: multiple
title: Eliminar una instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2229889ec4bc21ad234eb1636f264977bb3e25e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706167"
---
# <a name="deleting-an-instance"></a>Eliminar una instancia

La eliminación de una instancia es el comando de eliminación más común que es probable que se realice en WMI. Al igual que cuando se elimina una clase, el comando real es bastante sencillo. Sin embargo, WMI funciona de forma bastante diferente según el tipo de instancia que se va a eliminar. Si la instancia es estática, WMI simplemente elimina la instancia del repositorio WMI. Para obtener información acerca de cómo quitar clases e instancias del repositorio WMI, vea el comando de preprocesador [**pragma deleteclass**](pragma-deleteclass.md) .

Si la instancia es dinámica, WMI debe llamar a [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) en los proveedores responsables de las siguientes clases:

-   Clase a la que pertenece la instancia.
-   Cada clase primaria de la clase a la que pertenece la instancia.
-   Cada subclase de la clase a la que pertenece la instancia.

El éxito de la eliminación depende de la clase no abstracta de nivel superior para la instancia original. Si el proveedor de cualquier clase no abstracta de nivel superior consigue completar la eliminación, la operación se realiza correctamente. Para obtener más información, vea la sección Comentarios de [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).

La [API de com para WMI](com-api-for-wmi.md) tiene distintos métodos para eliminar una instancia y eliminar un objeto.

En el procedimiento siguiente se describe cómo usar C++ para eliminar una instancia de una clase base o una clase derivada.

**Para eliminar una instancia de una clase base o una clase derivada mediante C++**

-   Llame a los métodos [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) o [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) .

    Como sugiere el nombre, [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) elimina una instancia de forma asincrónica mientras que [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) elimina una instancia sincrónicamente. Para usar **DeleteInstanceAsync**, también debe implementar un objeto [**IWbemObjectSink**](iwbemobjectsink.md) .

> [!Note]  
> Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

 

La [API de scripting para WMI](scripting-api-for-wmi.md) usa los mismos métodos para eliminar un objeto de clase o una instancia de.

En el procedimiento siguiente se describe cómo usar VBScript para eliminar una instancia de una clase base o una clase derivada.

**Para eliminar una instancia de una clase base o una clase derivada mediante VBScript**

-   Llame a los métodos [**SWbemObject. \_ Delete**](swbemobject-delete-.md) o [**SWbemObject. \_ DeleteAsync**](swbemobject-deleteasync-.md) .

    Como sugiere el nombre, [**Delete \_**](swbemobject-delete-.md) elimina una instancia sincrónicamente, mientras que [**DeleteAsync \_**](swbemobject-deleteasync-.md) elimina una instancia de forma asincrónica. Para obtener más información sobre cómo eliminar una instancia de forma asincrónica, vea [llamar a un método](calling-a-method.md).

    En el ejemplo siguiente se describe cómo eliminar una instancia de mediante VBScript.

    ```VB
    Dim service

    Set service = GetObject("winmgmts:{impersonationLevel=impersonate}") 

    Set objwbemobject= service.get("")

    objwbemobject.Path_.Class = "MyNewClass" 
    objwbemobject.put_
    service.delete  "MyNewClass"
    ```

    

> [!Note]  
> Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

 

 

 



