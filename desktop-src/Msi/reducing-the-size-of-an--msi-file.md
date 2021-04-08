---
description: Es posible que los desarrolladores de paquetes de Windows Installer observen que sus archivos. msi son más grandes de lo esperado después de las modificaciones y guardaciones repetidas.
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: Reducir el tamaño de un archivo. msi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5a19c92f0567fc6081d772279ec2cc0b6cafef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001873"
---
# <a name="reducing-the-size-of-an-msi-file"></a>Reducir el tamaño de un archivo. msi

Es posible que los desarrolladores de paquetes de Windows Installer observen que sus archivos. msi son más grandes de lo esperado después de las modificaciones y guardaciones repetidas. Windows Installer archivos. msi son archivos compuestos que contienen almacenamientos y secuencias, y tienen algunas de las mismas limitaciones de almacenamiento que los archivos de documento OLE. Si edita y guarda el mismo archivo. msi una y otra vez, crea espacio de almacenamiento desperdiciado en el archivo. Esto solo afecta a los autores de archivos. msi y no tiene ningún efecto en Windows Installer usuarios. Los desarrolladores pueden querer quitar este espacio de almacenamiento desperdiciado antes de enviar su archivo. msi final.

Para quitar el espacio de almacenamiento desperdiciado y reducir el tamaño final de los archivos. msi, tiene las siguientes opciones.

-   Exporte todas las tablas de la base de datos a archivos. IDT y, a continuación, impórtelos en una nueva base de datos. Esto produce el almacenamiento más compacto posible.
-   Use una utilidad de software para compactar el espacio de almacenamiento de los archivos de documento OLE.

 

 



