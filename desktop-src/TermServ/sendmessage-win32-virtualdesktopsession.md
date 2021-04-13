---
title: Método SendMessage de la clase Win32_VirtualDesktopSession
description: Envíe un mensaje al usuario a través de la sesión de escritorio virtual.
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- Método SendMessage Servicios de Escritorio remoto
- Método SendMessage Servicios de Escritorio remoto, clase Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession de clase Servicios de Escritorio remoto, método SendMessage
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.SendMessage
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e3e72f5c401b8cbb0e5e5de45f594d61af6275
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422270"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a><span data-ttu-id="93149-106">Método SendMessage de la \_ clase Win32 VirtualDesktopSession</span><span class="sxs-lookup"><span data-stu-id="93149-106">SendMessage method of the Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="93149-107">Envíe un mensaje al usuario a través de la sesión de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="93149-107">Send a message to the user through the virtual desktop session.</span></span>

## <a name="syntax"></a><span data-ttu-id="93149-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93149-108">Syntax</span></span>


```mof
uint32 SendMessage(
  [in] string Title,
  [in] string Message
);
```



## <a name="parameters"></a><span data-ttu-id="93149-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93149-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93149-110">*Título* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="93149-110">*Title* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93149-111">Título de los.</span><span class="sxs-lookup"><span data-stu-id="93149-111">The title of the messge.</span></span>

</dd> <dt>

<span data-ttu-id="93149-112">*Mensaje* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="93149-112">*Message* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93149-113">Contenido del mensaje.</span><span class="sxs-lookup"><span data-stu-id="93149-113">The content of the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93149-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93149-114">Return value</span></span>

<span data-ttu-id="93149-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="93149-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="93149-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93149-116">Requirements</span></span>



| <span data-ttu-id="93149-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="93149-117">Requirement</span></span> | <span data-ttu-id="93149-118">Value</span><span class="sxs-lookup"><span data-stu-id="93149-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="93149-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93149-119">Minimum supported client</span></span><br/> | <span data-ttu-id="93149-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="93149-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="93149-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93149-121">Minimum supported server</span></span><br/> | <span data-ttu-id="93149-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93149-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="93149-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="93149-123">Namespace</span></span><br/>                | <span data-ttu-id="93149-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="93149-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="93149-125">MOF</span><span class="sxs-lookup"><span data-stu-id="93149-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93149-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93149-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="93149-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93149-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93149-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93149-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="93149-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="93149-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93149-130">**Win32 \_ VirtualDesktopSession**</span><span class="sxs-lookup"><span data-stu-id="93149-130">**Win32\_VirtualDesktopSession**</span></span>](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





