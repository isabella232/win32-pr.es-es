---
title: Propiedad TaskFolder. SetSecurityDescriptor
description: Para el scripting, establece el descriptor de seguridad de la carpeta.
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- Programador de tareas de la propiedad SetSecurityDescriptor
- Programador de tareas de la propiedad SetSecurityDescriptor, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, propiedad SetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0854ee6485007e1465dd0a264c908d67443f248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996159"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a><span data-ttu-id="7e085-106">Propiedad TaskFolder. SetSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="7e085-106">TaskFolder.SetSecurityDescriptor property</span></span>

<span data-ttu-id="7e085-107">Para el scripting, establece el descriptor de seguridad de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="7e085-107">For scripting, sets the security descriptor for the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e085-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e085-108">Syntax</span></span>


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a><span data-ttu-id="7e085-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7e085-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="7e085-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e085-110">Remarks</span></span>

<span data-ttu-id="7e085-111">Puede especificar la lista de control de acceso (ACL) en el descriptor de seguridad para una carpeta de tareas con el fin de permitir o denegar el acceso de determinados usuarios y grupos a una carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="7e085-111">You can specify the access control list (ACL) in the security descriptor for a task folder in order to allow or deny certain users and groups access to a task folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e085-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e085-112">Requirements</span></span>



| <span data-ttu-id="7e085-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e085-113">Requirement</span></span> | <span data-ttu-id="7e085-114">Value</span><span class="sxs-lookup"><span data-stu-id="7e085-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e085-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e085-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7e085-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7e085-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7e085-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e085-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7e085-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e085-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7e085-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7e085-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="7e085-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7e085-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7e085-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e085-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e085-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e085-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e085-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e085-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e085-124">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7e085-124">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="7e085-125">**TaskFolder. GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7e085-125">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





