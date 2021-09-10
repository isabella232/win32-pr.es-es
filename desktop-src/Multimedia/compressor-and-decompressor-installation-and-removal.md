---
title: Instalación y eliminación de descompresión y descompresión
description: Instalación y eliminación de descompresión y descompresión
ms.assetid: 1f00d86f-a777-4bf8-8290-96cc83b2f331
keywords:
- Administrador de compresión de vídeo (VCM), instalación de instalaciones
- VCM (administrador de compresión de vídeo), instalación de instalaciones
- Función ICInstall
- Función ICRemove
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd65f0fc06dc1d5e90cb136f5cf4ea429c220d77
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372121"
---
# <a name="compressor-and-decompressor-installation-and-removal"></a>Instalación y eliminación de descompresión y descompresión

Una aplicación puede usar descomprimores y descompresión que ya están instalados en un sistema que ejecuta el sistema operativo Windows Microsoft. Una aplicación también puede instalar descomprimores y descompresión para usos generales o especiales. La mayoría de las aplicaciones no tendrán que instalar o quitar descomprimidores o descomprimidores, ya que normalmente se instalan mediante un programa de instalación. Sin embargo, una aplicación podría instalar directamente un dispositivo o instalar una función como un resalte.

Una aplicación puede instalar un descomprimidor o un descomprimidor (o una función que se usa como un descomprimidor o un descomprimidor) mediante [**la función ICInstall.**](/windows/desktop/api/Vfw/nf-vfw-icinstall) Esta función crea una entrada en el registro que identifica el descomprimidor o el descomprimidor. La aplicación u otra aplicación pueden buscar en el Registro para determinar si el sistema contiene un descomprimidor o un descomprimidor adecuado para sus datos. Use **ICInstall para** instalar todos los controladores de compresión y descompresión.

Una aplicación puede buscar y abrir un descomprimidor o descompresión instalado mediante las [**funciones ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) [**e ICOpen.**](/windows/desktop/api/Vfw/nf-vfw-icopen) Cuando una aplicación termina de usar un descompresión o un descomprimidor, lo cierra mediante la [**función ICClose.**](/windows/desktop/api/Vfw/nf-vfw-icclose)

Una aplicación puede quitar la entrada del Registro de un descomprimidor o descomprimido instalado mediante la [**función ICRemove.**](/windows/desktop/api/Vfw/nf-vfw-icremove) Esta función quita la entrada del Registro de un descomprimidor o descomprimido que no está cargado actualmente en memoria.

Una aplicación puede restringir el uso de un descomprimidor o descompresión instalando, abriendo, cerrando y quitando.

Como alternativa, para usar una función internamente como un descomprimidor o un descomprimidor sin instalarlo en el Registro, una aplicación puede usar la [**función ICOpenFunction.**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction) Esta función requiere que la aplicación que realiza la llamada tenga la dirección de la función que se usará como un descomprimidor o un descomprimidor. Cuando la aplicación termina de usar la función , debe cerrarla mediante **ICClose**. Dado que la función no se instaló, la aplicación no necesita quitar la función del Registro.

La estructura interna de una función que se usa como descomprimidor o decomisador debe ser la misma que la función de punto de entrada [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) que usan los controladores instalables. Para obtener más información sobre la función de punto de entrada **DriverProc,** vea [Controladores instalables.](installable-drivers.md)

> [!Note]  
> Una aplicación que instala una función como un descomprimidor o un descomprimidor debe quitar la función antes de que se cierre la aplicación para que otras aplicaciones no intenten usar la función. Al quitar una función, la aplicación debe identificarla con el código de cuatro caracteres usado para instalarla.

 

 

 