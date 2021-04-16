---
description: Permite que el filtro de procesamiento de imágenes escriba las propiedades de nuevo en el controlador (y en el dispositivo).
ms.assetid: b9bb8d81-2945-46ba-a0a2-7009000574aa
title: 'IWiaImageFilter:: ApplyProperties (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.ApplyProperties
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3c20527ee587b975adea34e7c480349836620015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716050"
---
# <a name="iwiaimagefilterapplyproperties-method"></a><span data-ttu-id="d9139-103">IWiaImageFilter:: ApplyProperties (método)</span><span class="sxs-lookup"><span data-stu-id="d9139-103">IWiaImageFilter::ApplyProperties method</span></span>

<span data-ttu-id="d9139-104">Permite que el filtro de procesamiento de imágenes escriba las propiedades de nuevo en el controlador (y en el dispositivo).</span><span class="sxs-lookup"><span data-stu-id="d9139-104">Enables the image processing filter to write properties back to the driver (and device).</span></span>

## <a name="syntax"></a><span data-ttu-id="d9139-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9139-105">Syntax</span></span>


```C++
HRESULT ApplyProperties(
  [in] IWiaPropertyStorage *pWiaPropertyStorage
);
```



## <a name="parameters"></a><span data-ttu-id="d9139-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9139-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9139-107">*pWiaPropertyStorage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d9139-107">*pWiaPropertyStorage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9139-108">Tipo: \**[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) \** _</span><span class="sxs-lookup"><span data-stu-id="d9139-108">Type: \**[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)\** _</span></span>

<span data-ttu-id="d9139-109">Especifica un puntero a [_ *IWiaPropertyStorage* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para las propiedades que se van a aplicar.</span><span class="sxs-lookup"><span data-stu-id="d9139-109">Specifies a pointer to the [_ *IWiaPropertyStorage*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) for the properties to be applied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9139-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9139-110">Return value</span></span>

<span data-ttu-id="d9139-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d9139-111">Type: **HRESULT**</span></span>

<span data-ttu-id="d9139-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d9139-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d9139-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d9139-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9139-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9139-114">Remarks</span></span>

<span data-ttu-id="d9139-115">No llame a este método directamente desde su aplicación.</span><span class="sxs-lookup"><span data-stu-id="d9139-115">Do not call this method directly from your application.</span></span> <span data-ttu-id="d9139-116">Lo llama la adquisición de imágenes de Windows (WIA) 2,0 después de que el filtro de procesamiento de imágenes haya procesado los datos sin procesar.</span><span class="sxs-lookup"><span data-stu-id="d9139-116">It is called by Windows Image Acquisition (WIA) 2.0 after the image processing filter has processed the raw data.</span></span>

<span data-ttu-id="d9139-117">*pWiaPropertyStorage* es la interfaz de [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) en la que el filtro de procesamiento de imágenes debe escribir propiedades.</span><span class="sxs-lookup"><span data-stu-id="d9139-117">*pWiaPropertyStorage* is the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface into which the image processing filter should write properties.</span></span> <span data-ttu-id="d9139-118">Un filtro de procesamiento de imágenes solo debe usar el método [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) para escribir propiedades.</span><span class="sxs-lookup"><span data-stu-id="d9139-118">An image processing filter should use only the [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) method to write properties.</span></span>

<span data-ttu-id="d9139-119">Este método permite que el filtro de procesamiento de imágenes escriba las propiedades de nuevo en el controlador (y en el dispositivo).</span><span class="sxs-lookup"><span data-stu-id="d9139-119">This method allows the image processing filter to write properties back to the driver (and device).</span></span> <span data-ttu-id="d9139-120">Esto puede ser necesario para los filtros que implementan características como la exposición automática durante el análisis de la película.</span><span class="sxs-lookup"><span data-stu-id="d9139-120">This may be necessary for filters that implement features such as auto-exposure during film scanning.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9139-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9139-121">Requirements</span></span>



| <span data-ttu-id="d9139-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9139-122">Requirement</span></span> | <span data-ttu-id="d9139-123">Value</span><span class="sxs-lookup"><span data-stu-id="d9139-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d9139-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9139-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d9139-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d9139-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d9139-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9139-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d9139-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9139-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d9139-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9139-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9139-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9139-129"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="d9139-130">IDL</span><span class="sxs-lookup"><span data-stu-id="d9139-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d9139-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d9139-131"><dt>Wia.idl</dt></span></span> </dl> |



 

 
