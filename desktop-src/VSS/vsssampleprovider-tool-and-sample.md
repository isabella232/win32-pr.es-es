---
description: Muestra cómo usar las interfaces de VSS para crear un proveedor de hardware de VSS.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: Ejemplo y herramienta VssSampleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8263c8c0db811892cf32f3887a862e13156a22934edac44d0b2c7a6922cbd6bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118842393"
---
# <a name="vsssampleprovider-tool-and-sample"></a>Ejemplo y herramienta VssSampleProvider

Muestra cómo usar las [interfaces](volume-shadow-copy-api-interfaces.md) de VSS para crear un proveedor de hardware de VSS.

> [!Note]  
> La herramienta VssSampleProvider y el ejemplo se incluyen en el Kit de desarrollo de software (SDK) de Microsoft Windows. Puede descargar el SDK de Windows desde [Windows Software Development Kit (SDK) para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).

 

En la instalación del SDK de Windows, la herramienta VssSampleProvider se puede encontrar en (para Windows de 64 bits) y (para archivos de `%Program Files(x86)%\Windows Kits\8.1\bin\x64` `%Program Files(x86)%\Windows Kits\8.1\bin\x86` 32 Windows).

> [!Note]  
> Los proveedores de hardware solo se admiten en Windows operativos server. En un Windows operativo cliente, puede compilar el ejemplo VssSampleProvider, pero no puede registrarlo como proveedor de hardware.

 

La herramienta VssSampleProvider consta de los siguientes archivos:

-   Virtualstorage.sys
-   Vstorcontrol.exe
-   Vssampleprovider.dll
-   Vstorinterface.dll

El ejemplo VssSampleProvider incluye los siguientes scripts de instalación y desinstalación:

-   Install-sampleprovider.cmd
-   Uninstall-sampleprovider.cmd
-   Registro \_app.vbs

**Para instalar y usar el ejemplo VssSampleProvider**

1.  Vaya al directorio `Program Files (x86)\Windows Kits\8.0\bin\`. Este directorio contiene virtualstoragevss.sys y vstorcontrol.exe.
2.  Abra una ventana del símbolo del sistema en el directorio especificado.
3.  Para instalar el controlador de almacenamiento virtual, en la ventana del símbolo del sistema, escriba el siguiente comando:

    ```cmd
    vstorcontrol.exe install
    ```

    

4.  Para instalar el proveedor de ejemplo de VSS, en la ventana del símbolo del sistema, escriba el siguiente comando:

    ```cmd
    install-sampleprovider.cmd
    ```

    

5.  Para crear un LUN virtual, haga lo siguiente.

    1.  En la ventana del símbolo del sistema, escriba el siguiente comando:

        ```cmd
        vstorcontrol.exe create fixeddisk -
        newimage C:\disk1.image -size 20M -storid "VSS Sample HW Provider"
        ```

        

        Este comando crea un LUN virtual cuyo identificador de almacenamiento es proveedor de HW de ejemplo **de VSS.** Para crear LUN virtuales adicionales, repita este paso.

        El proveedor de ejemplo de VSS reconoce un LUN solo si el proveedor de HW de ejemplo de **VSS** forma parte del identificador de almacenamiento. Para obtener más información sobre el identificador de almacenamiento, vea la siguiente entrada de blog.

        [LUN: resincronización con Diskshadow y Virtual Storage](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  En la ventana del símbolo del sistema, use diskpart.exe para dar formato al disco virtual y asignarle una letra de unidad.

        Este es un script de ejemplo para ejecutarlo en el símbolo del sistema diskpart.

        ```cmd
        Select disk 
        Create partition primary size=<size>
        Format FS=NTFS quick
        Assign Letter=<letter>
        Exit
        ```

        

6.  Para ejecutar el proveedor de ejemplo, en la ventana del símbolo del sistema, escriba el siguiente comando:

    ```cmd
    Run vshadow.exe -p -nw <drive>
    ```

    

    *<drive>* representa la letra de unidad del LUN virtual.

7.  Para desinstalar el proveedor de ejemplo de VSS, en la ventana del símbolo del sistema, escriba el siguiente comando:

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  Para desinstalar el controlador de almacenamiento virtual, en la ventana del símbolo del sistema, escriba el siguiente comando:

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



