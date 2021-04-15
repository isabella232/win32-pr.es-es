---
title: Abrir y cerrar archivos
description: Abrir y cerrar archivos
ms.assetid: 72655d33-f685-4205-a982-f7cd20c59f22
keywords:
- AVIFileOpen función)
- AVIFileRelease función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e1c51c4747e03bf4f18a8e6c560e45798e1c8c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105689706"
---
# <a name="opening-and-closing-files"></a>Abrir y cerrar archivos

Una aplicación debe abrir un archivo AVI antes de leerlo o escribir en él. Para abrir un archivo AVI, utilice la función [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) . **AVIFileOpen** devuelve la dirección de una interfaz de archivo AVI que contiene el identificador del archivo abierto e incrementa el recuento de referencias del archivo.

La función **AVIFileOpen** admite el de las marcas usadas con la función [OpenFile](/documentation/) . Si una aplicación escribe en un archivo existente, debe incluir el marcador de \_ escritura en **AVIFileOpen**. Del mismo modo, si la aplicación crea y escribe en un nuevo archivo, debe incluir la de \_ Create y de las \_ marcas de escritura en **AVIFileOpen**.

Al abrir un archivo con **AVIFileOpen**, puede utilizar un controlador de archivos predeterminado o puede especificar un controlador de archivos personalizado para leer y escribir en el archivo y sus flujos de datos. En cualquier caso, AVIFile busca en el registro el controlador de archivos correcto que se va a usar. Debe asegurarse de que los controladores de archivos personalizados se encuentran en el registro antes de que una aplicación pueda tener acceso a ellos.

Puede incrementar el recuento de referencias de un archivo mediante la función [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) . Por ejemplo, puede que desee hacer esto al pasar un identificador de la interfaz de archivo a otra aplicación, o bien cuando desee mantener un archivo abierto mientras usa una función que normalmente cerraría el archivo.

Puede cerrar un archivo mediante la función [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) . La función **AVIFileRelease** disminuye el recuento de referencias de un archivo AVI, guarda los cambios realizados en el archivo y, cuando el recuento de referencias llega a cero, cierra el archivo. Las aplicaciones deben equilibrar el recuento de referencias incluyendo una llamada a **AVIFileRelease** para cada uso de [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) y **AVIFileAddRef**.

> [!Note]  
> Una aplicación puede abrir un archivo con uno o más subprocesos del programa. Sin embargo, para obtener el mejor rendimiento posible, solo un subproceso debe tener acceso al archivo en cualquier momento.

 

 

 