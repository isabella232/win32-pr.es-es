---
title: Método IWMDRMLicense GetInclusionList (wmdrmsdk. h)
description: El método GetInclusionList recupera la lista de inclusión completa para la licencia actual o la cadena de licencias.
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- Método GetInclusionList formato de Windows Media
- Método GetInclusionList formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método GetInclusionList
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetInclusionList
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f0d2837a4bb84c07214cce3e4fbc3d4d96b9583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708167"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a><span data-ttu-id="8578d-106">IWMDRMLicense:: GetInclusionList (método)</span><span class="sxs-lookup"><span data-stu-id="8578d-106">IWMDRMLicense::GetInclusionList method</span></span>

<span data-ttu-id="8578d-107">El método **GetInclusionList** recupera la lista de inclusión completa para la licencia actual o la cadena de licencias.</span><span class="sxs-lookup"><span data-stu-id="8578d-107">The **GetInclusionList** method retrieves the entire inclusion list for the current license or license chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="8578d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8578d-108">Syntax</span></span>


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a><span data-ttu-id="8578d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8578d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8578d-110">*ppGuids* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8578d-110">*ppGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8578d-111">Recibe una matriz de GUID que identifican las tecnologías incluidas.</span><span class="sxs-lookup"><span data-stu-id="8578d-111">Receives an array of GUIDs identifying the included technologies.</span></span>

</dd> <dt>

<span data-ttu-id="8578d-112">*pcGuids* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8578d-112">*pcGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8578d-113">Recibe el número de elementos de la matriz *ppGuids* .</span><span class="sxs-lookup"><span data-stu-id="8578d-113">Receives the number of elements in the *ppGuids* array.</span></span> <span data-ttu-id="8578d-114">La matriz se asigna mediante **CoTaskMemAlloc**.</span><span class="sxs-lookup"><span data-stu-id="8578d-114">The array is allocated by using **CoTaskMemAlloc**.</span></span> <span data-ttu-id="8578d-115">Cuando termine la lista, libere la memoria mediante una llamada a **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="8578d-115">When finished with the list, release the memory by calling **CoTaskMemFree**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8578d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8578d-116">Return value</span></span>

<span data-ttu-id="8578d-117">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8578d-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8578d-118">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="8578d-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8578d-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8578d-119">Return code</span></span>                                                                          | <span data-ttu-id="8578d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8578d-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8578d-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8578d-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8578d-122">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="8578d-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8578d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8578d-123">Remarks</span></span>

<span data-ttu-id="8578d-124">El emisor de la licencia puede especificar otros sistemas de protección a los que se pueda convertir el contenido cifrado.</span><span class="sxs-lookup"><span data-stu-id="8578d-124">The license issuer can specify other protection systems to which the encrypted content may be converted.</span></span> <span data-ttu-id="8578d-125">La lista de GUID recuperada por este método identifica los sistemas de protección permitidos.</span><span class="sxs-lookup"><span data-stu-id="8578d-125">The list of GUIDs retrieved by this method identifies the allowed protection systems.</span></span> <span data-ttu-id="8578d-126">Al entrar en un contrato de licencia con Microsoft para obtener la biblioteca de código auxiliar, recibirá una lista de los sistemas de protección admitidos actualmente y los GUID que se usan para identificarlos.</span><span class="sxs-lookup"><span data-stu-id="8578d-126">When you enter into a license agreement with Microsoft to get the stub library, you will receive a list of currently supported protection systems and the GUIDs used to identify them.</span></span>

## <a name="requirements"></a><span data-ttu-id="8578d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8578d-127">Requirements</span></span>



| <span data-ttu-id="8578d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8578d-128">Requirement</span></span> | <span data-ttu-id="8578d-129">Value</span><span class="sxs-lookup"><span data-stu-id="8578d-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8578d-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8578d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8578d-131"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8578d-131"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="8578d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8578d-132">Library</span></span><br/> | <dl> <span data-ttu-id="8578d-133"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8578d-133"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8578d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="8578d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8578d-135">**Listas de inclusión y autorización explícitas**</span><span class="sxs-lookup"><span data-stu-id="8578d-135">**Explicit Authorization and Inclusion Lists**</span></span>](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[<span data-ttu-id="8578d-136">**Interfaz IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="8578d-136">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





