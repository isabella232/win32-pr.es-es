---
title: Mensaje de TB_SAVERESTORE (commctrl. h)
description: Envíe este mensaje para iniciar el guardado o la restauración de un estado de la barra de herramientas.
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- TB_SAVERESTORE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SAVERESTORE
- TB_SAVERESTOREA
- TB_SAVERESTOREW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e87e4ddbed87e81a88c8711c9931dcf95cf9e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904987"
---
# <a name="tb_saverestore-message"></a><span data-ttu-id="def71-104">\_Mensaje SAVERESTORE TB</span><span class="sxs-lookup"><span data-stu-id="def71-104">TB\_SAVERESTORE message</span></span>

<span data-ttu-id="def71-105">Envíe este mensaje para iniciar el guardado o la restauración de un estado de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="def71-105">Send this message to initiate saving or restoring a toolbar state.</span></span>

## <a name="parameters"></a><span data-ttu-id="def71-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="def71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def71-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="def71-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="def71-108">Marca guardar o restaurar.</span><span class="sxs-lookup"><span data-stu-id="def71-108">Save or restore flag.</span></span> <span data-ttu-id="def71-109">Si este parámetro es **true**, se guarda la información.</span><span class="sxs-lookup"><span data-stu-id="def71-109">If this parameter is **TRUE**, the information is saved.</span></span> <span data-ttu-id="def71-110">Si es **false**, se restaura la información.</span><span class="sxs-lookup"><span data-stu-id="def71-110">If it is **FALSE**, the information is restored.</span></span>

</dd> <dt>

<span data-ttu-id="def71-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="def71-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="def71-112">Puntero a una estructura [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) que especifica la clave del registro, la subclave y el nombre del valor de la información de estado de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="def71-112">Pointer to a [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) structure that specifies the registry key, subkey, and value name for the toolbar state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="def71-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="def71-113">Return value</span></span>

<span data-ttu-id="def71-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="def71-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="def71-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="def71-115">Remarks</span></span>

<span data-ttu-id="def71-116">Para la versión 4,72 y anteriores, para usar este mensaje para guardar o restaurar una barra de herramientas, la ventana primaria del control de barra de herramientas debe implementar un controlador para el código de notificación [ \_ GETBUTTONINFO de TBN](tbn-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="def71-116">For version 4.72 and earlier, to use this message to save or restore a toolbar, the parent window of the toolbar control must implement a handler for the [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) notification code.</span></span> <span data-ttu-id="def71-117">La barra de herramientas emite esta notificación para recuperar información sobre cada botón a medida que se restaura.</span><span class="sxs-lookup"><span data-stu-id="def71-117">The toolbar issues this notification to retrieve information about each button as it is restored.</span></span>

<span data-ttu-id="def71-118">La versión 5,80 incluye una nueva opción de guardar y restaurar.</span><span class="sxs-lookup"><span data-stu-id="def71-118">Version 5.80 includes a new save/restore option.</span></span> <span data-ttu-id="def71-119">Al principio del proceso y, cuando se guarda o se restaura cada botón, la aplicación recibirá una notificación [TBN \_ Save](tbn-save.md) o [TBN \_ restore](tbn-restore.md) .</span><span class="sxs-lookup"><span data-stu-id="def71-119">At the beginning of the process, and as each button is saved or restored, your application will receive a [TBN\_SAVE](tbn-save.md) or [TBN\_RESTORE](tbn-restore.md) notification.</span></span> <span data-ttu-id="def71-120">Para usar esta opción, debe implementar controladores de notificación para proporcionar al shell la información de mapa de bits y de estado que necesita para guardar o restaurar correctamente el estado de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="def71-120">To use this option, you must implement notification handlers to provide the Shell with the bitmap and state information it needs to successfully save or restore the toolbar state.</span></span>

## <a name="requirements"></a><span data-ttu-id="def71-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="def71-121">Requirements</span></span>



| <span data-ttu-id="def71-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="def71-122">Requirement</span></span> | <span data-ttu-id="def71-123">Value</span><span class="sxs-lookup"><span data-stu-id="def71-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="def71-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="def71-124">Minimum supported client</span></span><br/> | <span data-ttu-id="def71-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="def71-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="def71-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="def71-126">Minimum supported server</span></span><br/> | <span data-ttu-id="def71-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="def71-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="def71-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="def71-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="def71-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="def71-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="def71-130">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="def71-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="def71-131">**TB \_ SAVERESTOREW** (Unicode) y **TB \_ SAVERESTOREA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="def71-131">**TB\_SAVERESTOREW** (Unicode) and **TB\_SAVERESTOREA** (ANSI)</span></span><br/>             |



 

 





