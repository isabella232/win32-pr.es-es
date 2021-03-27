---
description: Muestra un mensaje de error en el globo de sugerencias asociado con el control de dirección de red.
title: Mensaje de NCM_DISPLAYERRORTIP (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5ECAB6C3-69FC-4f2a-A9E6-80BC37ED3119
api_name:
- NCM_DISPLAYERRORTIP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a3968b9001d74721938190369e6b52cf2368835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997256"
---
# <a name="ncm_displayerrortip-message"></a><span data-ttu-id="23160-103">NCM \_ DISPLAYERRORTIP</span><span class="sxs-lookup"><span data-stu-id="23160-103">NCM\_DISPLAYERRORTIP message</span></span>

<span data-ttu-id="23160-104">Muestra un mensaje de error en el globo de sugerencias asociado con el control de dirección de red.</span><span class="sxs-lookup"><span data-stu-id="23160-104">Displays an error message in the balloon tip associated with the network address control.</span></span>


```C++
NCM_DISPLAYERRORTIP

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="23160-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23160-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23160-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23160-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="23160-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="23160-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="23160-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23160-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="23160-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="23160-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23160-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23160-110">Return value</span></span>

<span data-ttu-id="23160-111">Si este mensaje se realiza correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="23160-111">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="23160-112">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="23160-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="23160-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23160-113">Remarks</span></span>

<span data-ttu-id="23160-114">Envía este mensaje para mostrar un mensaje de error cuando una dirección escrita en el control no se valida con respecto a los tipos de direcciones de red permitidos establecidos con el mensaje [**\_ SETALLOWTYPE de NCM**](ncm-setallowtype.md) .</span><span class="sxs-lookup"><span data-stu-id="23160-114">Send this message to display an error message when an address typed into the control does not validate against the allowed network address types set with the [**NCM\_SETALLOWTYPE**](ncm-setallowtype.md) message.</span></span> <span data-ttu-id="23160-115">Use el mensaje de [**NCM \_ GETADDRESS**](ncm-getaddress.md) para validar la dirección.</span><span class="sxs-lookup"><span data-stu-id="23160-115">Use the [**NCM\_GETADDRESS**](ncm-getaddress.md) message to validate the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="23160-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23160-116">Requirements</span></span>



| <span data-ttu-id="23160-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="23160-117">Requirement</span></span> | <span data-ttu-id="23160-118">Value</span><span class="sxs-lookup"><span data-stu-id="23160-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23160-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23160-119">Minimum supported client</span></span><br/> | <span data-ttu-id="23160-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="23160-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="23160-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23160-121">Minimum supported server</span></span><br/> | <span data-ttu-id="23160-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="23160-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23160-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23160-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="23160-124"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="23160-124"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23160-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="23160-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23160-126">**NetAddr \_ DisplayErrorTip**</span><span class="sxs-lookup"><span data-stu-id="23160-126">**NetAddr\_DisplayErrorTip**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




