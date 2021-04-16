---
description: Crea un objeto de enumerador y devuelve un puntero a su interfaz IEnumWiaItem2 para carpetas con elementos en el árbol IWiaItem2 de un dispositivo de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: 'IWiaItem2:: EnumChildItems (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumChildItems
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2de76d9bf43d10e08e5a85cd2a32d6b377680d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497554"
---
# <a name="iwiaitem2enumchilditems-method"></a><span data-ttu-id="dba58-103">IWiaItem2:: EnumChildItems (método)</span><span class="sxs-lookup"><span data-stu-id="dba58-103">IWiaItem2::EnumChildItems method</span></span>

<span data-ttu-id="dba58-104">Crea un objeto de enumerador y devuelve un puntero a su interfaz [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) para carpetas con elementos en el árbol [**IWiaItem2**](-wia-iwiaitem2.md) de un dispositivo de adquisición de imágenes de Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="dba58-104">Creates an enumerator object and passes back a pointer to its [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface for folders with items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree of a Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="dba58-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dba58-105">Syntax</span></span>


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="dba58-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dba58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dba58-107">*pCategoryGUID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dba58-107">*pCategoryGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dba58-108">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="dba58-108">Type: \**const GUID\** _</span></span>

<span data-ttu-id="dba58-109">Especifica un puntero a una categoría para la que se enumeran los nodos secundarios.</span><span class="sxs-lookup"><span data-stu-id="dba58-109">Specifies a pointer to a category for which child nodes are enumerated.</span></span> <span data-ttu-id="dba58-110">Si _ \* NULL \* \*, se enumeran todos los nodos secundarios.</span><span class="sxs-lookup"><span data-stu-id="dba58-110">If _\*NULL\*\*, then all child nodes are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="dba58-111">*ppIEnumWiaItem2* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="dba58-111">*ppIEnumWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dba58-112">Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="dba58-112">Type: **[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span></span>

<span data-ttu-id="dba58-113">Recibe la dirección de un puntero a la interfaz [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) que crea este método.</span><span class="sxs-lookup"><span data-stu-id="dba58-113">Receives the address of a pointer to the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface that this method creates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dba58-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dba58-114">Return value</span></span>

<span data-ttu-id="dba58-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dba58-115">Type: **HRESULT**</span></span>

<span data-ttu-id="dba58-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="dba58-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dba58-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dba58-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dba58-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dba58-118">Remarks</span></span>

<span data-ttu-id="dba58-119">El sistema en tiempo de ejecución de WIA 2,0 representa cada dispositivo de hardware WIA 2,0 como un árbol jerárquico de objetos [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="dba58-119">The WIA 2.0 run-time system represents each WIA 2.0 hardware device as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="dba58-120">El método **IWiaItem2:: EnumChildItems** permite a las aplicaciones enumerar los elementos secundarios del elemento actual.</span><span class="sxs-lookup"><span data-stu-id="dba58-120">The **IWiaItem2::EnumChildItems** method enables applications to enumerate child items in the current item.</span></span> <span data-ttu-id="dba58-121">Sin embargo, solo se puede aplicar a los elementos que son carpetas.</span><span class="sxs-lookup"><span data-stu-id="dba58-121">However, it can only be applied to items that are folders.</span></span>

<span data-ttu-id="dba58-122">Si la carpeta no está vacía, contiene un subárbol de objetos [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="dba58-122">If the folder is not empty, it contains a subtree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="dba58-123">El método **IWiaItem2:: EnumChildItems** enumera todos los elementos incluidos en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="dba58-123">The **IWiaItem2::EnumChildItems** method enumerates all of the items contained in the folder.</span></span> <span data-ttu-id="dba58-124">Almacena un puntero a un enumerador en el parámetro *ppIEnumWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="dba58-124">It stores a pointer to an enumerator in the *ppIEnumWiaItem2* parameter.</span></span> <span data-ttu-id="dba58-125">Las aplicaciones usan el puntero de enumerador para realizar la enumeración de los elementos secundarios de un objeto.</span><span class="sxs-lookup"><span data-stu-id="dba58-125">Applications use the enumerator pointer to perform the enumeration of an object's child items.</span></span>

<span data-ttu-id="dba58-126">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIEnumWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="dba58-126">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnumWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="dba58-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dba58-127">Requirements</span></span>



| <span data-ttu-id="dba58-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="dba58-128">Requirement</span></span> | <span data-ttu-id="dba58-129">Value</span><span class="sxs-lookup"><span data-stu-id="dba58-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dba58-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dba58-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dba58-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dba58-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dba58-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dba58-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dba58-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dba58-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dba58-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dba58-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="dba58-135"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="dba58-135"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="dba58-136">IDL</span><span class="sxs-lookup"><span data-stu-id="dba58-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dba58-137"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dba58-137"><dt>Wia.idl</dt></span></span> </dl> |



 

 
