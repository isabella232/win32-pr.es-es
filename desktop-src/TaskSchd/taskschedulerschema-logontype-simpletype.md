---
title: Tipo simple de logonType
description: Define los valores posibles del elemento LogonType.
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- Programador de tareas de tipo simple logonType
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58d8c859502e81b5c5101adac3c8c26539870dd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150797"
---
# <a name="logontype-simple-type"></a><span data-ttu-id="59e89-104">Tipo simple de logonType</span><span class="sxs-lookup"><span data-stu-id="59e89-104">logonType Simple Type</span></span>

<span data-ttu-id="59e89-105">Define los valores posibles del elemento [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="59e89-105">Defines the possible values of the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="logonType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="S4U"
         />
        <xs:enumeration
            value="Password"
         />
        <xs:enumeration
            value="InteractiveToken"
         />
        <xs:enumeration
            value="InteractiveTokenOrPassword"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="59e89-106">Valores de enumeración</span><span class="sxs-lookup"><span data-stu-id="59e89-106">Enumeration values</span></span>

<span data-ttu-id="59e89-107">El tipo simple **logonType** define los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="59e89-107">The **logonType** simple type defines the following values.</span></span>



| <span data-ttu-id="59e89-108">Value</span><span class="sxs-lookup"><span data-stu-id="59e89-108">Value</span></span>                      | <span data-ttu-id="59e89-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="59e89-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59e89-110">S4U</span><span class="sxs-lookup"><span data-stu-id="59e89-110">S4U</span></span>                        | <span data-ttu-id="59e89-111">El usuario debe iniciar sesión con un inicio de sesión de servicio para el usuario (S4U).</span><span class="sxs-lookup"><span data-stu-id="59e89-111">User must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="59e89-112">Cuando se usa un inicio de sesión de S4U, el sistema no almacena ninguna contraseña y no se tiene acceso a la red ni a los archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="59e89-112">When an S4U logon is used, no password is stored by the system and there is no access to either the network or encrypted files.</span></span><br/>                                                                                                                                                          |
| <span data-ttu-id="59e89-113">Contraseña</span><span class="sxs-lookup"><span data-stu-id="59e89-113">Password</span></span>                   | <span data-ttu-id="59e89-114">El usuario debe iniciar sesión con una contraseña.</span><span class="sxs-lookup"><span data-stu-id="59e89-114">User must log on using a password.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="59e89-115">InteractiveToken</span><span class="sxs-lookup"><span data-stu-id="59e89-115">InteractiveToken</span></span>           | <span data-ttu-id="59e89-116">El usuario ya debe haber iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="59e89-116">User must already be logged on.</span></span> <span data-ttu-id="59e89-117">La tarea se ejecutará solo en una sesión interactiva existente.</span><span class="sxs-lookup"><span data-stu-id="59e89-117">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="59e89-118">InteractiveTokenOrPassword</span><span class="sxs-lookup"><span data-stu-id="59e89-118">InteractiveTokenOrPassword</span></span> | <span data-ttu-id="59e89-119">Ya no se utiliza; es idéntico a password.</span><span class="sxs-lookup"><span data-stu-id="59e89-119">No longer in use; currently identical to Password.</span></span><br/> <span data-ttu-id="59e89-120">**Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows Vista y Windows server 2008:** La tarea se ejecutará en una sesión interactiva existente o el usuario debe iniciar sesión con una contraseña.</span><span class="sxs-lookup"><span data-stu-id="59e89-120">**Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows Vista and Windows Server 2008:** The task will be run in an existing interactive session or the user must log on using a password.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="59e89-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59e89-121">Requirements</span></span>



| <span data-ttu-id="59e89-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="59e89-122">Requirement</span></span> | <span data-ttu-id="59e89-123">Value</span><span class="sxs-lookup"><span data-stu-id="59e89-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59e89-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59e89-124">Minimum supported client</span></span><br/> | <span data-ttu-id="59e89-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="59e89-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="59e89-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59e89-126">Minimum supported server</span></span><br/> | <span data-ttu-id="59e89-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="59e89-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59e89-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="59e89-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59e89-129">Tipos simples de esquema de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="59e89-129">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="59e89-130">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="59e89-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





