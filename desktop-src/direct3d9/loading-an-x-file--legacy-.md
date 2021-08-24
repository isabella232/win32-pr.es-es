---
description: Use el procedimiento siguiente en aplicaciones heredadas para cargar un archivo .x.
ms.assetid: 2b975873-2e5d-4c64-a022-d2098c3d95b8
title: Cargar un archivo X (heredado) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8ac27c43ba33f6bd0408403d6390d4855f2644182d82f1ad8e84e5939f98ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846525"
---
# <a name="loading-an-x-file-legacy-direct3d-9"></a>Cargar un archivo X (heredado) (Direct3D 9)

Use el procedimiento siguiente en aplicaciones heredadas para cargar un archivo .x.

1.  Use la [**función DirectXFileCreate**](directxfilecreate.md) para crear un [**objeto IDirectXFile.**](idirectxfile.md)
2.  Si las plantillas están presentes en el archivo DirectX que se va a cargar, use el método [**IDirectXFile::RegisterTemplates**](idirectxfile--registertemplates.md) para registrar esas plantillas.
3.  Use el [**método IDirectXFile::CreateEnumObject**](idirectxfile--createenumobject.md) para crear un objeto [**enumerador IDirectXFileEnumObject.**](idirectxfileenumobject.md)
4.  Recorrer en bucle los objetos del archivo. Para cada objeto, realice los pasos siguientes.
    1.  Use el [**método IDirectXFileEnumObject::GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) para recuperar cada [**objeto IDirectXFileData.**](idirectxfiledata.md)
    2.  Use el [**método IDirectXFileData::GetType**](idirectxfiledata--gettype.md) para recuperar el tipo de los datos.
    3.  Cargue los datos mediante el [**método IDirectXFileData::GetData.**](idirectxfiledata--getdata.md)
    4.  Si el objeto tiene miembros opcionales, recupere los miembros opcionales llamando al método [**IDirectXFileData::GetNextObject.**](idirectxfiledata--getnextobject.md)
    5.  Libere el [**objeto IDirectXFileData.**](idirectxfiledata.md)
5.  Libere el [**objeto IDirectXFileEnumObject.**](idirectxfileenumobject.md)
6.  Libere el [**objeto IDirectXFile.**](idirectxfile.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Archivos X (heredados)](x-files--legacy-.md)
</dt> </dl>

 

 



