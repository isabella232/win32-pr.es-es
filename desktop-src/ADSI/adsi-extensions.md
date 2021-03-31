---
title: Extensiones ADSI
description: Una extensión ADSI es un objeto COM especial que permite a los programadores extender un objeto ADSI.
ms.assetid: 3e40e702-089a-4d2a-806c-cd5b29d11bfd
ms.tgt_platform: multiple
keywords:
- Extensiones ADSI
- ADSI ADSI, usar extensiones
- ADSI de extensiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3852e64ad282c11ecd17c6b13904738ee7f46a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075087"
---
# <a name="adsi-extensions"></a><span data-ttu-id="d348d-106">Extensiones ADSI</span><span class="sxs-lookup"><span data-stu-id="d348d-106">ADSI Extensions</span></span>

<span data-ttu-id="d348d-107">Una extensión ADSI es un objeto COM especial que permite a los programadores extender un objeto ADSI.</span><span class="sxs-lookup"><span data-stu-id="d348d-107">An ADSI extension is a special COM object that enable a developer to extend an ADSI object.</span></span> <span data-ttu-id="d348d-108">Cada extensión está asociada a una clase especificada en el directorio.</span><span class="sxs-lookup"><span data-stu-id="d348d-108">Each extension is associated with a specified class in the directory.</span></span> <span data-ttu-id="d348d-109">Con este modelo de extensión, los desarrolladores pueden agregar métodos para dar un significado más dinámico a un objeto.</span><span class="sxs-lookup"><span data-stu-id="d348d-109">With this extension model, developers can add methods to give more dynamic meaning to an object.</span></span> <span data-ttu-id="d348d-110">En un modelo de programación de directorios tradicional, se obtiene acceso a un objeto mediante la obtención y configuración de los atributos del objeto.</span><span class="sxs-lookup"><span data-stu-id="d348d-110">In a traditional directory programming model, an object is accessed by getting and setting the object attributes.</span></span> <span data-ttu-id="d348d-111">Con las extensiones ADSI, puede agregar más características a un objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="d348d-111">Using ADSI extensions, you can add more features to a directory object.</span></span>

<span data-ttu-id="d348d-112">En esta sección se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="d348d-112">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="d348d-113">Ventajas del uso de las extensiones ADSI</span><span class="sxs-lookup"><span data-stu-id="d348d-113">Benefits of Using ADSI Extensions</span></span>](benefits-of-using-adsi-extensions.md)
-   [<span data-ttu-id="d348d-114">Arquitectura de extensión ADSI</span><span class="sxs-lookup"><span data-stu-id="d348d-114">ADSI Extension Architecture</span></span>](adsi-extension-architecture.md)
-   [<span data-ttu-id="d348d-115">Cómo integra ADSI Extensions</span><span class="sxs-lookup"><span data-stu-id="d348d-115">How ADSI Integrates Extensions</span></span>](adsi-and-extensions.md)
-   [<span data-ttu-id="d348d-116">¿Qué ve un cliente?</span><span class="sxs-lookup"><span data-stu-id="d348d-116">What Does a Client See?</span></span>](what-does-a-client-see.md)
-   [<span data-ttu-id="d348d-117">Obtención de interfaces ADSI de la extensión</span><span class="sxs-lookup"><span data-stu-id="d348d-117">Getting ADSI Interfaces From Your Extension</span></span>](getting-adsi-interfaces-from-your-extension.md)
-   [<span data-ttu-id="d348d-118">Bibliotecas de tipos de extensiones ADSI</span><span class="sxs-lookup"><span data-stu-id="d348d-118">ADSI Extension Type Libraries</span></span>](adsi-extension-type-libraries.md)
-   [<span data-ttu-id="d348d-119">Compatibilidad con enlaces tempranas</span><span class="sxs-lookup"><span data-stu-id="d348d-119">Early Binding Support</span></span>](early-binding-support.md)
-   [<span data-ttu-id="d348d-120">Compatibilidad con enlace en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="d348d-120">Late Binding Support</span></span>](late-binding-support.md)
-   [<span data-ttu-id="d348d-121">Interfaz IADsExtension</span><span class="sxs-lookup"><span data-stu-id="d348d-121">IADsExtension Interface</span></span>](iadsextension-interface.md)
-   [<span data-ttu-id="d348d-122">Compatibilidad con interfaces duales o de distribución</span><span class="sxs-lookup"><span data-stu-id="d348d-122">Supporting Dual or Dispatch Interfaces</span></span>](supporting-dual-or-dispatch-interfaces.md)
-   [<span data-ttu-id="d348d-123">Revisar las reglas de agregación COM con extensiones ADSI</span><span class="sxs-lookup"><span data-stu-id="d348d-123">Revisiting COM Aggregation Rules with ADSI Extensions</span></span>](revisiting-com-aggregation-rules-with-adsi-extensions.md)
-   [<span data-ttu-id="d348d-124">Resolución de varios componentes de agregación que admiten la misma interfaz</span><span class="sxs-lookup"><span data-stu-id="d348d-124">Resolution of Multiple Aggregation Components Supporting the Same Interface</span></span>](resolution-of-multiple-aggregation-components-supporting-the-same-interface.md)
-   [<span data-ttu-id="d348d-125">Resolución de conflictos de nombres de función y propiedad en la automatización en extensiones</span><span class="sxs-lookup"><span data-stu-id="d348d-125">Resolution of Function/Property Name Conflicts in Automation in Extensions</span></span>](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md)

 

 




