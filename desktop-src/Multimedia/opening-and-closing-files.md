---
title: Abrir y cerrar archivos
description: Abrir y cerrar archivos
ms.assetid: 72655d33-f685-4205-a982-f7cd20c59f22
keywords:
- Función AVIFileOpen
- Función AVIFileRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca5cfdce177e119d178ca09dd447b7d4e3b6a52c1881f059b72e4424f9c54c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038325"
---
# <a name="opening-and-closing-files"></a>Abrir y cerrar archivos

Una aplicación debe abrir un archivo AVI antes de leer o escribir. Para abrir un archivo AVI, use la [**función AVIFileOpen.**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) **AVIFileOpen** devuelve la dirección de una interfaz de archivo AVI que contiene el identificador del archivo abierto e incrementa el recuento de referencias del archivo.

La **función AVIFileOpen** admite las marcas OF usadas con la [función OpenFile.](/documentation/) Si una aplicación escribe en un archivo existente, debe incluir la marca OF \_ WRITE en **AVIFileOpen.** Del mismo modo, si la aplicación crea y escribe en un nuevo archivo, debe incluir las marcas OF CREATE y \_ OF \_ WRITE en **AVIFileOpen.**

Al abrir un archivo mediante **AVIFileOpen**, puede usar un controlador de archivos predeterminado o puede especificar un controlador de archivos personalizado para leer y escribir en el archivo y sus flujos de datos. En cualquier caso, AVIFile busca en el Registro el controlador de archivos correcto que se usará. Debe asegurarse de que los controladores de archivos personalizados están en el Registro antes de que una aplicación pueda acceder a ellos.

Puede incrementar el recuento de referencias de un archivo mediante la [**función AVIFileAddRef.**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) Por ejemplo, puede que desee hacerlo al pasar un identificador de la interfaz de archivo a otra aplicación o cuando desee mantener un archivo abierto mientras usa una función que normalmente cerraría el archivo.

Puede cerrar un archivo mediante la [**función AVIFileRelease.**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) La **función AVIFileRelease** disminuye el recuento de referencias de un archivo AVI, guarda los cambios realizados en el archivo y, cuando el recuento de referencias alcanza cero, cierra el archivo. Las aplicaciones deben equilibrar el recuento de referencias mediante la inclusión de una llamada a **AVIFileRelease** para cada uso de [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) y **AVIFileAddRef**.

> [!Note]  
> Una aplicación puede abrir un archivo con uno o varios subprocesos de programa. Sin embargo, para obtener el mejor rendimiento posible, solo un subproceso debe tener acceso al archivo en cualquier momento.

 

 

 