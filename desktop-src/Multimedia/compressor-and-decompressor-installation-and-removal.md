---
title: Instalación y descompresor del compresor y descompresor
description: Instalación y descompresor del compresor y descompresor
ms.assetid: 1f00d86f-a777-4bf8-8290-96cc83b2f331
keywords:
- Administrador de compresión de vídeo (VCM), instalar compresores
- VCM (Administrador de compresión de vídeo), instalar compresores
- ICInstall función)
- ICRemove función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd65f0fc06dc1d5e90cb136f5cf4ea429c220d77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358831"
---
# <a name="compressor-and-decompressor-installation-and-removal"></a>Instalación y descompresor del compresor y descompresor

Una aplicación puede utilizar compresores y descompresores que ya están instalados en un sistema que ejecuta el sistema operativo Microsoft Windows. Una aplicación también puede instalar comprimiendores y descompresores para usos generales o especiales. La mayoría de las aplicaciones no necesitará instalar o quitar compresores o descompresores porque normalmente los instala un programa de instalación. Sin embargo, una aplicación puede instalar un compresor directamente o instalar una función como compresor.

Una aplicación puede instalar un compresor o descompresor (o una función usada como compresor o descompresor) mediante la función [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) . Esta función crea una entrada en el registro que identifica el compresor o descompresor. La aplicación u otra aplicación puede buscar en el registro para determinar si el sistema contiene un compresor o descompresor adecuado para sus datos. Use **ICInstall** para instalar todos los controladores de compresión y descompresión.

Una aplicación puede buscar y abrir un compresor o descompresor instalado mediante las funciones [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) y [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) . Cuando una aplicación termina de usar un compresor o descompresor, la cierra mediante la función [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) .

Una aplicación puede quitar la entrada del registro de un compresor o descompresor instalado mediante la función [**ICRemove**](/windows/desktop/api/Vfw/nf-vfw-icremove) . Esta función quita la entrada del registro de un compresor o descompresor que no está cargado actualmente en la memoria.

Una aplicación puede restringir el uso de un compresor o descompresor mediante la instalación, apertura, cierre y eliminación.

Como alternativa, para utilizar una función internamente como compresor o descompresor sin necesidad de instalarla en el registro, una aplicación puede usar la función [**ICOpenFunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction) . Esta función requiere que la aplicación que realiza la llamada tenga la dirección de la función que se va a usar como compresor o descompresor. Cuando la aplicación termina de usar la función, debe cerrarla mediante **ICClose**. Dado que la función no se ha instalado, no es necesario que la aplicación Quite la función del registro.

La estructura interna de una función utilizada como compresor o descompresor debe ser la misma que la función de punto de entrada [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) que usan los controladores instalables. Para obtener más información sobre la función de punto de entrada **DriverProc** , vea [Controladores instalables](installable-drivers.md).

> [!Note]  
> Una aplicación que instala una función como compresor o descompresor debe quitar la función antes de que se cierre la aplicación para que otras aplicaciones no intenten usar la función. Al quitar una función, la aplicación debe identificarla con el código de cuatro caracteres que se usa para instalarla.

 

 

 