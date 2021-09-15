---
description: Esta sección contiene información de referencia de las interfaces COM que se usan para leer y escribir desde archivos .x de DirectX. En desuso.
ms.assetid: 66e3476a-4ee8-48ac-aab8-6653793e0ef3
title: Interfaces de archivo X
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6e47325a4912faeb919cb60571de3cccbbe265
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566021"
---
# <a name="x-file-interfaces"></a>Interfaces de archivo X

Esta sección contiene información de referencia de las interfaces COM que se usan para leer y escribir desde archivos .x de DirectX. En desuso.

-   [**IDirectXFile**](idirectxfile.md)
-   [**IDirectXFileBinary**](idirectxfilebinary.md)
-   [**IDirectXFileData**](idirectxfiledata.md)
-   [**IDirectXFileDataReference**](idirectxfiledatareference.md)
-   [**IDirectXFileEnumObject**](idirectxfileenumobject.md)
-   [**IDirectXFileObject**](idirectxfileobject.md)
-   [**IDirectXFileSaveObject**](idirectxfilesaveobject.md)

En las tablas siguientes se muestra la relación entre las interfaces de archivo .x.



| Interfaz             | Deriva de           | Deriva de |
|-----------------------|------------------------|--------------|
|                       | IDirectXFile           | IUnknown     |
| IDirectXFileBinary    | IDirectXFileObject     | IUnknown     |
| IDirectXFileData      | IDirectXFileObject     | IUnknown     |
| IDirectXFileReference | IDirectXFileObject     | IUnknown     |
|                       | IDirectXFileSaveObject | IUnknown     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de archivo X (heredado)](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



