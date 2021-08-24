---
title: Instalación y eliminación de descomprimir y descomprimir
description: Instalación y eliminación de descomprimir y descomprimir
ms.assetid: 1f00d86f-a777-4bf8-8290-96cc83b2f331
keywords:
- Administrador de compresión de vídeo (VCM), instalación de los programas
- VCM (administrador de compresión de vídeo), instalación de paquetes
- Función ICInstall
- Función ICRemove
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82a34f1818f9a60226c0f3cead8186ae3fa163ebe1782c0c83e7cfb5b633c1b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144988"
---
# <a name="compressor-and-decompressor-installation-and-removal"></a>Instalación y eliminación de descomprimir y descomprimir

Una aplicación puede usar los descompresores y los que ya están instalados en un sistema que ejecuta microsoft Windows sistema operativo. Una aplicación también puede instalar descompresores y descompresores para usos generales o especiales. La mayoría de las aplicaciones no tendrán que instalar o quitar descomprimidores o descomprimidores, ya que normalmente se instalan mediante un programa de instalación. Sin embargo, una aplicación podría instalar un elemento directamente o instalar una función como un resalte.

Una aplicación puede instalar un descomprimidor o un descomprimidor (o una función que se usa como descomprimidor o descompresión) mediante [**la función ICInstall.**](/windows/desktop/api/Vfw/nf-vfw-icinstall) Esta función crea una entrada en el registro que identifica el descomprimidor o el descomprimidor. La aplicación u otra aplicación pueden buscar en el Registro para determinar si el sistema contiene un descomprimidor o un descompresión adecuado para sus datos. Use **ICInstall para** instalar todos los controladores de compresión y descompresión.

Una aplicación puede buscar y abrir un descomprimidor o descompresión instalados mediante las funciones [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) [**e ICOpen.**](/windows/desktop/api/Vfw/nf-vfw-icopen) Cuando una aplicación termina de usar un descomprimidor o un descomprimidor, la cierra mediante la [**función ICClose.**](/windows/desktop/api/Vfw/nf-vfw-icclose)

Una aplicación puede quitar la entrada del Registro de un descomprimidor o descompresión instalado mediante [**la función ICRemove.**](/windows/desktop/api/Vfw/nf-vfw-icremove) Esta función quita la entrada del Registro de un descomprimidor o descompresión que no está cargado actualmente en la memoria.

Una aplicación puede restringir el uso de un descomprimidor o descompresión instalando, abriendo, cerrando y quitando.

Como alternativa, para usar una función internamente como un descomprimidor o descompresión sin instalarla en el Registro, una aplicación puede usar la [**función ICOpenFunction.**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction) Esta función requiere que la aplicación que realiza la llamada tenga la dirección de la función que se va a usar como un descomprimido o un descomprimidor. Cuando la aplicación termina de usar la función , debe cerrarla mediante **ICClose**. Dado que la función no se instaló, la aplicación no necesita quitar la función del Registro.

La estructura interna de una función que se usa como descompresión o descompresión debe ser la misma que la función de punto de entrada [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) que usan los controladores instalables. Para obtener más información sobre la función de punto de **entrada DriverProc,** vea [Controladores instalables.](installable-drivers.md)

> [!Note]  
> Una aplicación que instala una función como un descomprimidor o un descomprimidor debe quitar la función antes de cerrar la aplicación para que otras aplicaciones no intenten usar la función. Al quitar una función, la aplicación debe identificarla con el código de cuatro caracteres usado para instalarla.

 

 

 