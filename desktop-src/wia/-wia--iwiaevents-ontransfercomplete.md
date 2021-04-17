---
description: Evento que tiene lugar cuando se completa una transferencia de datos correctamente.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Evento WIA. OnTransferComplete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnTransferComplete
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d33685e0e8fe233f96e9841359e56f759032d17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276865"
---
# <a name="wiaontransfercomplete-event"></a><span data-ttu-id="558b5-103">Evento WIA. OnTransferComplete</span><span class="sxs-lookup"><span data-stu-id="558b5-103">Wia.OnTransferComplete event</span></span>

<span data-ttu-id="558b5-104">Evento que tiene lugar cuando se completa una transferencia de datos correctamente.</span><span class="sxs-lookup"><span data-stu-id="558b5-104">Event that occurs when a data transfer is completed successfully.</span></span>

## <a name="syntax"></a><span data-ttu-id="558b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="558b5-105">Syntax</span></span>


```JScript
Wia.OnTransferComplete(
  Item,
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="558b5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="558b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="558b5-107">*Elemento*</span><span class="sxs-lookup"><span data-stu-id="558b5-107">*Item*</span></span> 
</dt> <dd>

<span data-ttu-id="558b5-108">Objeto de [**elemento**](-wia-item.md) transferido.</span><span class="sxs-lookup"><span data-stu-id="558b5-108">The [**Item**](-wia-item.md) object transferred.</span></span>

</dd> <dt>

<span data-ttu-id="558b5-109">*Ruta de acceso*</span><span class="sxs-lookup"><span data-stu-id="558b5-109">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="558b5-110">Ruta de acceso y nombre de archivo de la imagen transferida.</span><span class="sxs-lookup"><span data-stu-id="558b5-110">The path and file name of the transferred image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="558b5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="558b5-111">Return value</span></span>

<span data-ttu-id="558b5-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="558b5-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="558b5-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="558b5-113">Remarks</span></span>

<span data-ttu-id="558b5-114">WIA notifica el script o la aplicación cuando una transferencia de datos, imagen o sonido se completa correctamente.</span><span class="sxs-lookup"><span data-stu-id="558b5-114">WIA notifies the script or application when a data transfer, image or sound, completes successfully.</span></span> <span data-ttu-id="558b5-115">Implemente la subrutina **objWia** \_ **OnTransferComplete ()** para permitir que el script o la aplicación respondan a la finalización de la transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="558b5-115">Implement the **objWia**\_**OnTransferComplete()** subroutine to allow your script or application to respond to the completion of the data transfer.</span></span>

<span data-ttu-id="558b5-116">Por ejemplo, podría querer un script para mostrar una imagen después de transferirla.</span><span class="sxs-lookup"><span data-stu-id="558b5-116">For example, you might want a script to display an image after it is transferred.</span></span>

## <a name="requirements"></a><span data-ttu-id="558b5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="558b5-117">Requirements</span></span>



| <span data-ttu-id="558b5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="558b5-118">Requirement</span></span> | <span data-ttu-id="558b5-119">Value</span><span class="sxs-lookup"><span data-stu-id="558b5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="558b5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="558b5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="558b5-121">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="558b5-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="558b5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="558b5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="558b5-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="558b5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="558b5-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="558b5-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="558b5-125"><dt>Wiascr.dll (versión 4,90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="558b5-125"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




