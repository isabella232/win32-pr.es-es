---
title: Monikers de clase
description: Aunque las clases se identifican normalmente directamente con CLSID en funciones como CoCreateInstance o CoGetClassObject, las clases también pueden identificarse con un moniker denominado moniker de clase.
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80886ce49ea25d2fb5acbf4dddf550c9d2c3ae29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357652"
---
# <a name="class-monikers"></a><span data-ttu-id="2514a-103">Monikers de clase</span><span class="sxs-lookup"><span data-stu-id="2514a-103">Class Monikers</span></span>

<span data-ttu-id="2514a-104">Aunque las clases se identifican normalmente directamente con CLSID en funciones como [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), las clases también pueden identificarse con un moniker denominado *moniker de clase*.</span><span class="sxs-lookup"><span data-stu-id="2514a-104">Although classes are typically identified directly with CLSIDs to functions such as [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), classes may also now be identified with a moniker called a *class moniker*.</span></span> <span data-ttu-id="2514a-105">Los monikers de clase se enlazan al objeto de clase de la clase para la que se crean.</span><span class="sxs-lookup"><span data-stu-id="2514a-105">Class monikers bind to the class object of the class for which they are created.</span></span>

<span data-ttu-id="2514a-106">La capacidad de identificar clases con un moniker admite operaciones útiles que, de lo contrario, son difíciles de manejar.</span><span class="sxs-lookup"><span data-stu-id="2514a-106">The ability to identify classes with a moniker supports useful operations that are otherwise unwieldy.</span></span> <span data-ttu-id="2514a-107">Por ejemplo, los monikers de archivo tradicionalmente admitía el enlace enriquecido solo a la clase asociada a la clase de archivo a la que hacía referencia; un moniker a un archivo de Excel se enlazaría a una instancia de un objeto de Excel y un moniker a una imagen GIF se enlazaría a una instancia del controlador GIF registrado actualmente.</span><span class="sxs-lookup"><span data-stu-id="2514a-107">For example, file monikers traditionally supported rich binding only to the class associated with the class of file they referred to; a moniker to an Excel file would bind to an instance of an Excel object, and a moniker to a GIF image would bind to an instance of the currently registered GIF handler.</span></span> <span data-ttu-id="2514a-108">Un moniker de clase le permite indicar la clase que desea utilizar para manipular un archivo a través de la composición con un moniker de archivo.</span><span class="sxs-lookup"><span data-stu-id="2514a-108">A class moniker allows you to indicate the class you want to use to manipulate a file through composition with a file moniker.</span></span> <span data-ttu-id="2514a-109">Un moniker de clase para una clase de gráficos 3D compuesto con un moniker para un archivo de Excel produce un moniker que se enlaza a una instancia del objeto de gráfico 3D e inicializa el objeto con el contenido del archivo de Excel.</span><span class="sxs-lookup"><span data-stu-id="2514a-109">A class moniker for a 3D charting class composed with a moniker to an Excel file yields a moniker that binds to an instance of the 3D charting object and initializes the object with the contents of the Excel file.</span></span>

<span data-ttu-id="2514a-110">Por lo tanto, los monikers de clase son más útiles en la composición con otros tipos de monikers, como monikers de archivo o monikers de elemento.</span><span class="sxs-lookup"><span data-stu-id="2514a-110">Class monikers are therefore most useful in composition with other types of monikers, such as file monikers or item monikers.</span></span>

<span data-ttu-id="2514a-111">Los monikers de clase también se pueden componer a la derecha de monikers que admiten enlaces a la interfaz [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) .</span><span class="sxs-lookup"><span data-stu-id="2514a-111">Class monikers may also be composed to the right of monikers supporting binding to the [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) interface.</span></span> <span data-ttu-id="2514a-112">Cuando se componen de esta manera, **IClassActivator** simplemente proporciona acceso al objeto de clase y a las instancias de la clase a través de [**IClassActivator:: getclassobject (**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject).</span><span class="sxs-lookup"><span data-stu-id="2514a-112">When composed in this manner, **IClassActivator** simply gives access to the class object and instances of the class through [**IClassActivator::GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject).</span></span> <span data-ttu-id="2514a-113">Los monikers de clase se pueden identificar mediante [**IMoniker:: IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), que devuelve MKSYS \_ CLASSMONIKER en *pdwMksys*.</span><span class="sxs-lookup"><span data-stu-id="2514a-113">Class monikers may be identified through [**IMoniker::IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), which returns MKSYS\_CLASSMONIKER in *pdwMksys*.</span></span>

<span data-ttu-id="2514a-114">Normalmente, los programadores crean monikers de clase mediante la función [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) o a través de [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname).</span><span class="sxs-lookup"><span data-stu-id="2514a-114">Programmers typically create class monikers using the [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) function or through [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname).</span></span> <span data-ttu-id="2514a-115">(Consulte [**IMoniker::P arsedisplayname**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="2514a-115">(See [**IMoniker::ParseDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) for details.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="2514a-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2514a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2514a-117">Anti-monikers</span><span class="sxs-lookup"><span data-stu-id="2514a-117">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="2514a-118">Monikers compuestos</span><span class="sxs-lookup"><span data-stu-id="2514a-118">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="2514a-119">Monikers de archivo</span><span class="sxs-lookup"><span data-stu-id="2514a-119">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="2514a-120">Monikers de elemento</span><span class="sxs-lookup"><span data-stu-id="2514a-120">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="2514a-121">Monikers de puntero</span><span class="sxs-lookup"><span data-stu-id="2514a-121">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




