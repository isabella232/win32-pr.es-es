---
description: Obtiene el elemento primario del árbol que representa un dispositivo de hardware de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: c6fdaf1d-9875-4852-893c-813894d89f6c
title: 'IWiaItem2:: GetParentItem (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetParentItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 055625b98807103c3b79109216f6081d00564b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360332"
---
# <a name="iwiaitem2getparentitem-method"></a><span data-ttu-id="64c5f-103">IWiaItem2:: GetParentItem (método)</span><span class="sxs-lookup"><span data-stu-id="64c5f-103">IWiaItem2::GetParentItem method</span></span>

<span data-ttu-id="64c5f-104">Obtiene el elemento primario del árbol que representa un dispositivo de hardware de adquisición de imágenes de Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="64c5f-104">Gets the parent item in the tree that represents a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="64c5f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64c5f-105">Syntax</span></span>


```C++
HRESULT GetParentItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="64c5f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64c5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64c5f-107">*ppIWiaItem2* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="64c5f-107">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64c5f-108">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="64c5f-108">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="64c5f-109">Recibe la dirección de un puntero a la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) del elemento primario del elemento en el árbol de objetos de elemento.</span><span class="sxs-lookup"><span data-stu-id="64c5f-109">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the parent of the item in the tree of item objects.</span></span> <span data-ttu-id="64c5f-110">Si se llama a este método en la raíz del árbol, la dirección devuelta es **null**.</span><span class="sxs-lookup"><span data-stu-id="64c5f-110">If this method is called on the root of the tree, then the returned address is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64c5f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64c5f-111">Return value</span></span>

<span data-ttu-id="64c5f-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="64c5f-112">Type: **HRESULT**</span></span>

<span data-ttu-id="64c5f-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="64c5f-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="64c5f-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="64c5f-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="64c5f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64c5f-115">Remarks</span></span>

<span data-ttu-id="64c5f-116">Dado cualquier objeto [**IWiaItem2**](-wia-iwiaitem2.md) en el árbol de objetos de un dispositivo de hardware WIA 2,0, la aplicación recupera un puntero al elemento primario llamando a esta función.</span><span class="sxs-lookup"><span data-stu-id="64c5f-116">Given any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device, the application retrieves a pointer to the parent item by calling this function.</span></span>

<span data-ttu-id="64c5f-117">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIWiaItem2* si estos punteros no son **null**.</span><span class="sxs-lookup"><span data-stu-id="64c5f-117">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter if these pointers are not **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="64c5f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64c5f-118">Requirements</span></span>



| <span data-ttu-id="64c5f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="64c5f-119">Requirement</span></span> | <span data-ttu-id="64c5f-120">Value</span><span class="sxs-lookup"><span data-stu-id="64c5f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64c5f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64c5f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="64c5f-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="64c5f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="64c5f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64c5f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="64c5f-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="64c5f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="64c5f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64c5f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="64c5f-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="64c5f-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="64c5f-127">IDL</span><span class="sxs-lookup"><span data-stu-id="64c5f-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="64c5f-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="64c5f-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 
