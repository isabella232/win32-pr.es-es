---
description: 'Cuando una aplicación realiza una operación IPropertyStorage:: WriteMultiple en cualquier propiedad de adquisición de imagen de Windows (WIA) grabable, el controlador WIA realiza una validación en el nuevo valor de propiedad.'
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: Validación de propiedades de WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60d9e64122e19249c19bc47564631162d783920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275446"
---
# <a name="wia-property-validation"></a><span data-ttu-id="6ce1d-103">Validación de propiedades de WIA</span><span class="sxs-lookup"><span data-stu-id="6ce1d-103">WIA Property Validation</span></span>

<span data-ttu-id="6ce1d-104">Cuando una aplicación realiza una operación [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) en cualquier propiedad de adquisición de imagen de Windows (WIA) grabable, el controlador WIA realiza una validación en el nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6ce1d-104">When an application performs an [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) operation on any writeable Windows Image Acquisition (WIA) property, the WIA driver performs a validation on the new property value.</span></span> <span data-ttu-id="6ce1d-105">La escritura de una propiedad puede tener efectos secundarios que cambien otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6ce1d-105">Writing one property may have side affects that change other property values.</span></span> <span data-ttu-id="6ce1d-106">Depende de la aplicación leer todos los valores de propiedad después de una operación de escritura para determinar que todas las propiedades se establecen en los valores que desea la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6ce1d-106">It is up to the application to read all property values after a write operation to determine that all properties are set to values the application desires.</span></span>

<span data-ttu-id="6ce1d-107">Se pueden escribir varias propiedades simultáneamente mediante la operación [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) .</span><span class="sxs-lookup"><span data-stu-id="6ce1d-107">Multiple properties can be written simultaneously using the [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) operation.</span></span> <span data-ttu-id="6ce1d-108">Puede haber casos en los que algunas asignaciones de propiedad estén en conflicto.</span><span class="sxs-lookup"><span data-stu-id="6ce1d-108">There may be cases where some property assignments conflict.</span></span> <span data-ttu-id="6ce1d-109">En estos casos, la prioridad usada para resolver conflictos es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="6ce1d-109">In such cases, the priority used to resolve conflicts is as follows:</span></span>

1.  <span data-ttu-id="6ce1d-110">\_intención del \_ CUR de IPS de WIA \_</span><span class="sxs-lookup"><span data-stu-id="6ce1d-110">WIA\_IPS\_CUR\_INTENT</span></span>
2.  <span data-ttu-id="6ce1d-111">tipo de DataType del \_ IPA de WIA \_</span><span class="sxs-lookup"><span data-stu-id="6ce1d-111">WIA\_IPA\_DATATYPE</span></span>
3.  <span data-ttu-id="6ce1d-112">\_profundidad de IPA de WIA \_</span><span class="sxs-lookup"><span data-stu-id="6ce1d-112">WIA\_IPA\_DEPTH</span></span>
4.  <span data-ttu-id="6ce1d-113">\_XRES de IP WIA \_</span><span class="sxs-lookup"><span data-stu-id="6ce1d-113">WIA\_IPS\_XRES</span></span>
5.  <span data-ttu-id="6ce1d-114">\_YRES de IP WIA \_</span><span class="sxs-lookup"><span data-stu-id="6ce1d-114">WIA\_IPS\_YRES</span></span>
6.  <span data-ttu-id="6ce1d-115">IP de WIA ( \_ \_ XPOS)</span><span class="sxs-lookup"><span data-stu-id="6ce1d-115">WIA\_IPS\_XPOS</span></span>
7.  <span data-ttu-id="6ce1d-116">WIA \_ IP \_ YPOS</span><span class="sxs-lookup"><span data-stu-id="6ce1d-116">WIA\_IPS\_YPOS</span></span>
8.  <span data-ttu-id="6ce1d-117">\_XEXTENT de IP WIA \_</span><span class="sxs-lookup"><span data-stu-id="6ce1d-117">WIA\_IPS\_XEXTENT</span></span>
9.  <span data-ttu-id="6ce1d-118">\_YEXTENT de IP WIA \_</span><span class="sxs-lookup"><span data-stu-id="6ce1d-118">WIA\_IPS\_YEXTENT</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ce1d-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ce1d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ce1d-120">**IWiaPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="6ce1d-120">**IWiaPropertyStorage**</span></span>](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
