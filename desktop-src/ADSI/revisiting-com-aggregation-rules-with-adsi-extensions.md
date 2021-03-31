---
title: Revisar las reglas de agregación COM con extensiones ADSI
description: La siguiente es una breve revisión de las reglas de agregación de COM y de extensión ADSI.
ms.assetid: 3efcdfcf-4965-4436-90b2-dc0f627c71b4
ms.tgt_platform: multiple
keywords:
- Extensiones ADSI, reglas de agregación COM
- Agregación de COM ADSI
- Revisar las reglas de agregación COM con ADSI Extensions ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9b3e3614c4adc225883f120f8fbf362df3e646
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793845"
---
# <a name="revisiting-com-aggregation-rules-with-adsi-extensions"></a><span data-ttu-id="b7036-106">Revisar las reglas de agregación COM con extensiones ADSI</span><span class="sxs-lookup"><span data-stu-id="b7036-106">Revisiting COM Aggregation Rules with ADSI Extensions</span></span>

<span data-ttu-id="b7036-107">La siguiente es una breve revisión de las reglas de agregación de COM y de extensión ADSI.</span><span class="sxs-lookup"><span data-stu-id="b7036-107">The following is a brief review of COM aggregation and ADSI extension rules.</span></span>

-   <span data-ttu-id="b7036-108">El método **CreateInstance** devuelve un puntero a una interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , como se indica a continuación, que no delega ninguna llamada de función al agregador.</span><span class="sxs-lookup"><span data-stu-id="b7036-108">The **CreateInstance** method returns a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface, as follows, that does not delegate any function calls to the aggregator.</span></span>

    <span data-ttu-id="b7036-109">El método [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) devuelve punteros a las interfaces que admite y errores para las interfaces que no admite.</span><span class="sxs-lookup"><span data-stu-id="b7036-109">The [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method returns pointers to the interfaces that it supports, and errors for interfaces it does not support.</span></span>

    <span data-ttu-id="b7036-110">El método [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrementa el recuento de referencias en el propio objeto de extensión agregado.</span><span class="sxs-lookup"><span data-stu-id="b7036-110">The [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method increments the reference count on the aggregated extension object itself.</span></span>

    <span data-ttu-id="b7036-111">El método [**IUnkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) reduce el recuento de referencias en el propio objeto de extensión agregado y se destruye cuando el recuento de referencias es 0.</span><span class="sxs-lookup"><span data-stu-id="b7036-111">The [**IUnkown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method decrements the reference count on the aggregated extension object itself and destroys itself when the reference count is 0.</span></span>

-   <span data-ttu-id="b7036-112">El objeto de extensión debe almacenar el puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del agregador, como m \_ pOuterUnknown, durante la implementación del método **CreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="b7036-112">The extension object should store the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer of the aggregator, such as m\_pOuterUnknown, during the implementation of the **CreateInstance** method.</span></span>
-   <span data-ttu-id="b7036-113">Todas las interfaces que admite el objeto de extensión, incluido [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), deben heredar de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), que delega de nuevo todas las llamadas de función al agregador.</span><span class="sxs-lookup"><span data-stu-id="b7036-113">All interfaces that the extension object supports, including [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), should inherit from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), which delegates all function calls back to the aggregator.</span></span>
    -   <span data-ttu-id="b7036-114">[**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) llama a "m \_ POuterUnknown->QueryInterface"</span><span class="sxs-lookup"><span data-stu-id="b7036-114">[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) calls "m\_pOuterUnknown->QueryInterface"</span></span>
    -   <span data-ttu-id="b7036-115">[**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) llama a "m \_ POuterUnknown->AddRef"</span><span class="sxs-lookup"><span data-stu-id="b7036-115">[**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) calls "m\_pOuterUnknown->AddRef"</span></span>
    -   <span data-ttu-id="b7036-116">[**IUnkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) llama a "m \_ POuterUnknown->versión"</span><span class="sxs-lookup"><span data-stu-id="b7036-116">[**IUnkown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) calls "m\_pOuterUnknown->Release"</span></span>

<span data-ttu-id="b7036-117">Los escritores de extensiones pueden elegir cualquier implementación interna que prefieran, siempre y cuando cumplan las reglas de agregación COM estándar.</span><span class="sxs-lookup"><span data-stu-id="b7036-117">Extension writers can choose any internal implementation they prefer as long as they obey standard COM aggregation rules.</span></span> <span data-ttu-id="b7036-118">Tenga en cuenta que no es necesario que un objeto de extensión funcione como un objeto independiente.</span><span class="sxs-lookup"><span data-stu-id="b7036-118">Be aware that an extension object does not have to work as a standalone object.</span></span> <span data-ttu-id="b7036-119">Las extensiones están diseñadas para funcionar como agregados.</span><span class="sxs-lookup"><span data-stu-id="b7036-119">Extensions are designed to work as aggregates.</span></span> <span data-ttu-id="b7036-120">Sin embargo, se puede escribir una extensión para que funcione como un objeto independiente y como agregado.</span><span class="sxs-lookup"><span data-stu-id="b7036-120">However, an extension can be written to work as both a standalone object and as an aggregate.</span></span>

<span data-ttu-id="b7036-121">Además de la compatibilidad con la agregación COM estándar, un objeto de extensión puede admitir [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para las características más avanzadas.</span><span class="sxs-lookup"><span data-stu-id="b7036-121">In addition to standard COM aggregation support, an extension object may support [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) for more advanced features.</span></span> <span data-ttu-id="b7036-122">Si se admite el enlace en tiempo de ejecución, la extensión debe:</span><span class="sxs-lookup"><span data-stu-id="b7036-122">If late binding is supported, the extension should:</span></span>

-   <span data-ttu-id="b7036-123">Delegar funciones para [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) de nuevo al agregador.</span><span class="sxs-lookup"><span data-stu-id="b7036-123">Delegate functions for [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) back to the aggregator.</span></span>
-   <span data-ttu-id="b7036-124">Implemente la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) en [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="b7036-124">Implement the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface in [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>

 

 