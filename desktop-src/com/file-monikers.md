---
title: Monikers de archivo
description: Monikers de archivo
ms.assetid: 923f798d-d789-4e6d-b27e-dd5a72f92abf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c18beeff04804b11f04c0a2c211f2dd09dd60d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356900"
---
# <a name="file-monikers"></a><span data-ttu-id="f3afc-103">Monikers de archivo</span><span class="sxs-lookup"><span data-stu-id="f3afc-103">File Monikers</span></span>

<span data-ttu-id="f3afc-104">Los *monikers de archivo* son la clase de moniker más sencilla.</span><span class="sxs-lookup"><span data-stu-id="f3afc-104">*File monikers* are the simplest moniker class.</span></span> <span data-ttu-id="f3afc-105">Los monikers de archivo se pueden usar para identificar cualquier objeto almacenado en su propio archivo.</span><span class="sxs-lookup"><span data-stu-id="f3afc-105">File monikers can be used to identify any object that is stored in its own file.</span></span> <span data-ttu-id="f3afc-106">Un moniker de archivo actúa como un contenedor para el nombre de la ruta de acceso que el sistema de archivos nativo asigna al archivo.</span><span class="sxs-lookup"><span data-stu-id="f3afc-106">A file moniker acts as a wrapper for the path name the native file system assigns to the file.</span></span> <span data-ttu-id="f3afc-107">La llamada a [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) para este moniker haría que este objeto se activara y, a continuación, devolvería un puntero de interfaz al objeto.</span><span class="sxs-lookup"><span data-stu-id="f3afc-107">Calling [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) for this moniker would cause this object to be activated and then would return an interface pointer to the object.</span></span> <span data-ttu-id="f3afc-108">El origen del objeto denominado por el moniker debe proporcionar una implementación de la interfaz [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) para admitir el enlace de un moniker de archivo.</span><span class="sxs-lookup"><span data-stu-id="f3afc-108">The source of the object named by the moniker must provide an implementation of the [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) interface to support binding a file moniker.</span></span> <span data-ttu-id="f3afc-109">Los monikers de archivo pueden representar una ruta de acceso completa o relativa.</span><span class="sxs-lookup"><span data-stu-id="f3afc-109">File monikers can represent either a complete or a relative path.</span></span>

<span data-ttu-id="f3afc-110">Por ejemplo, el moniker de archivo de un objeto de hoja de cálculo almacenado como el archivo C: \\ Work \\MySheet.xls contendría información equivalente a ese nombre de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="f3afc-110">For example, the file moniker for a spreadsheet object stored as the file C:\\Work\\MySheet.xls would contain information equivalent to that path name.</span></span> <span data-ttu-id="f3afc-111">Sin embargo, el moniker no consistiría necesariamente en la misma cadena.</span><span class="sxs-lookup"><span data-stu-id="f3afc-111">The moniker would not necessarily consist of the same string, however.</span></span> <span data-ttu-id="f3afc-112">La cadena es simplemente su *nombre de displayÂ*, una representación del contenido del moniker que es significativa para un usuario final.</span><span class="sxs-lookup"><span data-stu-id="f3afc-112">The string is just its *displayÂ name*, a representation of the moniker's contents that is meaningful to an end user.</span></span> <span data-ttu-id="f3afc-113">El nombre para mostrar, que está disponible a través del método [**IMoniker:: getDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) , solo se usa cuando se muestra un moniker para un usuario final.</span><span class="sxs-lookup"><span data-stu-id="f3afc-113">The display name, which is available through the [**IMoniker::GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) method, is used only when displaying a moniker to an end user.</span></span> <span data-ttu-id="f3afc-114">Este método obtiene el nombre para mostrar de cualquiera de las clases moniker.</span><span class="sxs-lookup"><span data-stu-id="f3afc-114">This method gets the display name for any of the moniker classes.</span></span> <span data-ttu-id="f3afc-115">Internamente, el moniker puede almacenar la misma información en un formato más eficaz para realizar operaciones de moniker, pero no tiene sentido para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="f3afc-115">Internally, the moniker may store the same information in a format that is more efficient for performing moniker operations but isn't meaningful to users.</span></span> <span data-ttu-id="f3afc-116">A continuación, cuando este mismo objeto se enlaza a través de una llamada al método [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) , el objeto se activaría, probablemente mediante la carga del archivo en la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="f3afc-116">Then, when this same object is bound through a call to the [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) method, the object would be activated, probably by loading the file into the spreadsheet.</span></span>

<span data-ttu-id="f3afc-117">OLE ofrece a los proveedores de monikers la función auxiliar [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) que crea un objeto de moniker de archivo y devuelve su puntero al proveedor.</span><span class="sxs-lookup"><span data-stu-id="f3afc-117">OLE offers moniker providers the helper function [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) that creates a file moniker object and returns its pointer to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3afc-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3afc-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3afc-119">Anti-monikers</span><span class="sxs-lookup"><span data-stu-id="f3afc-119">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="f3afc-120">Monikers de clase</span><span class="sxs-lookup"><span data-stu-id="f3afc-120">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="f3afc-121">Monikers compuestos</span><span class="sxs-lookup"><span data-stu-id="f3afc-121">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="f3afc-122">Monikers de elemento</span><span class="sxs-lookup"><span data-stu-id="f3afc-122">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="f3afc-123">Monikers de puntero</span><span class="sxs-lookup"><span data-stu-id="f3afc-123">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




