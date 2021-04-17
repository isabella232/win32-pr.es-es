---
description: Muestra cómo usar las interfaces VSS para crear un proveedor de hardware VSS.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: Herramienta y ejemplo de VssSampleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fceaa65b851e5469a3e82323da92d8bde0651a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696444"
---
# <a name="vsssampleprovider-tool-and-sample"></a>Herramienta y ejemplo de VssSampleProvider

Muestra cómo usar las [interfaces](volume-shadow-copy-api-interfaces.md) VSS para crear un proveedor de hardware VSS.

> [!Note]  
> La herramienta VssSampleProvider y el ejemplo se incluyen en el kit de desarrollo de software (SDK) de Microsoft Windows. Puede descargar el Windows SDK desde el [Kit de desarrollo de software (SDK) de Windows para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).

 

En la instalación de Windows SDK, la herramienta VssSampleProvider se puede encontrar en `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para Windows de 64 bits) y `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (para windows de 32 bits).

> [!Note]  
> Los proveedores de hardware solo se admiten en sistemas operativos Windows Server. En un sistema operativo de cliente de Windows, puede compilar el ejemplo VssSampleProvider, pero no puede registrarlo como proveedor de hardware.

 

La herramienta VssSampleProvider consta de los siguientes archivos:

-   Virtualstorage.sys
-   Vstorcontrol.exe
-   Vssampleprovider.dll
-   Vstorinterface.dll

El ejemplo VssSampleProvider incluye los siguientes scripts de instalación y desinstalación:

-   Install-sampleprovider. cmd
-   Uninstall-sampleprovider. cmd
-   Registrar \_app.vbs

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

        

        Este comando crea un LUN virtual cuyo identificador de almacenamiento es **proveedor de HW de ejemplo de VSS**. Para crear LUN virtuales adicionales, repita este paso.

        El proveedor de ejemplo de VSS reconoce un LUN solo si el **proveedor de HW de ejemplo de VSS** forma parte del identificador de almacenamiento. Para obtener más información sobre el identificador de almacenamiento, consulte la siguiente entrada de blog.

        [LUN: resincronización con DiskShadow y almacenamiento virtual](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  En la ventana del símbolo del sistema, use diskpart.exe para formatear el disco virtual y asignarle una letra de unidad.

        Este es un script de ejemplo para ejecutar en el símbolo del sistema de Diskpart.

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

    

 

 



