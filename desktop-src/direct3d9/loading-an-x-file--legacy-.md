---
description: Utilice el procedimiento siguiente en las aplicaciones heredadas para cargar un archivo. x.
ms.assetid: 2b975873-2e5d-4c64-a022-d2098c3d95b8
title: Cargar un archivo X (heredado) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ed54afdc7d1aa18fdde992a0799a8990a49c6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537029"
---
# <a name="loading-an-x-file-legacy-direct3d-9"></a><span data-ttu-id="cbc43-103">Cargar un archivo X (heredado) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cbc43-103">Loading an X File (Legacy) (Direct3D 9)</span></span>

<span data-ttu-id="cbc43-104">Utilice el procedimiento siguiente en las aplicaciones heredadas para cargar un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="cbc43-104">Use the following procedure in legacy applications to load a .x file.</span></span>

1.  <span data-ttu-id="cbc43-105">Use la función [**DirectXFileCreate**](directxfilecreate.md) para crear un objeto [**IDirectXFile**](idirectxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="cbc43-105">Use the [**DirectXFileCreate**](directxfilecreate.md) function to create an [**IDirectXFile**](idirectxfile.md) object.</span></span>
2.  <span data-ttu-id="cbc43-106">Si las plantillas están presentes en el archivo de DirectX que va a cargar, use el método [**IDirectXFile:: RegisterTemplates**](idirectxfile--registertemplates.md) para registrar dichas plantillas.</span><span class="sxs-lookup"><span data-stu-id="cbc43-106">If templates are present in the DirectX file that you will load, use the [**IDirectXFile::RegisterTemplates**](idirectxfile--registertemplates.md) method to register those templates.</span></span>
3.  <span data-ttu-id="cbc43-107">Use el método [**IDirectXFile:: CreateEnumObject**](idirectxfile--createenumobject.md) para crear un objeto de enumerador [**IDirectXFileEnumObject**](idirectxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="cbc43-107">Use the [**IDirectXFile::CreateEnumObject**](idirectxfile--createenumobject.md) method to create an [**IDirectXFileEnumObject**](idirectxfileenumobject.md) enumerator object.</span></span>
4.  <span data-ttu-id="cbc43-108">Recorra los objetos del archivo.</span><span class="sxs-lookup"><span data-stu-id="cbc43-108">Loop through the objects in the file.</span></span> <span data-ttu-id="cbc43-109">Para cada objeto, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="cbc43-109">For each object, perform the following steps.</span></span>
    1.  <span data-ttu-id="cbc43-110">Use el método [**IDirectXFileEnumObject:: GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) para recuperar cada objeto [**IDirectXFileData**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="cbc43-110">Use the [**IDirectXFileEnumObject::GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) method to retrieve each [**IDirectXFileData**](idirectxfiledata.md) object.</span></span>
    2.  <span data-ttu-id="cbc43-111">Use el método [**IDirectXFileData:: GetType**](idirectxfiledata--gettype.md) para recuperar el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cbc43-111">Use the [**IDirectXFileData::GetType**](idirectxfiledata--gettype.md) method to retrieve the data's type.</span></span>
    3.  <span data-ttu-id="cbc43-112">Cargue los datos mediante el método [**IDirectXFileData:: GetData**](idirectxfiledata--getdata.md) .</span><span class="sxs-lookup"><span data-stu-id="cbc43-112">Load the data using the [**IDirectXFileData::GetData**](idirectxfiledata--getdata.md) method.</span></span>
    4.  <span data-ttu-id="cbc43-113">Si el objeto tiene miembros opcionales, recupere los miembros opcionales llamando al método [**IDirectXFileData:: GetNextObject**](idirectxfiledata--getnextobject.md) .</span><span class="sxs-lookup"><span data-stu-id="cbc43-113">If the object has optional members, retrieve the optional members by calling the [**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md) method.</span></span>
    5.  <span data-ttu-id="cbc43-114">Libere el objeto [**IDirectXFileData**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="cbc43-114">Release the [**IDirectXFileData**](idirectxfiledata.md) object.</span></span>
5.  <span data-ttu-id="cbc43-115">Libere el objeto [**IDirectXFileEnumObject**](idirectxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="cbc43-115">Release the [**IDirectXFileEnumObject**](idirectxfileenumobject.md) object.</span></span>
6.  <span data-ttu-id="cbc43-116">Libere el objeto [**IDirectXFile**](idirectxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="cbc43-116">Release the [**IDirectXFile**](idirectxfile.md) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbc43-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cbc43-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbc43-118">Archivos X (heredado)</span><span class="sxs-lookup"><span data-stu-id="cbc43-118">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 



