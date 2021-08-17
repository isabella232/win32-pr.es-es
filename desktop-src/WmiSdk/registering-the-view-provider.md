---
description: WMI registra automáticamente el archivo DLL del proveedor de vistas durante el proceso de instalación de WMI. Sin embargo, todavía debe registrar el proveedor de vistas con WMI para cada espacio de nombres que contendrá clases de vista.
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: Registro del proveedor de vistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a119816d388e07f1f032557af1171bb2666ef02a63d959b843b99b7942a790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992465"
---
# <a name="registering-the-view-provider"></a>Registro del proveedor de vistas

WMI registra automáticamente el archivo DLL del proveedor de vistas durante el proceso de instalación de WMI. Sin embargo, todavía debe registrar el proveedor de vistas con WMI para cada espacio de nombres que contendrá clases de vista.

En el procedimiento siguiente se describe cómo registrar el proveedor de vistas.

**Para registrar el proveedor de vistas**

1.  Cree una instancia de la [**\_ \_ clase Win32Provider**](--win32provider.md) para describir la implementación del proveedor de vistas.

    La [**\_ \_ instancia de Win32Provider**](--win32provider.md) describe el nombre del proveedor y su identificador de clase (CLSID), así como la configuración de seguridad predeterminada.

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

2.  Cree una instancia de la [**\_ \_ clase InstanceProviderRegistration.**](--instanceproviderregistration.md)

    En el ejemplo de código siguiente se muestra cómo crear una instancia de la **\_ \_ clase InstanceProviderRegistration.**

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

3.  Cree una instancia de la [**\_ \_ clase MethodProviderRegistration**](--methodproviderregistration.md) si desea que los métodos de compatibilidad de la clase de vista de unión.

    En el ejemplo de código siguiente se muestra cómo crear una instancia de la **\_ \_ clase MethodProviderRegistration.**

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  Compile el código MOF mediante el compilador MOF ([mofcomp](mofcomp.md)) o la [**interfaz IMofCompiler.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)

    Si guarda el ejemplo de código MOF enumerado anteriormente en un archivo denominado Viewtest.mof, use el comando Mofcomp para cargar el código MOF en el espacio de nombres de destino. *NamespacePath es* el espacio de nombres en el que desea crear la instancia de clase de vista.

    Escriba el siguiente comando en un símbolo del sistema para cargar el código MOF en el espacio de nombres de destino.

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    Para obtener más información, [vea Compilar archivos MOF](compiling-mof-files.md).

Para obtener más información, [vea Registrar un proveedor.](registering-a-provider.md)

 

 



