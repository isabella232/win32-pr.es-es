---
description: En este tema se describe cómo crear un experto genérico que se incluye con el SDK de Monitor de red.
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: Creación de un experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ead0ff222b72c66bfc88ec477d1a8d6a941273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276698"
---
# <a name="building-an-expert"></a>Creación de un experto

En este tema se describe cómo crear un experto genérico que se incluye con el SDK de Monitor de red.

> [!Note]  
> Antes de crear los siguientes ejemplos de código, instale el SDK de Monitor de red e inicialice el archivo de MySetEnv.bat.

 

**Para compilar un experto genérico**

1.  Abra un símbolo del sistema de Monitor de red y navegue hasta el \\ subdirectorio Experts; por ejemplo, C: \\ archivos de programa \\ NetMonSDK2 \\ Experts.
2.  Escriba **xcopy/e/s/V Blrplate**, a continuación, cuando se le solicite, escriba **D**.
3.  Desplácese al \\ subdirectorio de mi experto.
4.  Escriba **ren Blrplate \* . \* Mi experto \* . \*** Asegúrese de que se ha cambiado el nombre de todos los archivos correctamente. Compruebe los nombres de archivo comparando los archivos del \\ \\ subdirectorio Experts Blrplate.
5.  Modifique el archivo make reemplazando todas las apariciones de **Blrplate** por mi **experto**.
6.  Edite ambos archivos. cpp reemplazando todas las apariciones de **Blrplate** por mi **experto**. Tenga en cuenta que el identificador del cuadro de diálogo en config. cpp debe escribirse en mayúsculas (por ejemplo, mi **experto**).
7.  Edite el. h reemplazando todas las apariciones de **Blrplate** por mi **experto**.
8.  Edite Resrc1. h cambiando el nombre de **BLRPLATE** a mi **experto**. (Recuerde que **debe** escribirse en mayúsculas).
9.  Edite el archivo de mi experto. RC cambiando el nombre del cuadro de diálogo de configuración de BLRPLATE de IDD al cuadro de **\_ \_ \_ diálogo de configuración de IDD**. **\_ \_ \_**
10. Escriba **NMake** para compilar el archivo dll. Para comprobar la compilación, cambie el directorio al \\ subdirectorio obj y compruebe que el archivo existe. Para obtener más información, vea [Ver propiedades de archivos dll de expertos](viewing-expert-dll-properties.md).

Una vez completada la compilación, tendrá un archivo DLL experto que podrá probar e implementar con Monitor de red. Para obtener más información acerca de cómo instalar un experto, consulte [instalación de un experto en Monitor de red 2,1](installing-an-expert-to-network-monitor-2-1.md). Para obtener más información sobre cómo depurar un experto, consulte [depuración de un experto](debugging-an-expert.md).

 

 



