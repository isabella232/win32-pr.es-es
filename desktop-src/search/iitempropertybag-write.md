---
description: Hace que una o más propiedades se guarden en el contenedor de propiedades. La interfaz IItemPropertyBag solo se admite en Windows XP y Windows Server 2003, y ya no debe usarse.
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: 'IItemPropertyBag:: Write (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7df66487bba0c2bbef40cf3642754dff56f65835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153941"
---
# <a name="iitempropertybagwrite-method"></a><span data-ttu-id="c0054-104">IItemPropertyBag:: Write (método)</span><span class="sxs-lookup"><span data-stu-id="c0054-104">IItemPropertyBag::Write method</span></span>

<span data-ttu-id="c0054-105">Hace que una o más propiedades se guarden en el contenedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c0054-105">Causes one or more properties to be saved into the property bag.</span></span> <span data-ttu-id="c0054-106">La interfaz [**IItemPropertyBag**](iitempropertybag.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="c0054-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0054-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0054-107">Syntax</span></span>


```C++
HRESULT Write(
  [in] ULONG    cProperties,
  [in] ITEMPROP *pPropBag,
  [in] VARIANT  *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="c0054-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0054-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0054-109">*cProperties* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c0054-109">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0054-110">Número de propiedades que se van a guardar.</span><span class="sxs-lookup"><span data-stu-id="c0054-110">The number of properties to save.</span></span> <span data-ttu-id="c0054-111">Este argumento especifica el número de elementos de las matrices en *pPropBag* y *pvarValue*.</span><span class="sxs-lookup"><span data-stu-id="c0054-111">This argument specifies the number of elements in the arrays at *pPropBag* and *pvarValue*.</span></span>

</dd> <dt>

<span data-ttu-id="c0054-112">*pPropBag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c0054-112">*pPropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0054-113">Puntero a una matriz de estructuras [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que especifica las propiedades que se van a guardar.</span><span class="sxs-lookup"><span data-stu-id="c0054-113">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that specifies the properties to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="c0054-114">*pvarValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c0054-114">*pvarValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0054-115">Puntero a una **variante** cuyo tipo depende del tipo de datos de la información de propiedad que contiene.</span><span class="sxs-lookup"><span data-stu-id="c0054-115">Pointer to a **VARIANT** whose type depends on the data type of the property information that it contains.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0054-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0054-116">Return value</span></span>

<span data-ttu-id="c0054-117">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="c0054-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="c0054-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c0054-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0054-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0054-119">Remarks</span></span>

<span data-ttu-id="c0054-120">La interfaz [**IItemPropertyBag**](iitempropertybag.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="c0054-120">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="c0054-121">Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**IItemPropertyBag**](iitempropertybag.md) y las siguientes API: las interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) y [**ISearchItem**](-search-isearchitem.md) , las estructuras [**LINKINFO**](-search-linkinfo.md) y [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) y la enumeración [**LINKTYPE**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="c0054-121">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0054-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0054-122">Requirements</span></span>



| <span data-ttu-id="c0054-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0054-123">Requirement</span></span> | <span data-ttu-id="c0054-124">Value</span><span class="sxs-lookup"><span data-stu-id="c0054-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c0054-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0054-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c0054-126">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0054-126">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c0054-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0054-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c0054-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0054-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c0054-129">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="c0054-129">Redistributable</span></span><br/>          | <span data-ttu-id="c0054-130">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="c0054-130">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c0054-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0054-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0054-132">**IItemPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="c0054-132">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




