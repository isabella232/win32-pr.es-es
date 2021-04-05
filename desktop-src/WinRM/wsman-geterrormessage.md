---
title: Método WSMan. GetErrorMessage (WSManDisp. h)
description: Devuelve una cadena con formato que contiene el texto de un número de error.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- Método GetErrorMessage Administración remota de Windows
- Administración remota de Windows método GetErrorMessage, objeto WSMan
- Administración remota de Windows de objeto WSMan, método GetErrorMessage
topic_type:
- apiref
api_name:
- WSMan.GetErrorMessage
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d085e6f19c64f609fe1389a2822df1594ee69bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359737"
---
# <a name="wsmangeterrormessage-method"></a><span data-ttu-id="139c6-106">WSMan. GetErrorMessage (método)</span><span class="sxs-lookup"><span data-stu-id="139c6-106">WSMan.GetErrorMessage method</span></span>

<span data-ttu-id="139c6-107">Devuelve una cadena con formato que contiene el texto de un número de error.</span><span class="sxs-lookup"><span data-stu-id="139c6-107">Returns a formatted string that contains the text of an error number.</span></span> <span data-ttu-id="139c6-108">Este método **realiza la misma** operación que la línea de comandos WinRM **HELPMSG** *decimal o el número de error hexadecimal*.</span><span class="sxs-lookup"><span data-stu-id="139c6-108">This method performs the same operation as the **Winrm** command-line **winrm helpmsg** *decimal or hexadecimal error number*.</span></span>

## <a name="syntax"></a><span data-ttu-id="139c6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="139c6-109">Syntax</span></span>


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="139c6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="139c6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="139c6-111">*númeroerror* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="139c6-111">*errorNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="139c6-112">Un número de mensaje de error en formato decimal o hexadecimal de WinRM, WinHTTP u otros componentes del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="139c6-112">An error message number in decimal or hexadecimal from WinRM, WinHTTP, or other operating system components.</span></span>

</dd> <dt>

<span data-ttu-id="139c6-113">*errorMessage* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="139c6-113">*errorMessage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="139c6-114">Una cadena de mensaje de error con formato de mensajes devueltos por el comando **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="139c6-114">An error message string formatted like messages returned from the **Winrm** command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="139c6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="139c6-115">Remarks</span></span>

<span data-ttu-id="139c6-116">El método de C++ correspondiente es [**IWSManEx:: GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).</span><span class="sxs-lookup"><span data-stu-id="139c6-116">The corresponding C++ method is [**IWSManEx::GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).</span></span>

## <a name="requirements"></a><span data-ttu-id="139c6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="139c6-117">Requirements</span></span>



| <span data-ttu-id="139c6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="139c6-118">Requirement</span></span> | <span data-ttu-id="139c6-119">Value</span><span class="sxs-lookup"><span data-stu-id="139c6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="139c6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="139c6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="139c6-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="139c6-121">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="139c6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="139c6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="139c6-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="139c6-123">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="139c6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="139c6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="139c6-125"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="139c6-125"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="139c6-126">IDL</span><span class="sxs-lookup"><span data-stu-id="139c6-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="139c6-127"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="139c6-127"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="139c6-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="139c6-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="139c6-129"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="139c6-129"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="139c6-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="139c6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="139c6-131"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="139c6-131"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="139c6-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="139c6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="139c6-133">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="139c6-133">**WSMan**</span></span>](wsman.md)
</dt> </dl>

 

 





