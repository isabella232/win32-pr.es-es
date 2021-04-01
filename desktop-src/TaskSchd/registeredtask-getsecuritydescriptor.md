---
title: RegisteredTask. GetSecurityDescriptor, método
description: En el caso de scripting, obtiene el descriptor de seguridad que se usa como credenciales para la tarea registrada.
ms.assetid: 9b5985c5-c01a-4104-940f-1e0e79f18bb7
keywords:
- Método GetSecurityDescriptor Programador de tareas
- Método GetSecurityDescriptor Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, método GetSecurityDescriptor
topic_type:
- apiref
api_name:
- RegisteredTask.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c7c0e6125bc848b361e4cc2d4515c32d797c57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996852"
---
# <a name="registeredtaskgetsecuritydescriptor-method"></a><span data-ttu-id="142fd-106">RegisteredTask. GetSecurityDescriptor, método</span><span class="sxs-lookup"><span data-stu-id="142fd-106">RegisteredTask.GetSecurityDescriptor method</span></span>

<span data-ttu-id="142fd-107">En el caso de scripting, obtiene el descriptor de seguridad que se usa como credenciales para la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="142fd-107">For scripting, gets the security descriptor that is used as credentials for the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="142fd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="142fd-108">Syntax</span></span>


```VB
sddl = .GetSecurityDescriptor( _
  ByVal securityInformation _
)
```



## <a name="parameters"></a><span data-ttu-id="142fd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="142fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="142fd-110">*securityInformation*</span><span class="sxs-lookup"><span data-stu-id="142fd-110">*securityInformation*</span></span> 
</dt> <dd>

<span data-ttu-id="142fd-111">Información de seguridad de [**la \_ información de seguridad**](/windows/desktop/SecAuthZ/security-information).</span><span class="sxs-lookup"><span data-stu-id="142fd-111">The security information from [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="142fd-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="142fd-112">Return value</span></span>

<span data-ttu-id="142fd-113">Descriptor de seguridad de la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="142fd-113">The security descriptor for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="142fd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="142fd-114">Requirements</span></span>



| <span data-ttu-id="142fd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="142fd-115">Requirement</span></span> | <span data-ttu-id="142fd-116">Value</span><span class="sxs-lookup"><span data-stu-id="142fd-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="142fd-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="142fd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="142fd-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="142fd-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="142fd-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="142fd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="142fd-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="142fd-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="142fd-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="142fd-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="142fd-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="142fd-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="142fd-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="142fd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="142fd-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="142fd-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="142fd-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="142fd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="142fd-126">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="142fd-126">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="142fd-127">**TaskFolder. GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="142fd-127">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="142fd-128">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="142fd-128">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

