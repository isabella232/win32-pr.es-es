---
title: Propiedad MsRdpWorkspace de IMsRdpClientShell2
description: Recupera un puntero a la interfaz IMsRdpWorkspace, que se usa para administrar Conexión de RemoteApp y Escritorio credenciales y conexiones.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad MsRdpWorkspace
- Propiedad MsRdpWorkspace Servicios de Escritorio remoto, interfaz IMsRdpClientShell2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientShell2, propiedad MsRdpWorkspace
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.MsRdpWorkspace
- IMsRdpClientShell2.get_MsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91eadd3f1b422e3da96d5bcd3a5178a2a0b0eb52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802948"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a><span data-ttu-id="1120b-106">IMsRdpClientShell2:: MsRdpWorkspace (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1120b-106">IMsRdpClientShell2::MsRdpWorkspace property</span></span>

<span data-ttu-id="1120b-107">Recupera un puntero a la interfaz [**IMsRdpWorkspace**](imsrdpworkspace.md) , que se usa para administrar conexión de RemoteApp y escritorio credenciales y conexiones.</span><span class="sxs-lookup"><span data-stu-id="1120b-107">Retrieves a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface, which is used to manage RemoteApp and Desktop Connection credentials and connections.</span></span>

<span data-ttu-id="1120b-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1120b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1120b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1120b-109">Syntax</span></span>


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a><span data-ttu-id="1120b-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1120b-110">Property value</span></span>

<span data-ttu-id="1120b-111">Dirección de un puntero a la interfaz [**IMsRdpWorkspace**](imsrdpworkspace.md) .</span><span class="sxs-lookup"><span data-stu-id="1120b-111">The address of a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="1120b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1120b-112">Remarks</span></span>

<span data-ttu-id="1120b-113">La interfaz [**IMsRdpWorkspace**](imsrdpworkspace.md) no se expone como una interfaz personalizada.</span><span class="sxs-lookup"><span data-stu-id="1120b-113">The [**IMsRdpWorkspace**](imsrdpworkspace.md) interface is not exposed as a custom interface.</span></span> <span data-ttu-id="1120b-114">Solo se puede acceder a él a través de métodos [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="1120b-114">It is accessible through [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) methods only.</span></span>

## <a name="requirements"></a><span data-ttu-id="1120b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1120b-115">Requirements</span></span>



| <span data-ttu-id="1120b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1120b-116">Requirement</span></span> | <span data-ttu-id="1120b-117">Value</span><span class="sxs-lookup"><span data-stu-id="1120b-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1120b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1120b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1120b-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1120b-119">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1120b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1120b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1120b-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1120b-121">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="1120b-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1120b-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1120b-123"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1120b-123"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1120b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="1120b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1120b-125">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="1120b-125">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

