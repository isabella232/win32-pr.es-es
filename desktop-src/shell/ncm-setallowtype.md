---
description: Establece los tipos de dirección de red que acepta un control de dirección de red especificado.
title: Mensaje de NCM_SETALLOWTYPE (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FD998452-047A-4aea-A08E-8F6F8C30115B
api_name:
- NCM_SETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d9cc822e07022a01439fbe7e41243bd1b78e636b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810940"
---
# <a name="ncm_setallowtype-message"></a><span data-ttu-id="86182-103">NCM \_ SETALLOWTYPE</span><span class="sxs-lookup"><span data-stu-id="86182-103">NCM\_SETALLOWTYPE message</span></span>

<span data-ttu-id="86182-104">Establece los tipos de dirección de red que acepta un control de dirección de red especificado.</span><span class="sxs-lookup"><span data-stu-id="86182-104">Sets the network address types that a specified network address control accepts.</span></span>


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="86182-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86182-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86182-106">*addrMask* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86182-106">*addrMask* \[in\]</span></span>
</dt> <dd><span data-ttu-id="86182-107">Especifica los tipos de dirección de red como una o varias de las constantes de <a href="net-string.md">**\_ cadena**</a> de red.</span><span class="sxs-lookup"><span data-stu-id="86182-107">Specifies the network address types as one or more of the <a href="net-string.md">**NET\_STRING**</a> constants.</span></span></dd> <dt>

<span data-ttu-id="86182-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86182-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="86182-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="86182-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86182-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86182-110">Return value</span></span>

<span data-ttu-id="86182-111">Devuelve \_ si es correcto, o un valor de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="86182-111">Returns S\_OK if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="86182-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86182-112">Remarks</span></span>

<span data-ttu-id="86182-113">El conjunto de máscaras es el criterio que se usa para validar una dirección de red en el mensaje de [**NCM \_ GETADDRESS**](ncm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="86182-113">The mask set is the criterion used to validate a network address in the [**NCM\_GETADDRESS**](ncm-getaddress.md) message.</span></span>

<span data-ttu-id="86182-114">Use este mensaje solo para un control de dirección de red.</span><span class="sxs-lookup"><span data-stu-id="86182-114">Use this message for a network address control only.</span></span> <span data-ttu-id="86182-115">Para crear una instancia de, use la clase **msctls \_ netaddress** definida en ShellAPI. h.</span><span class="sxs-lookup"><span data-stu-id="86182-115">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="86182-116">Llame a [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) en tiempo de ejecución antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="86182-116">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="86182-117">Esto inicializa la biblioteca de controles comunes que contiene el control de dirección de red.</span><span class="sxs-lookup"><span data-stu-id="86182-117">This initializes the common controls library that contains the network address control.</span></span>

## <a name="requirements"></a><span data-ttu-id="86182-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86182-118">Requirements</span></span>



| <span data-ttu-id="86182-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="86182-119">Requirement</span></span> | <span data-ttu-id="86182-120">Value</span><span class="sxs-lookup"><span data-stu-id="86182-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86182-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86182-121">Minimum supported client</span></span><br/> | <span data-ttu-id="86182-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="86182-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="86182-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86182-123">Minimum supported server</span></span><br/> | <span data-ttu-id="86182-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="86182-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="86182-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86182-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="86182-126"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="86182-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86182-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="86182-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86182-128">**NCM \_ GETALLOWTYPE**</span><span class="sxs-lookup"><span data-stu-id="86182-128">**NCM\_GETALLOWTYPE**</span></span>](ncm-getallowtype.md)
</dt> <dt>

[<span data-ttu-id="86182-129">**NetAddr \_ SetAllowType**</span><span class="sxs-lookup"><span data-stu-id="86182-129">**NetAddr\_SetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




