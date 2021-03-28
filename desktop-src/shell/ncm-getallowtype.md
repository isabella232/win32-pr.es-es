---
description: Recupera los tipos de dirección de red que un control de dirección de red especificado acepta.
title: Mensaje de NCM_GETALLOWTYPE (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1B06463F-0CA6-4e8e-BD3B-917562A6A244
api_name:
- NCM_GETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d93cb3cff575c18764e352da54a717d7c557001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082235"
---
# <a name="ncm_getallowtype-message"></a><span data-ttu-id="eeba7-103">NCM \_ GETALLOWTYPE</span><span class="sxs-lookup"><span data-stu-id="eeba7-103">NCM\_GETALLOWTYPE message</span></span>

<span data-ttu-id="eeba7-104">Recupera los tipos de dirección de red que un control de dirección de red especificado acepta.</span><span class="sxs-lookup"><span data-stu-id="eeba7-104">Retrieves the network address types that a specified network address control accepts.</span></span>


```C++
NCM_GETALLOWTYPE

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="eeba7-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eeba7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeba7-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eeba7-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eeba7-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="eeba7-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eeba7-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eeba7-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eeba7-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="eeba7-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeba7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eeba7-110">Return value</span></span>

<span data-ttu-id="eeba7-111">Devuelve los tipos de dirección de red permitidos como una o varias de las constantes de [**\_ cadena**](net-string.md) de red.</span><span class="sxs-lookup"><span data-stu-id="eeba7-111">Returns the allowed network address types as one or more of the [**NET\_STRING**](net-string.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeba7-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eeba7-112">Remarks</span></span>

<span data-ttu-id="eeba7-113">La máscara devuelta es el criterio que se usa para validar una dirección de red en el mensaje de [**NCM \_ GETADDRESS**](ncm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="eeba7-113">The returned mask is the criterion used to validate a network address in the [**NCM\_GETADDRESS**](ncm-getaddress.md) message.</span></span>

<span data-ttu-id="eeba7-114">Use este mensaje solo para un control de dirección de red.</span><span class="sxs-lookup"><span data-stu-id="eeba7-114">Use this message for a network address control only.</span></span> <span data-ttu-id="eeba7-115">Para crear una instancia de, use la clase **msctls \_ netaddress** definida en ShellAPI. h.</span><span class="sxs-lookup"><span data-stu-id="eeba7-115">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="eeba7-116">Llame a [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) en tiempo de ejecución antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="eeba7-116">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="eeba7-117">Esto inicializa la biblioteca de controles comunes que contiene el control de dirección de red.</span><span class="sxs-lookup"><span data-stu-id="eeba7-117">This initializes the common controls library that contains the network address control.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeba7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eeba7-118">Requirements</span></span>



| <span data-ttu-id="eeba7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeba7-119">Requirement</span></span> | <span data-ttu-id="eeba7-120">Value</span><span class="sxs-lookup"><span data-stu-id="eeba7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eeba7-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeba7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eeba7-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="eeba7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eeba7-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeba7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eeba7-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="eeba7-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eeba7-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eeba7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeba7-126"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeba7-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeba7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="eeba7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeba7-128">**NCM \_ SETALLOWTYPE**</span><span class="sxs-lookup"><span data-stu-id="eeba7-128">**NCM\_SETALLOWTYPE**</span></span>](ncm-setallowtype.md)
</dt> <dt>

[<span data-ttu-id="eeba7-129">**NetAddr \_ GetAllowType**</span><span class="sxs-lookup"><span data-stu-id="eeba7-129">**NetAddr\_GetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




