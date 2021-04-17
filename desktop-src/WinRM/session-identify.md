---
title: Método Session. Identify (WSManDisp. h)
description: Consulta un equipo remoto para determinar si es compatible con el protocolo de WS-Management.
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- Identificar método Administración remota de Windows
- Identificar Administración remota de Windows de método, objeto de sesión
- Objeto de sesión Administración remota de Windows, método de identificación
topic_type:
- apiref
api_name:
- Session.Identify
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f1caa5b1e44e4ca65082e33bca4d045e487c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714629"
---
# <a name="sessionidentify-method"></a><span data-ttu-id="a11c7-106">Session. Identify (método)</span><span class="sxs-lookup"><span data-stu-id="a11c7-106">Session.Identify method</span></span>

<span data-ttu-id="a11c7-107">El método **Session. Identify** consulta un equipo remoto para determinar si es compatible con el protocolo de WS-Management.</span><span class="sxs-lookup"><span data-stu-id="a11c7-107">The **Session.Identify** method queries a remote computer to determine if it supports the WS-Management protocol.</span></span> <span data-ttu-id="a11c7-108">Para obtener más información, consulte [detectar si un equipo remoto admite WS-Management protocolo](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="a11c7-108">For more information, see [Detecting Whether a Remote Computer Supports WS-Management Protocol](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a11c7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a11c7-109">Syntax</span></span>


```VB
Session.Identify( _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a11c7-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a11c7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a11c7-111">*marcas* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a11c7-111">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a11c7-112">Para enviar la solicitud en modo autenticado, use la constante de autenticación de la enumeración **WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="a11c7-112">To send the request in authenticated mode use authentication constant from the **WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="a11c7-113">Para enviar en modo no autenticado, use **WSManFlagUseNoAuthentication**.</span><span class="sxs-lookup"><span data-stu-id="a11c7-113">To send in unauthenticated mode, use **WSManFlagUseNoAuthentication**.</span></span> <span data-ttu-id="a11c7-114">Para obtener más información, consulte [**constantes de autenticación**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a11c7-114">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a11c7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a11c7-115">Return value</span></span>

<span data-ttu-id="a11c7-116">Cadena XML que especifica la versión del protocolo WS-Management, el proveedor del sistema operativo y, si la solicitud se envió autenticada, la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a11c7-116">An XML string that specifies the WS-Management protocol version, the operating system vendor and, if the request was sent authenticated, the operating system version.</span></span>

## <a name="remarks"></a><span data-ttu-id="a11c7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a11c7-117">Remarks</span></span>

<span data-ttu-id="a11c7-118">**Session. Identify** se basa en la operación [protocolo WS-Management](ws-management-protocol.md) definida como wsmanIdentity.</span><span class="sxs-lookup"><span data-stu-id="a11c7-118">**Session.Identify** is based on the [WS-Management Protocol](ws-management-protocol.md) operation defined as wsmanIdentity.</span></span> <span data-ttu-id="a11c7-119">Esto se especifica en el paquete SOAP de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="a11c7-119">This is specified in the SOAP packet as follows:</span></span>


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



## <a name="examples"></a><span data-ttu-id="a11c7-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a11c7-120">Examples</span></span>

<span data-ttu-id="a11c7-121">El siguiente ejemplo de VBScript envía una solicitud de identificación no autenticada al equipo remoto denominado remoto en el mismo dominio.</span><span class="sxs-lookup"><span data-stu-id="a11c7-121">The following VBScript example sends an unauthenticated Identify request to the remote computer named Remote in the same domain.</span></span>


```VB
set WSMan = CreateObject("Wsman.Automation")
set Session = WSMan.CreateSession("Remote", _
  WSMan.SessionFlagUseNoAuthentication)
WScript.Echo Session.Identify
```



## <a name="requirements"></a><span data-ttu-id="a11c7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a11c7-122">Requirements</span></span>



| <span data-ttu-id="a11c7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a11c7-123">Requirement</span></span> | <span data-ttu-id="a11c7-124">Value</span><span class="sxs-lookup"><span data-stu-id="a11c7-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a11c7-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a11c7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a11c7-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a11c7-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a11c7-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a11c7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a11c7-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a11c7-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a11c7-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a11c7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a11c7-130"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a11c7-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a11c7-131">IDL</span><span class="sxs-lookup"><span data-stu-id="a11c7-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a11c7-132"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a11c7-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="a11c7-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a11c7-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="a11c7-134"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a11c7-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a11c7-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a11c7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a11c7-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a11c7-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a11c7-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a11c7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a11c7-138">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="a11c7-138">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="a11c7-139">**IWSManSession:: Identify**</span><span class="sxs-lookup"><span data-stu-id="a11c7-139">**IWSManSession::Identify**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[<span data-ttu-id="a11c7-140">Protocolo WS-Management</span><span class="sxs-lookup"><span data-stu-id="a11c7-140">WS-Management Protocol</span></span>](ws-management-protocol.md)
</dt> </dl>

 

 





