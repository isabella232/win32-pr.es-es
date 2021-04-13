---
description: Hace que una o más propiedades se lean del contenedor de propiedades. La interfaz IItemPropertyBag solo se admite en Windows XP y Windows Server 2003, y ya no debe usarse.
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: 'IItemPropertyBag:: Read (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: ef7af13dc42239a2823d7e7ca9b8def4748519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360187"
---
# <a name="iitempropertybagread-method"></a><span data-ttu-id="44fb3-104">IItemPropertyBag:: Read (método)</span><span class="sxs-lookup"><span data-stu-id="44fb3-104">IItemPropertyBag::Read method</span></span>

<span data-ttu-id="44fb3-105">Hace que una o más propiedades se lean del contenedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="44fb3-105">Causes one or more properties to be read from the property bag.</span></span> <span data-ttu-id="44fb3-106">La interfaz [**IItemPropertyBag**](iitempropertybag.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="44fb3-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="44fb3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44fb3-107">Syntax</span></span>


```C++
HRESULT Read(
  [in]  ULONG    cProperties,
  [in]  ITEMPROP *pPropBag,
  [out] VARIANT  *pvarValue,
  [out] HRESULT  *phrError
);
```



## <a name="parameters"></a><span data-ttu-id="44fb3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44fb3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44fb3-109">*cProperties* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="44fb3-109">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44fb3-110">Número de propiedades que se van a leer.</span><span class="sxs-lookup"><span data-stu-id="44fb3-110">The number of properties to read.</span></span> <span data-ttu-id="44fb3-111">Este argumento especifica el número de elementos de las matrices en *pPropBag*, *pvarValue* y *phrError*.</span><span class="sxs-lookup"><span data-stu-id="44fb3-111">This argument specifies the number of elements in the arrays at *pPropBag*, *pvarValue*, and *phrError*.</span></span>

</dd> <dt>

<span data-ttu-id="44fb3-112">*pPropBag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="44fb3-112">*pPropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44fb3-113">Puntero a una matriz de estructuras [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que especifica las propiedades que se solicitan.</span><span class="sxs-lookup"><span data-stu-id="44fb3-113">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that specifies the properties that are requested.</span></span>

</dd> <dt>

<span data-ttu-id="44fb3-114">*pvarValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="44fb3-114">*pvarValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44fb3-115">Recibe un puntero que devuelve una matriz de estructuras **variantes** que recibe los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="44fb3-115">Receives a pointer that returns an array of **VARIANT** structures that receives the property values.</span></span>

</dd> <dt>

<span data-ttu-id="44fb3-116">*phrError* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="44fb3-116">*phrError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44fb3-117">Puntero a una matriz de valores **HRESULT** que recibe el resultado de cada lectura de propiedad.</span><span class="sxs-lookup"><span data-stu-id="44fb3-117">Pointer to an array of **HRESULT** values that receives the result of each property read.</span></span> <span data-ttu-id="44fb3-118">Debe haber al menos *cProperties* elementos en esta matriz.</span><span class="sxs-lookup"><span data-stu-id="44fb3-118">There must be at least *cProperties* elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44fb3-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44fb3-119">Return value</span></span>

<span data-ttu-id="44fb3-120">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="44fb3-120">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="44fb3-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="44fb3-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="44fb3-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44fb3-122">Remarks</span></span>

<span data-ttu-id="44fb3-123">La interfaz [**IItemPropertyBag**](iitempropertybag.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="44fb3-123">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="44fb3-124">Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**IItemPropertyBag**](iitempropertybag.md) y las siguientes API: las interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) y [**ISearchItem**](-search-isearchitem.md) , las estructuras [**LINKINFO**](-search-linkinfo.md) y [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) y la enumeración [**LINKTYPE**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="44fb3-124">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="44fb3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44fb3-125">Requirements</span></span>



| <span data-ttu-id="44fb3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="44fb3-126">Requirement</span></span> | <span data-ttu-id="44fb3-127">Value</span><span class="sxs-lookup"><span data-stu-id="44fb3-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="44fb3-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44fb3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="44fb3-129">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="44fb3-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="44fb3-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44fb3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="44fb3-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="44fb3-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="44fb3-132">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="44fb3-132">Redistributable</span></span><br/>          | <span data-ttu-id="44fb3-133">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="44fb3-133">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="44fb3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="44fb3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44fb3-135">**IItemPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="44fb3-135">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




