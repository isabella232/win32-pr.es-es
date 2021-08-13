---
title: Agregar, eliminar y reemplazar recursos
description: En este tema se describe cómo agregar, eliminar o reemplazar recursos.
ms.assetid: 15b1086e-e3a2-460a-828b-17db5105309f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c23375dbfff770a22b96ef7cb517af1c0b8d40579d6919a31a8136e1691474
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735298"
---
# <a name="adding-deleting-and-replacing-resources"></a>Agregar, eliminar y reemplazar recursos

Las aplicaciones deben agregar, eliminar o reemplazar recursos en archivos ejecutables con frecuencia. Se pueden usar dos métodos para realizar estas tareas. La primera es editar el archivo de definición de recursos, volver a compilar los recursos y agregar los recursos recompilados al archivo ejecutable de la aplicación. El segundo método consiste en copiar los datos del recurso directamente en el archivo ejecutable de la aplicación.

Por ejemplo, para localización de una aplicación en inglés para su uso en Noruega, puede ser necesario reemplazar el cuadro de diálogo inglés por uno con noruego. Un desarrollador crea un cuadro de diálogo adecuado mediante un editor de cuadros de diálogo o escribiendo una plantilla en el archivo de definición de recursos. A continuación, el desarrollador vuelve a compilar los recursos y agrega los nuevos recursos al archivo ejecutable de la aplicación.

Sin embargo, si existe un cuadro de diálogo adecuado en formato binario, el desarrollador puede copiar los datos directamente en el archivo ejecutable localizado mediante las funciones siguientes. La [**función BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea) crea un identificador de actualización para el archivo ejecutable cuyos recursos se van a cambiar. La [**función UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) usa este identificador para agregar, eliminar o reemplazar un recurso en el archivo ejecutable. La [**función EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) cierra el identificador.

Una vez que [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea)crea un identificador de actualización para un archivo ejecutable, una aplicación puede usar [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) repetidamente para realizar cambios en los datos del recurso. Cada llamada a **UpdateResource** contribuye a una lista interna de adiciones, eliminaciones y reemplazos, pero realmente no escribe los datos en el archivo ejecutable. Inmediatamente antes de cerrar el identificador de actualización, [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) escribe los cambios acumulados en el archivo ejecutable.

A veces, una aplicación debe copiar recursos de otro archivo. [La actualización](using-resources.md) de recursos muestra un ejemplo de cómo obtener los datos del recurso y su tamaño de un archivo.

 

 




