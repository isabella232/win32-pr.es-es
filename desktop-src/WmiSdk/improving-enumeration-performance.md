---
description: Las enumeraciones tienden a usar una cantidad significativa de recursos del sistema.
ms.assetid: 4163e6c2-4ee3-4906-b297-618509666c90
ms.tgt_platform: multiple
title: Mejorar el rendimiento de la enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2554e9e1df2f2ece58f5703d6099d84acbe01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277929"
---
# <a name="improving-enumeration-performance"></a>Mejorar el rendimiento de la enumeración

Las enumeraciones tienden a usar una cantidad significativa de recursos del sistema. Por lo tanto, debe intentar optimizar el proceso de enumeración de WMI si planea realizar enumeraciones en un grupo de gran tamaño. Los scripts también pueden usar una consulta para evitar la degradación del rendimiento en las operaciones "for each.... Next" con un conjunto grande. Para obtener más información, consulte [consultar WMI](querying-wmi.md).

En el procedimiento siguiente se describe cómo mejorar el rendimiento de la enumeración.

**Para mejorar el rendimiento de la enumeración**

1.  Establezca el parámetro *lFlags* para permitir la devolución semisincrónica de los datos con un enumerador que descarte cada elemento de WMI cuando se entregue. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

    En el ejemplo de código de C++ siguiente se muestra cómo utilizar la **marca de WBEM devolver las marcas \_ \_ \_ inmediato** y de **WBEM marca de \_ \_ \_ solo avance** .

    `WBEM_FLAG_RETURN_IMMEDIATE | WBEM_FLAG_FORWARD_ONLY`

    En VBScript o Visual Basic, use las marcas de scripting **WbemFlagReturnImmediately** y **WbemFlagForwardOnly** de [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum). El valor combinado de estas marcas es decimal 48.

    Las marcas de scripting y de parámetros producen el siguiente comportamiento:

    -   La **\_ marca WBEM \_ devuelve \_** el comportamiento semisincrónico de las solicitudes de marca **wbemFlagReturnImmediately** o inmediata. La llamada para crear el enumerador se devuelve inmediatamente. A continuación, puede empezar a recorrer el conjunto de objetos que recibe.
    -   La marca **WBEM \_ marca de \_ \_ solo avance** o la marca **wbemFlagForwardOnly** solicita un enumerador que no se puede rebobinar. Es decir, WMI puede liberar un objeto después de ver el objeto.

    En situaciones en las que la enumeración es grande y la aplicación es muy rápida, el uso de enumeradores de solo avance con procesamiento semisincrónico permite a WMI conservar muchos menos objetos, lo que aumenta significativamente el tiempo de respuesta y el rendimiento de la memoria.

    En el ejemplo de código de VBScript siguiente se muestra cómo hacer una llamada mediante las marcas combinadas **wbemFlagReturnImmediately** y **wbemFlagForwardOnly** para obtener una colección de eventos de un registro de eventos.

    ```VB
    Set Events = GetObject("winmgmts:").ExecQuery _
         ("SELECT * FROM Win32_NTLogEvent " _
          & "WHERE Logfile = 'System'",,48)
    ```

    

2.  Siempre que sea posible, evite usar [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) en C++ o [**SWbemServices. instances**](swbemservices-instancesof.md)y, en su lugar, use **ExecQuery**.

    El método **ExecQuery** consulta a WMI mediante tecnologías de base de datos, mientras que [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) o [**SWbemServices. instances**](swbemservices-instancesof.md) enumera los objetos WMI. En concreto, **ExecQuery** puede solicitar subconjuntos específicos de datos que los métodos de enumeración no pueden.

    Dado que algunos proveedores no tienen capacidades de consulta, WMI proporciona una característica de "filtro posterior" que permite a WMI descartar las instancias que no cumplen las especificaciones de una consulta. Si un determinado proveedor aprovecha esta característica, es el autor del proveedor.

3.  Experimente con diferentes consultas para determinar lo que le da el mejor rendimiento.

    Por ejemplo, WMI raramente procesa las consultas con las cláusulas **Where** con el formato Prop1 < "x". Por el contrario, WMI normalmente procesa las consultas con el formato KeyProp1 = "x" de manera eficaz.

Para obtener más información, consulte [enumeración de WMI](enumerating-wmi.md).

 

 



