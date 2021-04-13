---
description: Se puede tener acceso a los dispositivos SNMP mediante la lectura o la escritura en su instancia de clase correspondiente en el SMIR de WMI (repositorio de información del módulo SNMP).
ms.assetid: af5e1321-b552-447e-a217-eecbebe1f203
ms.tgt_platform: multiple
title: Leer y escribir en dispositivos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc25f384d499e16e19c5e909f7d091ea34f9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544830"
---
# <a name="reading-from-and-writing-to-snmp-devices"></a>Leer y escribir en dispositivos SNMP

Se puede tener acceso a los dispositivos SNMP mediante la lectura o la escritura en su instancia de clase correspondiente en el SMIR de WMI (repositorio de información del módulo SNMP). Cuando trabaje con varios dispositivos del mismo tipo, para mayor eficacia, cargue las MIB para un tipo de dispositivo SNMP en el SMIR.

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Seleccione una de las siguientes opciones para leer o escribir en cada tipo de dispositivo SNMP actualizando la información de contexto de la instancia antes de comunicarse con cada una de ellas.

-   Use un nombre DNS en lugar de la dirección IP al hacer referencia a un dispositivo específico.

    En el ejemplo siguiente se muestra cómo usar el nombre DNS para un dispositivo específico.

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   Cree un espacio de nombres independiente y asocie una dirección de dispositivo al objeto de espacio de nombres mediante el calificador de instancia de AgentAddress para que el espacio de nombres esté enlazado permanentemente al dispositivo. En este caso, no es necesario especificar la información del objeto de contexto.
-   Leer desde un dispositivo SNMP.

    En el ejemplo siguiente se realiza una operación get en una clase de dispositivo.

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

    En el siguiente ejemplo se realiza una operación SET en una clase Device.

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

Las clases correlacionadas son aquellas a las que se sabe que un determinado dispositivo SNMP es compatible cuando se produce la enumeración. La correlación afecta al conjunto de clases devueltas desde SMIR. La enumeración no correlacionada devuelve todas las clases presentes en el SMIR, independientemente de si el dispositivo las admite. Para obtener más información sobre el uso de técnicas de correlación de WMI, vea [correlación de clases SNMP de WMI](wmi-snmp-class-correlation.md).

 

 



