---
description: Agrega un nombre de red local alternativo para el equipo desde el que se llama.
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: AddLocalAlternateComputerName función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddLocalAlternateComputerName
- AddLocalAlternateComputerNameA
- AddLocalAlternateComputerNameW
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
- API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
ms.openlocfilehash: 6027752a0e60f135f0cc8a1c0cdd536c59c09621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650011"
---
# <a name="addlocalalternatecomputername-function"></a><span data-ttu-id="09cfa-103">AddLocalAlternateComputerName función)</span><span class="sxs-lookup"><span data-stu-id="09cfa-103">AddLocalAlternateComputerName function</span></span>

<span data-ttu-id="09cfa-104">Agrega un nombre de red local alternativo para el equipo desde el que se llama.</span><span class="sxs-lookup"><span data-stu-id="09cfa-104">Adds an alternate local network name for the computer from which it is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="09cfa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09cfa-105">Syntax</span></span>


```C++
DWORD AddLocalAlternateComputerName(
  _In_ LPCTSTR lpDnsFQHostname,
  _In_ ULONG   ulFlags
);
```



## <a name="parameters"></a><span data-ttu-id="09cfa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09cfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09cfa-107">*lpDnsFQHostname* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09cfa-107">*lpDnsFQHostname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09cfa-108">Nombre alternativo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="09cfa-108">The alternate name to be added.</span></span> <span data-ttu-id="09cfa-109">El nombre debe estar en el formato **ComputerNameDnsFullyQualified** , tal y como se define en la enumeración de [**\_ \_ formato de nombre de equipo**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) , y la función [**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) debe ser capaz de validarla con su formato establecido en **DnsNameHostnameFull**.</span><span class="sxs-lookup"><span data-stu-id="09cfa-109">The name must be in the **ComputerNameDnsFullyQualified** format as defined in the [**COMPUTER\_NAME\_FORMAT**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) enumeration, and the [**DnsValidateName\_W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) function must be able to validate it with its format set to **DnsNameHostnameFull**.</span></span>

</dd> <dt>

<span data-ttu-id="09cfa-110">*ulFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09cfa-110">*ulFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09cfa-111">Este parámetro está reservado y debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="09cfa-111">This parameter is reserved and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09cfa-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09cfa-112">Return value</span></span>

<span data-ttu-id="09cfa-113">Si la función se ejecuta correctamente, la función devuelve el **error \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="09cfa-113">If the function succeeds, the function returns **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="09cfa-114">Si se produce un error en la función, devuelve un código de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="09cfa-114">If the function fails, it returns a nonzero error code.</span></span> <span data-ttu-id="09cfa-115">Entre los códigos de error que devuelve se encuentran los siguientes:</span><span class="sxs-lookup"><span data-stu-id="09cfa-115">Among the error codes that it returns are the following:</span></span>



| <span data-ttu-id="09cfa-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="09cfa-116">Return code</span></span>                                                                                               | <span data-ttu-id="09cfa-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="09cfa-117">Description</span></span>                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09cfa-118"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="09cfa-118"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>  | <span data-ttu-id="09cfa-119">Indica que el parámetro *lpDnsFQHostname* no apunta a un nombre DNS válido o que el parámetro *ulFlags* no es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="09cfa-119">Indicates that the *lpDnsFQHostname* parameter does not point to a valid DNS name, or that the *ulFlags* parameter is not equal to zero.</span></span><br/> |
| <dl> <span data-ttu-id="09cfa-120"><dt>**ERROR \_ de \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09cfa-120"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="09cfa-121">no hay suficiente memoria para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="09cfa-121">There is not enough memory to complete the operation.</span></span><br/>                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="09cfa-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09cfa-122">Requirements</span></span>



| <span data-ttu-id="09cfa-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="09cfa-123">Requirement</span></span> | <span data-ttu-id="09cfa-124">Value</span><span class="sxs-lookup"><span data-stu-id="09cfa-124">Value</span></span> |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09cfa-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09cfa-125">Library</span></span><br/>                | <dl> <span data-ttu-id="09cfa-126"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="09cfa-126"><dt>Kernel32.lib</dt></span></span> </dl>               |
| <span data-ttu-id="09cfa-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="09cfa-127">DLL</span></span><br/>                    | <dl> <span data-ttu-id="09cfa-128"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09cfa-128"><dt>Kernel32.dll</dt></span></span> </dl>               |
| <span data-ttu-id="09cfa-129">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="09cfa-129">Unicode and ANSI names</span></span><br/> | <span data-ttu-id="09cfa-130">**AddLocalAlternateComputerNameW** (Unicode) y **AddLocalAlternateComputerNameA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="09cfa-130">**AddLocalAlternateComputerNameW** (Unicode) and **AddLocalAlternateComputerNameA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09cfa-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="09cfa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09cfa-132">**\_formato de nombre de equipo \_**</span><span class="sxs-lookup"><span data-stu-id="09cfa-132">**COMPUTER\_NAME\_FORMAT**</span></span>](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[<span data-ttu-id="09cfa-133">**DnsValidateName \_ W**</span><span class="sxs-lookup"><span data-stu-id="09cfa-133">**DnsValidateName\_W**</span></span>](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 
