---
description: Solicita el título y el texto de un recuadro informativo de comillas angulares para el elemento especificado por la estructura SMDATA correspondiente.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: Mensaje de SMC_CHEVRONGETTIP (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118056627d19990648e81b69aa355f3df99ec286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985747"
---
# <a name="smc_chevrongettip-message"></a><span data-ttu-id="b0aad-103">Mensaje de CHEVRONGETTIP de SMC \_</span><span class="sxs-lookup"><span data-stu-id="b0aad-103">SMC\_CHEVRONGETTIP message</span></span>

<span data-ttu-id="b0aad-104">Solicita el título y el texto de un recuadro informativo de comillas angulares para el elemento especificado por la estructura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b0aad-104">Requests the title and text for a chevron infotip for the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a><span data-ttu-id="b0aad-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0aad-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0aad-106">*pwszTipTitle*</span><span class="sxs-lookup"><span data-stu-id="b0aad-106">*pwszTipTitle*</span></span> 
</dt> <dd>

<span data-ttu-id="b0aad-107">Un puntero a un búfer que recibe una cadena Unicode terminada en **null** que contiene el título del recuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="b0aad-107">A pointer to a buffer that receives a **NULL**-terminated Unicode string that contains the infotip's title.</span></span> <span data-ttu-id="b0aad-108">Esta cadena no debe tener más de \_ caracteres de ruta de acceso máxima, incluido el carácter **nulo** de terminación.</span><span class="sxs-lookup"><span data-stu-id="b0aad-108">This string must be no longer than MAX\_PATH characters long, including the terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="b0aad-109">*pwszTipText*</span><span class="sxs-lookup"><span data-stu-id="b0aad-109">*pwszTipText*</span></span> 
</dt> <dd>

<span data-ttu-id="b0aad-110">Un puntero a un búfer que recibe una cadena Unicode terminada en **null** que contiene el texto del recuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="b0aad-110">A pointer to a buffer that receives a **NULL**-terminated Unicode string that contains the infotip's text.</span></span> <span data-ttu-id="b0aad-111">Esta cadena no debe tener más de \_ caracteres de ruta de acceso máxima, incluido el carácter **nulo** de terminación.</span><span class="sxs-lookup"><span data-stu-id="b0aad-111">This string must be no longer than MAX\_PATH characters long, including the terminating **NULL** character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0aad-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0aad-112">Return value</span></span>

<span data-ttu-id="b0aad-113">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="b0aad-113">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0aad-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0aad-114">Remarks</span></span>

<span data-ttu-id="b0aad-115">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="b0aad-115">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0aad-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0aad-116">Requirements</span></span>



| <span data-ttu-id="b0aad-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0aad-117">Requirement</span></span> | <span data-ttu-id="b0aad-118">Value</span><span class="sxs-lookup"><span data-stu-id="b0aad-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0aad-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0aad-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b0aad-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b0aad-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b0aad-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0aad-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b0aad-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b0aad-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b0aad-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0aad-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0aad-124"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0aad-124"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0aad-125">IDL</span><span class="sxs-lookup"><span data-stu-id="b0aad-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0aad-126"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0aad-126"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




