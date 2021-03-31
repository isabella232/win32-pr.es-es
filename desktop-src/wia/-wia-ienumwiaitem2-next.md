---
description: Rellena una matriz de punteros a las interfaces de IWiaItem2.
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: 'IEnumWiaItem2:: Next (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Next
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e8800ead0c8f0abaddd0f055f31962d4d55d14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275641"
---
# <a name="ienumwiaitem2next-method"></a><span data-ttu-id="b0e13-103">IEnumWiaItem2:: Next (método)</span><span class="sxs-lookup"><span data-stu-id="b0e13-103">IEnumWiaItem2::Next method</span></span>

<span data-ttu-id="b0e13-104">Rellena una matriz de punteros a las interfaces de [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="b0e13-104">Fills an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0e13-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0e13-105">Syntax</span></span>


```C++
HRESULT Next(
  [in]      ULONG     cElt,
  [out]     IWiaItem2 **ppIWiaItem2,
  [in, out] ULONG     *pcEltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="b0e13-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0e13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0e13-107">*cElt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0e13-107">*cElt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e13-108">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="b0e13-108">Type: **ULONG**</span></span>

<span data-ttu-id="b0e13-109">Especifica el número de elementos de matriz de la matriz indicado por el parámetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="b0e13-109">Specifies the number of array elements in the array indicated by the *ppIWiaItem2* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b0e13-110">*ppIWiaItem2* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b0e13-110">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e13-111">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b0e13-111">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="b0e13-112">Recibe la dirección de una matriz de punteros de interfaz [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="b0e13-112">Receives the address of an array of [**IWiaItem2**](-wia-iwiaitem2.md) interface pointers.</span></span> <span data-ttu-id="b0e13-113">**IEnumWiaItem2:: Next** rellena esta matriz con punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="b0e13-113">**IEnumWiaItem2::Next** fills this array with interface pointers.</span></span>

</dd> <dt>

<span data-ttu-id="b0e13-114">*pcEltFetched* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b0e13-114">*pcEltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e13-115">Tipo: \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="b0e13-115">Type: \**ULONG\** _</span></span>

<span data-ttu-id="b0e13-116">En la salida, este parámetro recibe el número de punteros de interfaz almacenados realmente en la matriz indicada por el parámetro _ppIWiaItem2 \*.</span><span class="sxs-lookup"><span data-stu-id="b0e13-116">On output, this parameter receives the number of interface pointers actually stored in the array indicated by the _ppIWiaItem2\* parameter.</span></span> <span data-ttu-id="b0e13-117">Cuando se completa la enumeración, este parámetro contiene cero.</span><span class="sxs-lookup"><span data-stu-id="b0e13-117">When the enumeration is complete, this parameter contains zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0e13-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0e13-118">Return value</span></span>

<span data-ttu-id="b0e13-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b0e13-119">Type: **HRESULT**</span></span>

<span data-ttu-id="b0e13-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b0e13-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b0e13-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b0e13-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e13-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0e13-122">Remarks</span></span>

<span data-ttu-id="b0e13-123">El sistema en tiempo de ejecución de adquisición de imágenes de Windows (WIA) 2,0 representa dispositivos de hardware WIA 2,0 como un árbol jerárquico de objetos [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="b0e13-123">The Windows Image Acquisition (WIA) 2.0 run-time system represents WIA 2.0 hardware devices as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="b0e13-124">Las aplicaciones usan el método **IEnumWiaItem2:: Next** para obtener un puntero de interfaz **IWiaItem2** para cada elemento de la carpeta actual del árbol de objetos **IWiaItem2** de un dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="b0e13-124">Applications use the **IEnumWiaItem2::Next** method to obtain an **IWiaItem2** interface pointer for each item in the current folder of a hardware device's **IWiaItem2** object tree.</span></span>

<span data-ttu-id="b0e13-125">Para obtener la lista de punteros, la aplicación pasa una matriz de punteros de interfaz [**IWiaItem2**](-wia-iwiaitem2.md) que asigna.</span><span class="sxs-lookup"><span data-stu-id="b0e13-125">To obtain the list of pointers, the application passes an array of [**IWiaItem2**](-wia-iwiaitem2.md) interface pointers that it allocates.</span></span> <span data-ttu-id="b0e13-126">También pasa el número de elementos de matriz en el parámetro *cElt*.</span><span class="sxs-lookup"><span data-stu-id="b0e13-126">It also passes the number of array elements in the parameter *cElt*.</span></span> <span data-ttu-id="b0e13-127">El método **IEnumWiaItem2:: Next** rellena la matriz con punteros a interfaces **IWiaItem2** .</span><span class="sxs-lookup"><span data-stu-id="b0e13-127">The **IEnumWiaItem2::Next** method fills the array with pointers to **IWiaItem2** interfaces.</span></span>

<span data-ttu-id="b0e13-128">Hasta que se complete el proceso de enumeración, el método **IEnumWiaItem2:: Next** devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="b0e13-128">Until the enumeration process completes, the **IEnumWiaItem2::Next** method returns S\_OK.</span></span> <span data-ttu-id="b0e13-129">Cada vez que lo hace, establece el valor al que apunta *pcEltFetched* en el número de elementos que insertó en la matriz.</span><span class="sxs-lookup"><span data-stu-id="b0e13-129">Each time it does, it sets the value pointed to by *pcEltFetched* to the number of items it inserted into the array.</span></span> <span data-ttu-id="b0e13-130">Cuando **IEnumWiaItem2:: Next** finaliza el proceso de enumeración de objetos [**IWiaItem2**](-wia-iwiaitem2.md) , devuelve S \_ false y establece la ubicación de memoria a la que apunta *pcEltFetched* en cero.</span><span class="sxs-lookup"><span data-stu-id="b0e13-130">When **IEnumWiaItem2::Next** finishes the process of enumerating [**IWiaItem2**](-wia-iwiaitem2.md) objects, it returns S\_FALSE and sets the memory location pointed to by *pcEltFetched* to zero.</span></span>

<span data-ttu-id="b0e13-131">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="b0e13-131">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e13-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0e13-132">Requirements</span></span>



| <span data-ttu-id="b0e13-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0e13-133">Requirement</span></span> | <span data-ttu-id="b0e13-134">Value</span><span class="sxs-lookup"><span data-stu-id="b0e13-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e13-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0e13-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e13-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b0e13-136">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b0e13-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0e13-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e13-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0e13-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b0e13-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0e13-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0e13-140"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0e13-140"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0e13-141">IDL</span><span class="sxs-lookup"><span data-stu-id="b0e13-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0e13-142"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0e13-142"><dt>Wia.idl</dt></span></span> </dl> |



 

 
