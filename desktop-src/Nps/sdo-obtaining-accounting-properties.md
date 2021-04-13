---
title: Obtención de propiedades de cuentas
description: El objeto Accounting es uno de los objetos de la colección de controladores de solicitud.
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9911397c1de3521ccb5a275405416d8b88c1fa6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420993"
---
# <a name="obtaining-accounting-properties"></a><span data-ttu-id="d275e-103">Obtención de propiedades de cuentas</span><span class="sxs-lookup"><span data-stu-id="d275e-103">Obtaining Accounting Properties</span></span>

> [!Note]  
> <span data-ttu-id="d275e-104">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d275e-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="d275e-105">El contenido de este tema se aplica a IAS y NPS.</span><span class="sxs-lookup"><span data-stu-id="d275e-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="d275e-106">En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.</span><span class="sxs-lookup"><span data-stu-id="d275e-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="d275e-107">El objeto Accounting es uno de los objetos de la colección de controladores de solicitud.</span><span class="sxs-lookup"><span data-stu-id="d275e-107">The accounting object is one of the objects in the Request Handlers collection.</span></span> <span data-ttu-id="d275e-108">El valor de enumeración para la colección de controladores de solicitud es la propiedad de la **\_ \_ \_ colección RequestHandler de IAS**.</span><span class="sxs-lookup"><span data-stu-id="d275e-108">The enumeration value for the request handlers collection is **PROPERTY\_IAS\_REQUESTHANDLERS\_COLLECTION**.</span></span> <span data-ttu-id="d275e-109">El nombre del controlador para el objeto Accounting es "Microsoft Accounting".</span><span class="sxs-lookup"><span data-stu-id="d275e-109">The name of the handler for the accounting object is "Microsoft Accounting".</span></span>

<span data-ttu-id="d275e-110">El código Visual Basic siguiente tiene acceso a las propiedades disponibles desde el controlador de objetos de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="d275e-110">The following Visual Basic code accesses the properties available from the accounting object handler.</span></span>


```VB
Set sdoRequestHandler = sdoCollRequestHandlers.Item("Microsoft Accounting")
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_AUTHENTICATION)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE)
```



<span data-ttu-id="d275e-111">Para obtener acceso a las propiedades de cuentas mediante C++, primero obtenga la colección de controladores de solicitud.</span><span class="sxs-lookup"><span data-stu-id="d275e-111">To access the accounting properties using C++, first obtain the request handlers collection.</span></span> <span data-ttu-id="d275e-112">La [recuperación de una colección](/windows/desktop/Nps/sdo-retrieving-a-collection) contiene código de C++ que muestra cómo obtener una colección.</span><span class="sxs-lookup"><span data-stu-id="d275e-112">The [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection) contains C++ code that demonstrates how to obtain a collection.</span></span> <span data-ttu-id="d275e-113">El valor de enumeración para la colección de controladores de solicitud es la propiedad de la **\_ \_ \_ colección RequestHandler de IAS**.</span><span class="sxs-lookup"><span data-stu-id="d275e-113">The enumeration value for the request handlers collection is **PROPERTY\_IAS\_REQUESTHANDLERS\_COLLECTION**.</span></span> <span data-ttu-id="d275e-114">(Los valores correspondientes a las distintas colecciones de NPS se enumeran mediante el tipo de enumeración [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) ).</span><span class="sxs-lookup"><span data-stu-id="d275e-114">(The values corresponding to the various NPS collections are enumerated by the [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumeration type.)</span></span>

<span data-ttu-id="d275e-115">La colección de controladores de solicitud contiene un objeto denominado "Microsoft Accounting".</span><span class="sxs-lookup"><span data-stu-id="d275e-115">The request handlers collection contains an object named "Microsoft Accounting".</span></span> <span data-ttu-id="d275e-116">Recupere este objeto de la colección.</span><span class="sxs-lookup"><span data-stu-id="d275e-116">Retrieve this object from the collection.</span></span> <span data-ttu-id="d275e-117">La sección [recuperar un objeto de una colección](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contiene código de C++ que muestra cómo obtener un objeto de una colección.</span><span class="sxs-lookup"><span data-stu-id="d275e-117">The section [Retrieving an Object from a Collection](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contains C++ code that demonstrates how to obtain an object from a collection.</span></span>

<span data-ttu-id="d275e-118">Una vez que tenga el objeto de contabilidad de Microsoft, obtenga una interfaz [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) para el objeto mediante [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="d275e-118">Once you have the Microsoft Accounting object, obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface for the object using [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="d275e-119">La sección [recuperar un SDO de usuarios](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contiene código de C++ que muestra cómo obtener una interfaz **ISdo** para un objeto.</span><span class="sxs-lookup"><span data-stu-id="d275e-119">The section [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contains C++ code that demonstrates how obtain an **ISdo** interface for an object.</span></span> <span data-ttu-id="d275e-120">Después, puede usar el método [**ISdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) para obtener los valores de propiedad para el objeto de contabilidad de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d275e-120">You can then use the [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) method to obtain property values for the Microsoft Accounting object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d275e-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d275e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d275e-122">Recuperación de una colección</span><span class="sxs-lookup"><span data-stu-id="d275e-122">Retrieving a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[<span data-ttu-id="d275e-123">Recuperar un objeto de una colección</span><span class="sxs-lookup"><span data-stu-id="d275e-123">Retrieving an Object from a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[<span data-ttu-id="d275e-124">Recuperación de un SDO de usuarios</span><span class="sxs-lookup"><span data-stu-id="d275e-124">Retrieving a User SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[<span data-ttu-id="d275e-125">**ISdo**</span><span class="sxs-lookup"><span data-stu-id="d275e-125">**ISdo**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

<span data-ttu-id="d275e-126">[**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="d275e-126">[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
</dt> <dt>

[<span data-ttu-id="d275e-127">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="d275e-127">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 