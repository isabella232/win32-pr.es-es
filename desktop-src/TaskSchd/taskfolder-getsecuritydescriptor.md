---
title: Propiedad TaskFolder. GetSecurityDescriptor
description: En el caso de scripting, obtiene el descriptor de seguridad de la carpeta.
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- Programador de tareas de la propiedad GetSecurityDescriptor
- Programador de tareas de la propiedad GetSecurityDescriptor, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, propiedad GetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fdb3a301ba3238a699a5ed814057be53c3062d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686105"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a><span data-ttu-id="2c205-106">Propiedad TaskFolder. GetSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="2c205-106">TaskFolder.GetSecurityDescriptor property</span></span>

<span data-ttu-id="2c205-107">En el caso de scripting, obtiene el descriptor de seguridad de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="2c205-107">For scripting, gets the security descriptor for the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c205-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c205-108">Syntax</span></span>


```VB
TaskFolder.GetSecurityDescriptor( _
  ByVal securityInformation, _
  ByRef pSddl _
)
```



## <a name="property-value"></a><span data-ttu-id="2c205-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2c205-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="2c205-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c205-110">Requirements</span></span>



| <span data-ttu-id="2c205-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c205-111">Requirement</span></span> | <span data-ttu-id="2c205-112">Value</span><span class="sxs-lookup"><span data-stu-id="2c205-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c205-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c205-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2c205-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2c205-114">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2c205-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c205-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2c205-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c205-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2c205-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2c205-117">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c205-118"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2c205-118"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2c205-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2c205-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c205-120"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c205-120"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c205-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c205-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c205-122">**TaskFolder.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2c205-122">**TaskFolder.SetSecurityDescriptor**</span></span>](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="2c205-123">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2c205-123">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





