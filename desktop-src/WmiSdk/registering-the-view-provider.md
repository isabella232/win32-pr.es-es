---
description: WMI registra automáticamente el archivo DLL del proveedor de vistas durante el proceso de instalación de WMI. Sin embargo, todavía es necesario registrar el proveedor de vistas con WMI para cada espacio de nombres que contendrá clases de vista.
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: Registrar el proveedor de vistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530a701d3ffc39523b1b3432dd2d94a3da256605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707274"
---
# <a name="registering-the-view-provider"></a>Registrar el proveedor de vistas

WMI registra automáticamente el archivo DLL del proveedor de vistas durante el proceso de instalación de WMI. Sin embargo, todavía es necesario registrar el proveedor de vistas con WMI para cada espacio de nombres que contendrá clases de vista.

En el procedimiento siguiente se describe cómo registrar el proveedor de vistas.

**Para registrar el proveedor de vistas**

1.  Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) para describir la implementación del proveedor de vistas.

    La instancia de [**\_ \_ Win32Provider**](--win32provider.md) describe el nombre del proveedor y su identificador de clase (CLSID), así como la configuración de seguridad predeterminada.

    En el ejemplo de código siguiente se describe una implementación de [**\_ \_ Win32Provider**](--win32provider.md).

    ``` syntax
    instance of __Win32Provider as $DataProv
    {
        Name = "MS_VIEW_INSTANCE_PROVIDER";
        ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
        ImpersonationLevel = 1;
        PerUserInitialization = "True";
        
    };
    ```

2.  Cree una instancia de la clase [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .

    En el ejemplo de código siguiente se muestra cómo crear una instancia de la clase **\_ \_ InstanceProviderRegistration** .

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $DataProv;
        SupportsPut = True;
        SupportsGet = True;
        SupportsDelete = True;
        SupportsEnumeration = True;
        QuerySupportLevels = {"WQL:UnarySelect"};
    };
    ```

3.  Cree una instancia de la clase [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) si desea tener los métodos de compatibilidad de la clase de vista Union.

    En el ejemplo de código siguiente se muestra cómo crear una instancia de la clase **\_ \_ MethodProviderRegistration** .

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  Compile el código MOF mediante el compilador MOF ([MOFCOMP](mofcomp.md)) o la interfaz [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

    Si guarda el ejemplo de código MOF enumerado anteriormente en un archivo denominado Viewtest. mof, use el comando MOFCOMP para cargar el código MOF en el espacio de nombres de destino. *NamespacePath* es el espacio de nombres en el que desea crear la instancia de la clase de vista.

    Escriba el siguiente comando en un símbolo del sistema para cargar el código MOF en el espacio de nombres de destino.

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).

Para obtener más información, vea [registrar un proveedor](registering-a-provider.md).

 

 



