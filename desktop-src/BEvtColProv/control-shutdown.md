---
description: Detiene el recopilador. Si el recopilador se ejecuta como un servicio, el mejor enfoque es detener el servicio.
ms.assetid: fab3e060-156f-46f5-98a2-d47a23d64552
ms.tgt_platform: multiple
title: Método Shutdown de la clase control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Shutdown
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d401ac528498d7b8ab5ccacbf6a0b5bf781555f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659338"
---
# <a name="shutdown-method-of-the-control-class"></a><span data-ttu-id="65d1a-104">Método Shutdown de la clase control</span><span class="sxs-lookup"><span data-stu-id="65d1a-104">Shutdown method of the Control class</span></span>

<span data-ttu-id="65d1a-105">Detiene el recopilador.</span><span class="sxs-lookup"><span data-stu-id="65d1a-105">Stops the collector.</span></span> <span data-ttu-id="65d1a-106">Si el recopilador se ejecuta como un servicio, el mejor enfoque es detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="65d1a-106">If the collector is running as a service, stopping the service is the better approach.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d1a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65d1a-107">Syntax</span></span>


```mof
void Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="65d1a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65d1a-108">Parameters</span></span>

<span data-ttu-id="65d1a-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="65d1a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="65d1a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65d1a-110">Return value</span></span>

<span data-ttu-id="65d1a-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="65d1a-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="65d1a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65d1a-112">Requirements</span></span>



| <span data-ttu-id="65d1a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="65d1a-113">Requirement</span></span> | <span data-ttu-id="65d1a-114">Value</span><span class="sxs-lookup"><span data-stu-id="65d1a-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65d1a-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65d1a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="65d1a-116">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="65d1a-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="65d1a-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65d1a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="65d1a-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="65d1a-118">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="65d1a-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="65d1a-119">Namespace</span></span><br/>                | <span data-ttu-id="65d1a-120">Raíz de \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="65d1a-120">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="65d1a-121">MOF</span><span class="sxs-lookup"><span data-stu-id="65d1a-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65d1a-122"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65d1a-122"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="65d1a-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65d1a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65d1a-124"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="65d1a-124"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="65d1a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="65d1a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d1a-126">**Control**</span><span class="sxs-lookup"><span data-stu-id="65d1a-126">**Control**</span></span>](control.md)
</dt> </dl>

 

 




