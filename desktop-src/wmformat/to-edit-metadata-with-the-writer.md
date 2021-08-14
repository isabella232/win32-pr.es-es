---
title: Para editar metadatos con el escritor
description: Para editar metadatos con el escritor
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- Windows SDK de formato multimedia, edición de metadatos con el escritor
- Windows SDK de formato multimedia, edición de metadatos
- Formato de sistemas avanzados (ASF), edición de metadatos con el escritor
- ASF (formato de sistemas avanzados), edición de metadatos con el escritor
- Formato de sistemas avanzados (ASF), edición de metadatos
- ASF (formato de sistemas avanzados), edición de metadatos
- metadatos, edición con el escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d09db09a2cd7dbc50130243e322085ab2113e76f71d8b6760bd602d16f29d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197084"
---
# <a name="to-edit-metadata-with-the-writer"></a>Para editar metadatos con el escritor

Puede acceder, directamente desde el sistema de escritura, a los metadatos que irán al encabezado del archivo. Llame al **método QueryInterface** de cualquier interfaz del objeto writer para obtener un puntero a la [**interfaz IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) o [**IWMHeaderInfo2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) Después de tener un puntero a la interfaz adecuada, puede manipular los metadatos como lo haría si hubiera cargado el archivo en el objeto del editor de metadatos. Para obtener más información sobre cómo editar metadatos, vea [Trabajar con metadatos.](working-with-metadata.md)

Debe realizar todos los cambios en los metadatos antes de llamar a [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

> [!Note]  
> Si establece metadatos para un archivo, escribe el archivo y, a continuación, se prepara para escribir un nuevo archivo sin liberar el sistema de escritura, algunos metadatos que se han establecido para el primer archivo permanecerán establecidos y se incluirán con los archivos posteriores. Al escribir varios archivos con la misma instancia del objeto de escritor, tiene dos opciones: comprobar todos los metadatos antes de escribir cada archivo o escribir solo en los metadatos del escritor que se aplican a todos los archivos que está escribiendo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




