---
description: Establece una confianza de código dinámico de CRL de .NET en disco para .NET.
ms.assetid: 4C8C3EF5-5C3C-4710-8223-D7B5BA86EF47
title: Función WldpSetDynamicCodeTrust (WLDP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpSetDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a266563b40d255fe9e904f02e4e4593d4c4d3f33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423291"
---
# <a name="wldpsetdynamiccodetrust-function"></a><span data-ttu-id="22fab-103">WldpSetDynamicCodeTrust función)</span><span class="sxs-lookup"><span data-stu-id="22fab-103">WldpSetDynamicCodeTrust function</span></span>

<span data-ttu-id="22fab-104">Establece una confianza de código dinámico de CRL de .NET en disco para .NET.</span><span class="sxs-lookup"><span data-stu-id="22fab-104">Sets an on-disk .NET CRL Dynamic Code trustable for .NET.</span></span>

## <a name="syntax"></a><span data-ttu-id="22fab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22fab-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpSetDynamicCodeTrust(
   HANDLE FileHandle
);
```



## <a name="parameters"></a><span data-ttu-id="22fab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22fab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22fab-107">*FileHandle*</span><span class="sxs-lookup"><span data-stu-id="22fab-107">*FileHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="22fab-108">Identificador de un archivo de código dinámico en disco.</span><span class="sxs-lookup"><span data-stu-id="22fab-108">Handle to a on-disk dynamic code file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22fab-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22fab-109">Return value</span></span>

<span data-ttu-id="22fab-110">Este método devuelve **S \_ correcto** si es correcto o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="22fab-110">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="22fab-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22fab-111">Requirements</span></span>



| <span data-ttu-id="22fab-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="22fab-112">Requirement</span></span> | <span data-ttu-id="22fab-113">Value</span><span class="sxs-lookup"><span data-stu-id="22fab-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="22fab-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22fab-114">Minimum supported client</span></span><br/> | <span data-ttu-id="22fab-115">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="22fab-115">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="22fab-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22fab-116">Minimum supported server</span></span><br/> | <span data-ttu-id="22fab-117">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="22fab-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="22fab-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22fab-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="22fab-119"><dt>WLDP. h</dt></span><span class="sxs-lookup"><span data-stu-id="22fab-119"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="22fab-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="22fab-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22fab-121"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22fab-121"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




