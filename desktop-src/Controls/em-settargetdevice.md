---
title: Mensaje EM_SETTARGETDEVICE (RichEdit. h)
description: Establece el dispositivo de destino y el ancho de línea usados para \ 0034; lo que se ve es lo que se obtiene \ 0034; (WYSIWYG) formato en un control Rich Edit.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- EM_SETTARGETDEVICE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETTARGETDEVICE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f82d6ee5df86572564cffcf192395ccee1fbd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150464"
---
# <a name="em_settargetdevice-message"></a><span data-ttu-id="ceec3-104">\_Mensaje SETTARGETDEVICE em</span><span class="sxs-lookup"><span data-stu-id="ceec3-104">EM\_SETTARGETDEVICE message</span></span>

<span data-ttu-id="ceec3-105">Establece el dispositivo de destino y el ancho de línea que se usan para el formato de "lo que se ve es lo que se obtiene" (WYSIWYG) en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="ceec3-105">Sets the target device and line width used for "what you see is what you get" (WYSIWYG) formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ceec3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ceec3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceec3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ceec3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ceec3-108">HDC para el dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="ceec3-108">HDC for the target device.</span></span>

</dd> <dt>

<span data-ttu-id="ceec3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ceec3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ceec3-110">Ancho de línea que se va a usar para dar formato.</span><span class="sxs-lookup"><span data-stu-id="ceec3-110">Line width to use for formatting.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceec3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ceec3-111">Return value</span></span>

<span data-ttu-id="ceec3-112">El valor devuelto es cero si se produce un error en la operación, o es distinto de cero si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="ceec3-112">The return value is zero if the operation fails, or nonzero if it succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceec3-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ceec3-113">Remarks</span></span>

<span data-ttu-id="ceec3-114">La HDC para la impresora predeterminada se puede obtener como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="ceec3-114">The HDC for the default printer can be obtained as follows.</span></span>


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



<span data-ttu-id="ceec3-115">Si *lParam* es cero, no se crean saltos de línea.</span><span class="sxs-lookup"><span data-stu-id="ceec3-115">If *lParam* is zero, no line breaks are created.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceec3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ceec3-116">Requirements</span></span>



| <span data-ttu-id="ceec3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceec3-117">Requirement</span></span> | <span data-ttu-id="ceec3-118">Value</span><span class="sxs-lookup"><span data-stu-id="ceec3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ceec3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ceec3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ceec3-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ceec3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ceec3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ceec3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ceec3-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ceec3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ceec3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ceec3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ceec3-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ceec3-124"><dt>Richedit.h</dt></span></span> </dl> |



 

 





