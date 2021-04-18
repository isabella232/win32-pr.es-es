---
description: Control de errores de administración de COM+
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: Control de errores de administración de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e5838d7fee7616a23f5e361df1aef65421492
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714841"
---
# <a name="handling-com-administration-errors"></a><span data-ttu-id="a3ca0-103">Control de errores de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="a3ca0-103">Handling COM+ Administration Errors</span></span>

<span data-ttu-id="a3ca0-104">Los errores que se generan al usar los objetos COMAdmin se informan de dos maneras, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="a3ca0-104">Errors that are generated when using the COMAdmin objects are reported in two ways, as follows:</span></span>

-   <span data-ttu-id="a3ca0-105">Usar códigos de error específicos de la biblioteca COMAdmin.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-105">Using error codes specific to the COMAdmin library.</span></span>
-   <span data-ttu-id="a3ca0-106">Uso de información de error extendida disponible en una colección de [**errorInfo**](errorinfo.md) especial.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-106">Using extended error information available in a special [**ErrorInfo**](errorinfo.md) collection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a3ca0-107">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a3ca0-107">Error Codes</span></span>

<span data-ttu-id="a3ca0-108">Los códigos de error de administración se administran como cualquier otro mensaje de error COM.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-108">You handle administration error codes as you would any COM error message.</span></span> <span data-ttu-id="a3ca0-109">En Microsoft Visual C++, estos códigos se devuelven como valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a3ca0-109">In Microsoft Visual C++, these codes are returned as **HRESULT** values.</span></span> <span data-ttu-id="a3ca0-110">En Microsoft Visual Basic, se producen como excepciones que se pueden detectar.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-110">In Microsoft Visual Basic, they are thrown as exceptions that you can catch.</span></span> <span data-ttu-id="a3ca0-111">En el caso de los programadores de C++, los códigos de error de administración de COM+ se definen en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-111">For C++ programmers, the COM+ administration error codes are defined in Winerror.h.</span></span> <span data-ttu-id="a3ca0-112">Para los programadores de Visual Basic, están disponibles a través del IDE de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-112">For Visual Basic programmers, they are available through the Visual Basic IDE.</span></span>

## <a name="errorinfo-collection"></a><span data-ttu-id="a3ca0-113">Colección ErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a3ca0-113">ErrorInfo Collection</span></span>

<span data-ttu-id="a3ca0-114">Cuando se produce un error, señalado por algún tipo de código de error, puede estar disponible información más detallada, dependiendo de la naturaleza del error.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-114">When an error occurs, signaled by some kind of failure code, more detailed information may be available, depending on the nature of the error.</span></span> <span data-ttu-id="a3ca0-115">Los objetos COMAdmin proporcionan información extendida en las circunstancias en las que es difícil determinar la causa exacta del error sin un informe detallado, como con varias operaciones de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-115">The COMAdmin objects provide extended information in circumstances where the precise cause of the failure is difficult to determine without a detailed report, such as with multiple read and write operations.</span></span>

<span data-ttu-id="a3ca0-116">Por ejemplo, si usa métodos como [**rellenar**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) y [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en un objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , puede leer o escribir datos para cada elemento de la colección.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-116">For example, when you use methods such as [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on a [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, you can be reading or writing data for every item in the collection.</span></span> <span data-ttu-id="a3ca0-117">Pueden producirse errores complicados y pueden ser difíciles de diagnosticar en función de un solo código de error numérico.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-117">Complicated errors can occur, and they can be difficult to diagnose based on a single numeric error code.</span></span> <span data-ttu-id="a3ca0-118">Por lo tanto, la biblioteca COMAdmin crea información de error extendida a través de una colección especial.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-118">Therefore, the COMAdmin Library makes extended error information through a special collection.</span></span>

<span data-ttu-id="a3ca0-119">Cuando la información de error extendida está disponible, se coloca en la colección [**errorInfo**](errorinfo.md) que está relacionada con la colección original que tuvo el error.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-119">When extended error information is available, it is placed in the [**ErrorInfo**](errorinfo.md) collection that is related to the original collection that had the error.</span></span> <span data-ttu-id="a3ca0-120">Para recuperar el informe de errores, obtenga la colección **errorInfo** relacionada con la colección original y examine los elementos que contiene.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-120">To retrieve the error report, get the **ErrorInfo** collection that is related to the original collection and examine the items it contains.</span></span> <span data-ttu-id="a3ca0-121">Puede recuperar la colección **errorInfo** mediante [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) en [**COMAdminCatalogCollection**](comadmincatalogcollection.md), y dejar el segundo parámetro en blanco, donde normalmente especificaría la propiedad clave de un elemento primario.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-121">You can retrieve the **ErrorInfo** collection by using [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) on [**COMAdminCatalogCollection**](comadmincatalogcollection.md), leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

<span data-ttu-id="a3ca0-122">Cuando se produce un error, debe obtener y rellenar inmediatamente la colección [**errorInfo**](errorinfo.md) para la colección en la que se produjo un error, sin realizar ninguna otra operación en esa colección.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-122">When you get an error, you must immediately get and populate the [**ErrorInfo**](errorinfo.md) collection for the collection that failed, without performing any other operations on that collection.</span></span> <span data-ttu-id="a3ca0-123">De lo contrario, se restablece la colección **errorInfo** y no se detalla ese error.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-123">Otherwise, the **ErrorInfo** collection is reset and does not detail that failure.</span></span>

<span data-ttu-id="a3ca0-124">Los elementos de la colección [**errorInfo**](errorinfo.md) exponen las propiedades de informes de errores especiales MajorRef y MinorRef, que detallan la causa concreta del error.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-124">The items in the [**ErrorInfo**](errorinfo.md) collection expose the special error-reporting properties MajorRef and MinorRef, which detail the particular cause of the error.</span></span> <span data-ttu-id="a3ca0-125">Para obtener más información, consulte **errorInfo**.</span><span class="sxs-lookup"><span data-stu-id="a3ca0-125">For more information, see **ErrorInfo**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3ca0-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3ca0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3ca0-127">Operaciones de administración de COM+ en transacciones</span><span class="sxs-lookup"><span data-stu-id="a3ca0-127">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="a3ca0-128">Ejemplo introductorio con el catálogo de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="a3ca0-128">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="a3ca0-129">Información general de los objetos COMAdmin</span><span class="sxs-lookup"><span data-stu-id="a3ca0-129">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="a3ca0-130">Recuperar recopilaciones en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="a3ca0-130">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="a3ca0-131">Establecer propiedades y guardar cambios en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="a3ca0-131">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



