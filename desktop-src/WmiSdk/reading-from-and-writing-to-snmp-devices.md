---
description: Se puede acceder a los dispositivos SNMP leyendo o escribiendo en su instancia de clase correspondiente en el SMIR de WMI (repositorio de información del módulo SNMP).
ms.assetid: af5e1321-b552-447e-a217-eecbebe1f203
ms.tgt_platform: multiple
title: Lectura y escritura en dispositivos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c0419a5fc426c183ee1eb89a957a0c2f6a210ecd9b5d4612b6c4deb4e0f775a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554261"
---
# <a name="reading-from-and-writing-to-snmp-devices"></a>Lectura y escritura en dispositivos SNMP

Se puede acceder a los dispositivos SNMP leyendo o escribiendo en su instancia de clase correspondiente en el SMIR de WMI (repositorio de información del módulo SNMP). Cuando trabaje con varios dispositivos del mismo tipo, para mejorar la eficacia, cargue los MIB para un tipo de dispositivo SNMP en el SÚL.

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configuración del entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 

Seleccione una de las siguientes opciones para leer o escribir en cada tipo de dispositivo SNMP actualizando la información de contexto de la instancia antes de comunicarse con cada uno de ellos.

-   Use un nombre DNS en lugar de la dirección IP al hacer referencia a un dispositivo específico.

    En el ejemplo siguiente se muestra cómo usar el nombre DNS para un dispositivo específico.

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   Cree un espacio de nombres independiente y asocie una dirección de dispositivo al objeto de espacio de nombres mediante el calificador de instancia AgentAddress para que el espacio de nombres esté enlazado permanentemente al dispositivo. En este caso, no es necesario especificar la información del objeto de contexto.
-   Lectura desde un dispositivo SNMP.

    En el ejemplo siguiente se realiza una operación Get en una clase de dispositivo.

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set objSet = objServices.ExecQuery _
        ("SELECT * FROM SNMP_NET_DEVICE_123 WHERE hdwr_idx>1",, _
          wbemFlagReturnWhenComplete)
    for each obj in objset 
      'do whatever 
    next
    ```

    

-   Escribir en un dispositivo SNMP.

    En el ejemplo siguiente se realiza una operación Set en una clase de dispositivo.

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

Las clases correlacionadas son aquellas que se sabe que un dispositivo SNMP determinado admite cuando se produce la enumeración. La correlación afecta al conjunto de clases devueltas desde SMIR. La enumeración no relacionada devuelve todas las clases presentes en el SMIR, independientemente de si el dispositivo las admite. Para obtener más información sobre el uso de técnicas de correlación wmi, vea [Wmi SNMP Class Correlation](wmi-snmp-class-correlation.md).

 

 



