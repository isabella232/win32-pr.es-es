---
title: Para editar los metadatos con el escritor
description: Para editar los metadatos con el escritor
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- SDK de Windows Media Format, edición de metadatos con el escritor
- SDK de Windows Media Format, edición de metadatos
- Advanced Systems Format (ASF), edición de metadatos con el sistema de escritura
- ASF (formato de sistemas avanzados), edición de metadatos con el sistema de escritura
- Advanced Systems Format (ASF), edición de metadatos
- ASF (formato de sistemas avanzados), edición de metadatos
- metadatos, editar con el escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2823b266b51da366683ac0b5cf65e10debf1ad
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104420455"
---
# <a name="to-edit-metadata-with-the-writer"></a>Para editar los metadatos con el escritor

Puede tener acceso a, directamente desde el escritor, los metadatos que entrarán en el encabezado del archivo. Llame al método **QueryInterface** de cualquier interfaz del objeto Writer para obtener un puntero a la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) o [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) . Después de tener un puntero a la interfaz adecuada, puede manipular los metadatos tal como lo haría si hubiera cargado el archivo en el objeto del editor de metadatos. Para obtener más información sobre la edición de metadatos, vea [trabajar con metadatos](working-with-metadata.md).

Debe realizar todos los cambios en los metadatos antes de llamar a [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

> [!Note]  
> Si establece los metadatos de un archivo, escribe el archivo y, a continuación, prepara para escribir un archivo nuevo sin liberar el escritor, algunos metadatos que se establecieron para el primer archivo permanecerán establecidos y se incluirán con los archivos siguientes. Al escribir varios archivos con la misma instancia del objeto escritor, tiene dos opciones: comprobar todos los metadatos antes de escribir cada archivo o solo escribir en los metadatos del escritor que se aplican a todos los archivos que está escribiendo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




