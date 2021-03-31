---
description: Obtiene el elemento raíz de un árbol de objetos de elemento que se usa para representar un dispositivo de hardware de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: bc31ad4a-0851-4510-a038-83646ffd5c98
title: 'IWiaItem2:: GetRootItem (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetRootItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c8d4f004cc9c7cabaf4898f5e8c838a0399dc106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809985"
---
# <a name="iwiaitem2getrootitem-method"></a><span data-ttu-id="f9d5f-103">IWiaItem2:: GetRootItem (método)</span><span class="sxs-lookup"><span data-stu-id="f9d5f-103">IWiaItem2::GetRootItem method</span></span>

<span data-ttu-id="f9d5f-104">Obtiene el elemento raíz de un árbol de objetos de elemento que se usa para representar un dispositivo de hardware de adquisición de imágenes de Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="f9d5f-104">Gets the root item of a tree of item objects used to represent a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9d5f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9d5f-105">Syntax</span></span>


```C++
HRESULT GetRootItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="f9d5f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9d5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9d5f-107">*ppIWiaItem2* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9d5f-107">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d5f-108">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f9d5f-108">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="f9d5f-109">Recibe la dirección de un puntero a la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) del elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="f9d5f-109">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9d5f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9d5f-110">Return value</span></span>

<span data-ttu-id="f9d5f-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f9d5f-111">Type: **HRESULT**</span></span>

<span data-ttu-id="f9d5f-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f9d5f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f9d5f-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f9d5f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9d5f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9d5f-114">Remarks</span></span>

<span data-ttu-id="f9d5f-115">Dado cualquier objeto [**IWiaItem2**](-wia-iwiaitem2.md) en el árbol de objetos de un dispositivo de hardware WIA 2,0, la aplicación recupera un puntero al elemento raíz mediante una llamada a esta función.</span><span class="sxs-lookup"><span data-stu-id="f9d5f-115">Given any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device, the application retrieves a pointer to the root item by calling this function.</span></span>

<span data-ttu-id="f9d5f-116">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="f9d5f-116">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9d5f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9d5f-117">Requirements</span></span>



| <span data-ttu-id="f9d5f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9d5f-118">Requirement</span></span> | <span data-ttu-id="f9d5f-119">Value</span><span class="sxs-lookup"><span data-stu-id="f9d5f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9d5f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9d5f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f9d5f-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f9d5f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f9d5f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9d5f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f9d5f-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f9d5f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f9d5f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9d5f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9d5f-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9d5f-125"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9d5f-126">IDL</span><span class="sxs-lookup"><span data-stu-id="f9d5f-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9d5f-127"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9d5f-127"><dt>Wia.idl</dt></span></span> </dl> |



 

 
