---
description: Crea una instancia adicional de la interfaz IEnumWiaItem2 y le devuelve un puntero.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: 'IEnumWiaItem2:: Clone (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Clone
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3279e7db3efe66e940adbcb9677204e5df7867f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810802"
---
# <a name="ienumwiaitem2clone-method"></a><span data-ttu-id="09e71-103">IEnumWiaItem2:: Clone (método)</span><span class="sxs-lookup"><span data-stu-id="09e71-103">IEnumWiaItem2::Clone method</span></span>

<span data-ttu-id="09e71-104">Crea una instancia adicional de la interfaz [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) y le devuelve un puntero.</span><span class="sxs-lookup"><span data-stu-id="09e71-104">Creates an additional instance of the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface and sends back a pointer to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e71-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09e71-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="09e71-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09e71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09e71-107">*ppIEnum* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="09e71-107">*ppIEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09e71-108">Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="09e71-108">Type: **[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span></span>

<span data-ttu-id="09e71-109">Recibe la dirección de la instancia de la interfaz [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) que crea **IEnumWiaItem2:: Clone** .</span><span class="sxs-lookup"><span data-stu-id="09e71-109">Receives the address of the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface instance that **IEnumWiaItem2::Clone** creates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09e71-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09e71-110">Return value</span></span>

<span data-ttu-id="09e71-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="09e71-111">Type: **HRESULT**</span></span>

<span data-ttu-id="09e71-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="09e71-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="09e71-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="09e71-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="09e71-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09e71-114">Remarks</span></span>

<span data-ttu-id="09e71-115">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="09e71-115">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="09e71-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09e71-116">Requirements</span></span>



| <span data-ttu-id="09e71-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="09e71-117">Requirement</span></span> | <span data-ttu-id="09e71-118">Value</span><span class="sxs-lookup"><span data-stu-id="09e71-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09e71-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09e71-119">Minimum supported client</span></span><br/> | <span data-ttu-id="09e71-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="09e71-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="09e71-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09e71-121">Minimum supported server</span></span><br/> | <span data-ttu-id="09e71-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="09e71-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="09e71-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09e71-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="09e71-124"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="09e71-124"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="09e71-125">IDL</span><span class="sxs-lookup"><span data-stu-id="09e71-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="09e71-126"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="09e71-126"><dt>Wia.idl</dt></span></span> </dl> |



 

 
