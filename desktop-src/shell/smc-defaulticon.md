---
description: Devuelve el icono predeterminado para el elemento especificado por la estructura SMDATA adjunta.
title: Mensaje de SMC_DEFAULTICON (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d5f6789a-f160-4fba-ba64-b1a0c491fdaa
api_name:
- SMC_DEFAULTICON
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 10edab26c87dae4b1c9d2d5f06390fc608ba1edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997793"
---
# <a name="smc_defaulticon-message"></a><span data-ttu-id="a0871-103">Mensaje de DEFAULTICON de SMC \_</span><span class="sxs-lookup"><span data-stu-id="a0871-103">SMC\_DEFAULTICON message</span></span>

<span data-ttu-id="a0871-104">Devuelve el icono predeterminado para el elemento especificado por la estructura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) adjunta.</span><span class="sxs-lookup"><span data-stu-id="a0871-104">Return the default icon for the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DEFAULTICON 
    wParam = (WPARAM) (LPWSTR) pwszIcon;
    lParam = (LPARAM) (int) iIcon
            
```



## <a name="parameters"></a><span data-ttu-id="a0871-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0871-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0871-106">*pwszIcon*</span><span class="sxs-lookup"><span data-stu-id="a0871-106">*pwszIcon*</span></span> 
</dt> <dd>

<span data-ttu-id="a0871-107">Un puntero a una cadena que recibe la ruta de acceso completa del archivo que contiene el icono predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a0871-107">A pointer to a string that receives the fully qualified path of the file that contains the default icon.</span></span>

</dd> <dt>

<span data-ttu-id="a0871-108">*iIcon*</span><span class="sxs-lookup"><span data-stu-id="a0871-108">*iIcon*</span></span> 
</dt> <dd>

<span data-ttu-id="a0871-109">Un puntero a un entero que recibe el índice del icono en el archivo especificado por *pwszIcon*.</span><span class="sxs-lookup"><span data-stu-id="a0871-109">A pointer to an integer that receives the index of the icon in the file specified by *pwszIcon*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0871-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0871-110">Return value</span></span>

<span data-ttu-id="a0871-111">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="a0871-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0871-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0871-112">Remarks</span></span>

<span data-ttu-id="a0871-113">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="a0871-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0871-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0871-114">Requirements</span></span>



| <span data-ttu-id="a0871-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0871-115">Requirement</span></span> | <span data-ttu-id="a0871-116">Value</span><span class="sxs-lookup"><span data-stu-id="a0871-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0871-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0871-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a0871-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a0871-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a0871-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0871-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a0871-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a0871-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a0871-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0871-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0871-122"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0871-122"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0871-123">IDL</span><span class="sxs-lookup"><span data-stu-id="a0871-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a0871-124"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a0871-124"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




