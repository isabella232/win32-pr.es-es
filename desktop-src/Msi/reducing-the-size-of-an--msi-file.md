---
description: Los desarrolladores de Windows Installer pueden observar que sus archivos .msi más grandes de lo esperado después de ediciones y guardados repetidos.
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: Reducir el tamaño de un archivo .msi archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5a19c92f0567fc6081d772279ec2cc0b6cafef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069703"
---
# <a name="reducing-the-size-of-an-msi-file"></a>Reducir el tamaño de un archivo .msi archivo

Los desarrolladores de Windows Installer pueden observar que sus archivos .msi más grandes de lo esperado después de ediciones y guardados repetidos. Windows Los archivos .msi instalador son archivos compuestos que contienen almacenamientos y secuencias, y tienen algunas de las mismas limitaciones de almacenamiento que los archivos de documento OLE. Si edita y guarda el mismo archivo .msi una y otra vez, se crea espacio de almacenamiento desperdiciado en el archivo. Esto solo afecta a los autores de .msi archivos y no tiene ningún efecto en Windows installer. Es posible que los desarrolladores quieran quitar este espacio de almacenamiento desperdiciado antes de enviar su archivo .msi final.

Para quitar el espacio de almacenamiento desperdiciado y reducir el tamaño final de .msi archivos, tiene las siguientes opciones.

-   Exporte todas las tablas de la base de datos a archivos .idt y, a continuación, impórtelos en una nueva base de datos. Esto genera el almacenamiento más compacto posible.
-   Use una utilidad de software para compactar el espacio de almacenamiento de los archivos de documento OLE.

 

 



