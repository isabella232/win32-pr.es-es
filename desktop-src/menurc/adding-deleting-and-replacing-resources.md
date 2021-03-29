---
title: Agregar, eliminar y reemplazar recursos
description: En este tema se describe cómo agregar, eliminar o reemplazar recursos.
ms.assetid: 15b1086e-e3a2-460a-828b-17db5105309f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941c12a1531e422efe44cbd0b3deca9f89838698
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665701"
---
# <a name="adding-deleting-and-replacing-resources"></a>Agregar, eliminar y reemplazar recursos

Las aplicaciones deben agregar, eliminar o reemplazar recursos con frecuencia en archivos ejecutables. Se pueden usar dos métodos para llevar a cabo estas tareas. La primera es editar el archivo de definición de recursos, volver a compilar los recursos y agregar los recursos recompilados al archivo ejecutable de la aplicación. El segundo método consiste en copiar los datos de recursos directamente en el archivo ejecutable de la aplicación.

Por ejemplo, para localizar una aplicación en inglés para su uso en Noruega, puede que sea necesario reemplazar el cuadro de diálogo inglés por otro con noruego. Un programador crea un cuadro de diálogo adecuado mediante un editor de cuadros de diálogo o escribiendo una plantilla en el archivo de definición de recursos. A continuación, el desarrollador vuelve a compilar los recursos y agrega los nuevos recursos al archivo ejecutable de la aplicación.

Sin embargo, si existe un cuadro de diálogo adecuado en formato binario, el desarrollador puede copiar los datos directamente en el archivo ejecutable que se está localizando mediante las siguientes funciones. La función [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea) crea un identificador de actualización para el archivo ejecutable cuyos recursos se van a cambiar. La función [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) usa este identificador para agregar, eliminar o reemplazar un recurso en el archivo ejecutable. La función [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) cierra el identificador.

Una vez que [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea)crea un identificador de actualización para un archivo ejecutable, una aplicación puede usar [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) repetidamente para realizar cambios en los datos del recurso. Cada llamada a **UpdateResource** contribuye a una lista interna de adiciones, eliminaciones y reemplazos, pero no escribe realmente los datos en el archivo ejecutable. Inmediatamente antes de cerrar el identificador de actualización, [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) escribe los cambios acumulados en el archivo ejecutable.

A veces, una aplicación debe copiar recursos desde otro archivo. [Actualizar recursos](using-resources.md) muestra un ejemplo de cómo obtener los datos de recursos y su tamaño de un archivo.

 

 




