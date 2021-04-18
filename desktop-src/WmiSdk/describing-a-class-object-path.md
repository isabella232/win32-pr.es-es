---
description: Una ruta de acceso de objeto de clase describe la ubicación de una clase dentro de un espacio de nombres.
ms.assetid: 5ae95707-d023-4102-9b41-140c54b0c5b7
ms.tgt_platform: multiple
title: Describir una ruta de acceso de objeto de clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1cfd603ea3b6de151d297a7f4b6fc8a2a27dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706814"
---
# <a name="describing-a-class-object-path"></a>Describir una ruta de acceso de objeto de clase

Una ruta de acceso de objeto de clase describe la ubicación de una clase dentro de un espacio de nombres.

Puede usar los métodos siguientes para especificar una ruta de acceso de objeto:

-   Una ruta de acceso de objeto completa a una clase anexa el nombre de la clase a una ruta de acceso del espacio de nombres.

    En el ejemplo siguiente se muestra la ubicación de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en el \\ espacio de \\ nombres root Cimv2 en el servidor denominado admin.

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   Una ruta de acceso relativa al objeto representa una clase que reside en el espacio de nombres actual. Una ruta de acceso relativa a un objeto para una clase contiene solo el nombre de clase.

    En el ejemplo siguiente se muestra la ruta de acceso relativa a la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

    ``` syntax
    Win32_LogicalDisk
    ```

Cuando se consulta un nombre de clase pero no se especifica ninguna instancia, WMI devuelve la definición de clase. En el procedimiento siguiente se describe cómo recuperar una definición de clase en VBScript.

**Para recuperar una definición de clase en VBScript**

-   Puede usar la conexión de moniker con una consulta o [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx). También puede usar [**SWbemServices. Get**](swbemservices-get.md).

    En el ejemplo siguiente se muestra cómo usar [GetObject](/previous-versions//kdccchxa(v=vs.85)) para obtener una definición de clase.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
       & "{impersonationLevel=impersonate}!\\" _
       & strComputer & "\root\cimv2:Win32_Printer")
    ```

    

    En el ejemplo siguiente se muestra cómo consultar una definición de clase.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
        & "{impersonationLevel=impersonate}!\\" _
        & strComputer & "\root\cimv2")
    Set colInstalledPrinters =  objWMIService.ExecQuery _
        ("Select * from Win32_Printer")
    ```

    

Puede recuperar una definición de clase en C++ especificando solo el nombre de clase y sin ruta de acceso a una instancia determinada. En el procedimiento siguiente se describe cómo recuperar una definición de clase en C++.

**Para recuperar una definición de clase en C++**

-   Realice una llamada a las funciones [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .

    En el ejemplo siguiente se muestra cómo llamar a la función [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    En el ejemplo de código anterior se requiere que la siguiente \# instrucción include se compile correctamente.

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
