---
description: Busca en el árbol de subelementos de un elemento utilizando el nombre como clave de búsqueda.
ms.assetid: e4ce0bfb-9793-4928-b454-66ae1455b7b5
title: 'IWiaItem2:: FindItemByName (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.FindItemByName
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 821be7e4abd8d1396befa886093aa197bcdea7f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715192"
---
# <a name="iwiaitem2finditembyname-method"></a><span data-ttu-id="73974-103">IWiaItem2:: FindItemByName (método)</span><span class="sxs-lookup"><span data-stu-id="73974-103">IWiaItem2::FindItemByName method</span></span>

<span data-ttu-id="73974-104">Busca en el árbol de subelementos de un elemento utilizando el nombre como clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="73974-104">Searches an item's tree of subitems using the name as the search key.</span></span>

## <a name="syntax"></a><span data-ttu-id="73974-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73974-105">Syntax</span></span>


```C++
HRESULT FindItemByName(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrFullItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="73974-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73974-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73974-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73974-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73974-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="73974-108">Type: **LONG**</span></span>

<span data-ttu-id="73974-109">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="73974-109">Currently unused.</span></span> <span data-ttu-id="73974-110">Debe establecerse como cero.</span><span class="sxs-lookup"><span data-stu-id="73974-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="73974-111">*bstrFullItemName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73974-111">*bstrFullItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73974-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="73974-112">Type: **BSTR**</span></span>

<span data-ttu-id="73974-113">Especifica el nombre del elemento que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="73974-113">Specifies the name fo the item to search for.</span></span>

</dd> <dt>

<span data-ttu-id="73974-114">*ppIWiaItem2* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="73974-114">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73974-115">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="73974-115">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="73974-116">Recibe la dirección de un puntero a la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) del elemento encontrado.</span><span class="sxs-lookup"><span data-stu-id="73974-116">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item found.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73974-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73974-117">Return value</span></span>

<span data-ttu-id="73974-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="73974-118">Type: **HRESULT**</span></span>

<span data-ttu-id="73974-119">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="73974-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73974-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73974-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="73974-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73974-121">Remarks</span></span>

<span data-ttu-id="73974-122">Este método busca en el árbol de elementos secundarios del elemento actual utilizando el nombre como clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="73974-122">This method searches the current item's tree of sub-items using the name as the search key.</span></span> <span data-ttu-id="73974-123">Si **IWiaItem2:: FindItemByName** encuentra el elemento especificado por *bstrFullItemName*, almacena la dirección de un puntero a la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) del elemento en el parámetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="73974-123">If **IWiaItem2::FindItemByName** finds the item specified by *bstrFullItemName*, it stores the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item in the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="73974-124">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="73974-124">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="73974-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73974-125">Requirements</span></span>



| <span data-ttu-id="73974-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="73974-126">Requirement</span></span> | <span data-ttu-id="73974-127">Value</span><span class="sxs-lookup"><span data-stu-id="73974-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73974-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73974-128">Minimum supported client</span></span><br/> | <span data-ttu-id="73974-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="73974-129">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="73974-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73974-130">Minimum supported server</span></span><br/> | <span data-ttu-id="73974-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="73974-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="73974-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73974-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="73974-133"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="73974-133"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="73974-134">IDL</span><span class="sxs-lookup"><span data-stu-id="73974-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="73974-135"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="73974-135"><dt>Wia.idl</dt></span></span> </dl> |



 

 
