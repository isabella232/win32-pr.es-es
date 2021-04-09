---
description: Obtiene la operación de suspensión de la aplicación.
ms.assetid: 33FCAED5-7568-4483-A643-A536B53F7003
title: 'Propiedad ISuspendingEventArgs:: SuspendingOperation (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs.SuspendingOperation
- ISuspendingEventArgs.get_SuspendingOperation
- ISuspendingEventArgs.put_SuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e12ccbb372d7c712585766bba8d7921fae57a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907972"
---
# <a name="isuspendingeventargssuspendingoperation-property"></a><span data-ttu-id="56d08-103">ISuspendingEventArgs:: SuspendingOperation (propiedad)</span><span class="sxs-lookup"><span data-stu-id="56d08-103">ISuspendingEventArgs::SuspendingOperation property</span></span>

<span data-ttu-id="56d08-104">Obtiene la operación de suspensión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56d08-104">Gets the app suspending operation.</span></span>

<span data-ttu-id="56d08-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="56d08-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="56d08-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56d08-106">Syntax</span></span>


```C++
HRESULT put_SuspendingOperation();

HRESULT get_SuspendingOperation(
  [out, retval] ISuspendingOperation **value
);
```



## <a name="property-value"></a><span data-ttu-id="56d08-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="56d08-107">Property value</span></span>

<span data-ttu-id="56d08-108">Operación de suspensión.</span><span class="sxs-lookup"><span data-stu-id="56d08-108">The suspending operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="56d08-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56d08-109">Requirements</span></span>



| <span data-ttu-id="56d08-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="56d08-110">Requirement</span></span> | <span data-ttu-id="56d08-111">Value</span><span class="sxs-lookup"><span data-stu-id="56d08-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56d08-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56d08-112">Minimum supported client</span></span><br/> | <span data-ttu-id="56d08-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="56d08-113">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="56d08-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56d08-114">Minimum supported server</span></span><br/> | <span data-ttu-id="56d08-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="56d08-115">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="56d08-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56d08-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="56d08-117"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="56d08-117"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="56d08-118">IDL</span><span class="sxs-lookup"><span data-stu-id="56d08-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="56d08-119"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56d08-119"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56d08-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="56d08-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56d08-121">**ISuspendingEventArgs**</span><span class="sxs-lookup"><span data-stu-id="56d08-121">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> </dl>

 

 




