---
description: Use el procedimiento siguiente en aplicaciones heredadas para guardar plantillas de archivo .x y datos en un archivo .x.
ms.assetid: 5401b381-3599-465a-b41b-e63b7372fc0e
title: Guardar en un archivo X (heredado) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03070b25c8839ddd17ab698a4f017822004d027d978b5c4ce589491f2e8fb8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797787"
---
# <a name="saving-to-an-x-file-legacy-direct3d-9"></a>Guardar en un archivo X (heredado) (Direct3D 9)

Use el procedimiento siguiente en aplicaciones heredadas para guardar plantillas de archivo .x y datos en un archivo .x.

1.  Use la [**función DirectXFileCreate**](directxfilecreate.md) para crear un [**objeto IDirectXFile.**](idirectxfile.md)
2.  Use el [**método IDirectXFile::RegisterTemplates**](idirectxfile--registertemplates.md) para informar al sistema de archivos de DirectX sobre las plantillas que usará.
3.  Use el [**método IDirectXFile::CreateSaveObject**](idirectxfile--createsaveobject.md) para crear un [**objeto IDirectXFileSaveObject.**](idirectxfilesaveobject.md)
4.  Use el [**método IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md) para guardar plantillas, si lo desea.
5.  Recorrer en bucle los objetos que se guardarán. Para cada objeto de nivel superior, realice los pasos siguientes.
    -   Use el [**método IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) para crear un objeto [**IDirectXFileData**](idirectxfiledata.md) como un objeto de nivel superior en el archivo. Si el objeto de datos de nivel superior tiene objetos secundarios opcionales, agrégrelos al objeto mediante el método adecuado del paso siguiente.
    -   Cada [**objeto IDirectXFileData**](idirectxfiledata.md) puede tener objetos secundarios opcionales si su plantilla lo permite. Los objetos secundarios pueden ser cualquiera de los tres tipos de objetos: **IDirectXFileData,** [**IDirectXFileDataReference**](idirectxfiledatareference.md)o [**IDirectXFileBinary.**](idirectxfilebinary.md) Recorrer en bucle los objetos que necesita guardar y agregar cada miembro secundario opcional a la lista de objetos de la manera adecuada para su tipo, como se muestra en los pasos siguientes. A continuación, si el tipo de objeto es Data, llame al método [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) para crear un objeto **IDirectXFileData** y, a continuación, llame al método [**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md) para agregarlo como elemento secundario del objeto . Si el tipo de objeto es Referencia de datos, llame al método [**IDirectXFileData::AddDataReference**](idirectxfiledata--adddatareference.md) para crear y agregar el objeto de referencia de datos como elemento secundario del objeto . O bien, si el tipo de objeto es Binary, llame al método [**IDirectXFileData::AddBinaryObject**](idirectxfiledata--addbinaryobject.md) para crear y agregar el objeto binario como elemento secundario del objeto.
    -   Llame al [**método IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) para guardar el objeto de datos y sus secundarios.
    -   Libere el [**objeto IDirectXFileData.**](idirectxfiledata.md)
6.  Libere el [**objeto IDirectXFileSaveObject.**](idirectxfilesaveobject.md)
7.  Libere el [**objeto IDirectXFile.**](idirectxfile.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Archivos X (heredados)](x-files--legacy-.md)
</dt> </dl>

 

 



