---
description: Obtiene la información necesaria para leer o guardar las propiedades en el contenedor de propiedades. La interfaz IItemPropertyBag solo se admite en Windows XP y Windows Server 2003, y ya no debe usarse.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: 'IItemPropertyBag:: GetPropertyInfo (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.GetPropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: a64b064c6c6d3708edc353db136fcad599d14adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714997"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a><span data-ttu-id="9c0cc-104">IItemPropertyBag:: GetPropertyInfo (método)</span><span class="sxs-lookup"><span data-stu-id="9c0cc-104">IItemPropertyBag::GetPropertyInfo method</span></span>

<span data-ttu-id="9c0cc-105">Obtiene la información necesaria para leer o guardar las propiedades en el contenedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-105">Gets the information required to read or save the properties in the property bag.</span></span> <span data-ttu-id="9c0cc-106">La interfaz [**IItemPropertyBag**](iitempropertybag.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c0cc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c0cc-107">Syntax</span></span>


```C++
HRESULT GetPropertyInfo(
  [in]  ULONG    iProperty,
  [in]  ULONG    cProperties,
  [out] ITEMPROP *pPropBag,
  [out] ULONG    *pcProperties
);
```



## <a name="parameters"></a><span data-ttu-id="9c0cc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c0cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c0cc-109">*iProperty* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c0cc-109">*iProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c0cc-110">Índice de base cero de la primera propiedad para la que se solicita información.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-110">The zero-based index of the first property for which information is requested.</span></span>

</dd> <dt>

<span data-ttu-id="9c0cc-111">*cProperties* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c0cc-111">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c0cc-112">Número de propiedades para las que se va a obtener información.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-112">The number of properties to get information for.</span></span> <span data-ttu-id="9c0cc-113">Este argumento especifica el número de elementos de matriz en *pPropBag*.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-113">This argument specifies the number of array elements in *pPropBag*.</span></span>

</dd> <dt>

<span data-ttu-id="9c0cc-114">*pPropBag* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9c0cc-114">*pPropBag* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c0cc-115">Puntero a una matriz de estructuras [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que recibe la información de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-115">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that receives the information for the properties.</span></span>

</dd> <dt>

<span data-ttu-id="9c0cc-116">*pcProperties* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9c0cc-116">*pcProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c0cc-117">Recibe un puntero a una variable **ULong** que recibe el número de propiedades para las que se recuperó la información.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-117">Receives a pointer to a **ULONG** variable that receives the number of properties for which information was retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c0cc-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c0cc-118">Return value</span></span>

<span data-ttu-id="9c0cc-119">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="9c0cc-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9c0cc-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c0cc-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c0cc-121">Remarks</span></span>

<span data-ttu-id="9c0cc-122">La interfaz [**IItemPropertyBag**](iitempropertybag.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-122">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="9c0cc-123">Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**IItemPropertyBag**](iitempropertybag.md) y las siguientes API: las interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) y [**ISearchItem**](-search-isearchitem.md) , las estructuras [**LINKINFO**](-search-linkinfo.md) y [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) y la enumeración [**LINKTYPE**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="9c0cc-123">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c0cc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c0cc-124">Requirements</span></span>



| <span data-ttu-id="9c0cc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c0cc-125">Requirement</span></span> | <span data-ttu-id="9c0cc-126">Value</span><span class="sxs-lookup"><span data-stu-id="9c0cc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9c0cc-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c0cc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9c0cc-128">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c0cc-128">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9c0cc-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c0cc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9c0cc-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c0cc-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9c0cc-131">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="9c0cc-131">Redistributable</span></span><br/>          | <span data-ttu-id="9c0cc-132">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="9c0cc-132">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="9c0cc-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c0cc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c0cc-134">**IItemPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="9c0cc-134">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




