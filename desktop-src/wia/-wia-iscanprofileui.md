---
description: La interfaz IScanProfileUI permite a las aplicaciones mostrar un cuadro de diálogo para que los usuarios puedan crear, modificar y eliminar perfiles de digitalización.
ms.assetid: d0c7edcc-00d8-49b2-a0f7-fe4bbba90bfb
title: Interfaz IScanProfileUI (Scanprofileui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: c8791461db76c72de81216aef188886f63fde4f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715348"
---
# <a name="iscanprofileui-interface"></a><span data-ttu-id="e55db-103">Interfaz IScanProfileUI</span><span class="sxs-lookup"><span data-stu-id="e55db-103">IScanProfileUI interface</span></span>

<span data-ttu-id="e55db-104">La interfaz **IScanProfileUI** permite a las aplicaciones mostrar un cuadro de diálogo para que los usuarios puedan crear, modificar y eliminar perfiles de digitalización.</span><span class="sxs-lookup"><span data-stu-id="e55db-104">The **IScanProfileUI** interface enables applications to display a dialog box so that users can create, modify, and delete scan profiles.</span></span>

## <a name="members"></a><span data-ttu-id="e55db-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="e55db-105">Members</span></span>

<span data-ttu-id="e55db-106">La interfaz **IScanProfileUI** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="e55db-106">The **IScanProfileUI** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e55db-107">**IScanProfileUI** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e55db-107">**IScanProfileUI** also has these types of members:</span></span>

-   [<span data-ttu-id="e55db-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e55db-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e55db-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e55db-109">Methods</span></span>

<span data-ttu-id="e55db-110">La interfaz **IScanProfileUI** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e55db-110">The **IScanProfileUI** interface has these methods.</span></span>



| <span data-ttu-id="e55db-111">Método</span><span class="sxs-lookup"><span data-stu-id="e55db-111">Method</span></span>                                                             | <span data-ttu-id="e55db-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e55db-112">Description</span></span>                                                                                      |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e55db-113">**ScanProfileDialog**</span><span class="sxs-lookup"><span data-stu-id="e55db-113">**ScanProfileDialog**</span></span>](-wia-iscanprofileui-scanprofiledialog.md) | <span data-ttu-id="e55db-114">Muestra un cuadro de diálogo que permite a los usuarios crear, modificar y eliminar perfiles de digitalización.</span><span class="sxs-lookup"><span data-stu-id="e55db-114">Displays a dialog box that enables users to create, modify, and delete scan profiles.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e55db-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e55db-115">Remarks</span></span>

<span data-ttu-id="e55db-116">El cuadro de diálogo es modal; el usuario no puede cambiar a la ventana primaria hasta que se cierre el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e55db-116">The dialog box is modal; the user cannot switch to the parent window until the dialog box closes.</span></span>

## <a name="requirements"></a><span data-ttu-id="e55db-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e55db-117">Requirements</span></span>



| <span data-ttu-id="e55db-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e55db-118">Requirement</span></span> | <span data-ttu-id="e55db-119">Value</span><span class="sxs-lookup"><span data-stu-id="e55db-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e55db-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e55db-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e55db-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e55db-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e55db-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e55db-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e55db-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e55db-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e55db-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e55db-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e55db-125"><dt>Scanprofileui. h</dt></span><span class="sxs-lookup"><span data-stu-id="e55db-125"><dt>Scanprofileui.h</dt></span></span> </dl>  |
| <span data-ttu-id="e55db-126">IDL</span><span class="sxs-lookup"><span data-stu-id="e55db-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e55db-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e55db-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e55db-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e55db-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e55db-129">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="e55db-129">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="e55db-130">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="e55db-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
