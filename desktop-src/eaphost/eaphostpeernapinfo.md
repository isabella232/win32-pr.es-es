---
title: Estructura EapHostPeerNapInfo (Eaphostpeerapis. h)
description: Contiene la información de protección de acceso a redes (NAP) de un suplicante EAP.
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- EapHostPeerNapInfo estructura EAPHost
topic_type:
- apiref
api_name:
- EapHostPeerNapInfo
api_location:
- eaphostpeerapis.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3221f40dea9e84e410a1a643bbbcdc94e9039b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079688"
---
# <a name="eaphostpeernapinfo-structure"></a><span data-ttu-id="d14c0-104">Estructura EapHostPeerNapInfo</span><span class="sxs-lookup"><span data-stu-id="d14c0-104">EapHostPeerNapInfo structure</span></span>

<span data-ttu-id="d14c0-105">La estructura **EapHostPeerNapInfo** contiene la información de protección de acceso a redes (NAP) de un suplicante EAP.</span><span class="sxs-lookup"><span data-stu-id="d14c0-105">The **EapHostPeerNapInfo** structure contains the Network Access Protection (NAP) information on an EAP supplicant.</span></span>

## <a name="syntax"></a><span data-ttu-id="d14c0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d14c0-106">Syntax</span></span>


```C++
typedef struct _tagEapHostPeerNapInfo {
  ISOLATION_STATE isolationState;
  ProbationTime   probationTime;
  UINT32          stringCorrelationIdLength;
} EapHostPeerNapInfo;
```



## <a name="members"></a><span data-ttu-id="d14c0-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d14c0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d14c0-108">**isolationState**</span><span class="sxs-lookup"><span data-stu-id="d14c0-108">**isolationState**</span></span>
</dt> <dd>

<span data-ttu-id="d14c0-109">Una estructura de [**\_ Estado de aislamiento**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) que especifica el estado de aislamiento de NAP de un equipo.</span><span class="sxs-lookup"><span data-stu-id="d14c0-109">An [**ISOLATION\_STATE**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) structure that specifies the NAP isolation state of a computer.</span></span> <span data-ttu-id="d14c0-110">El estado de aislamiento determina el nivel de acceso a la red concedido.</span><span class="sxs-lookup"><span data-stu-id="d14c0-110">The isolation state determines the level of network access granted.</span></span>

</dd> <dt>

<span data-ttu-id="d14c0-111">**probationTime**</span><span class="sxs-lookup"><span data-stu-id="d14c0-111">**probationTime**</span></span>
</dt> <dd>

<span data-ttu-id="d14c0-112">Estructura **ProbationTime** que especifica el tiempo necesario para que la conexión salga de la cuarentena después de la cual se quitará la conexión.</span><span class="sxs-lookup"><span data-stu-id="d14c0-112">A **ProbationTime** structure that specifies the time required for the connection to come out of quarantine after which the connection will be dropped.</span></span> <span data-ttu-id="d14c0-113">Una estructura **ProbationTime** es idéntica a una estructura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="d14c0-113">A **ProbationTime** structure is identical to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d14c0-114">**stringCorrelationIdLength**</span><span class="sxs-lookup"><span data-stu-id="d14c0-114">**stringCorrelationIdLength**</span></span>
</dt> <dd>

<span data-ttu-id="d14c0-115">La longitud, en bytes, del [STRINGCORRELATIONID](/windows/desktop/NAP/nap-datatypes) NAP que sigue a esta estructura.</span><span class="sxs-lookup"><span data-stu-id="d14c0-115">The length, in bytes, of the NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) that follows this structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d14c0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d14c0-116">Remarks</span></span>

<span data-ttu-id="d14c0-117">La estructura **EapHostPeerNapInfo** precede a la [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) NAP del tipo de datos **WCHAR** en el flujo de bytes RPC.</span><span class="sxs-lookup"><span data-stu-id="d14c0-117">The **EapHostPeerNapInfo** structure precedes the NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) of data type **WCHAR** in the RPC byte stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="d14c0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d14c0-118">Requirements</span></span>



| <span data-ttu-id="d14c0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d14c0-119">Requirement</span></span> | <span data-ttu-id="d14c0-120">Value</span><span class="sxs-lookup"><span data-stu-id="d14c0-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d14c0-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d14c0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d14c0-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d14c0-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="d14c0-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d14c0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d14c0-124">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d14c0-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d14c0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d14c0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d14c0-126"><dt>Eaphostpeerapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="d14c0-126"><dt>Eaphostpeerapis.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d14c0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d14c0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d14c0-128">Estructuras de suplicante de EAPHost</span><span class="sxs-lookup"><span data-stu-id="d14c0-128">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="d14c0-129">**EapHostPeerGetAuthStatus**</span><span class="sxs-lookup"><span data-stu-id="d14c0-129">**EapHostPeerGetAuthStatus**</span></span>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[<span data-ttu-id="d14c0-130">**EapHostPeerMethodAuthParams**</span><span class="sxs-lookup"><span data-stu-id="d14c0-130">**EapHostPeerMethodAuthParams**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

