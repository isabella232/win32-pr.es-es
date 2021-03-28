---
description: Se envía a un archivo DLL de extensión cuando el administrador de archivos está cargando el archivo DLL.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: Mensaje de FMEVENT_LOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: de7a950e3f17c9b2cee2b66a047d289ca29b6b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985514"
---
# <a name="fmevent_load-message"></a><span data-ttu-id="cf98b-103">Mensaje de carga de FMEVENT \_</span><span class="sxs-lookup"><span data-stu-id="cf98b-103">FMEVENT\_LOAD message</span></span>

<span data-ttu-id="cf98b-104">Se envía a un archivo DLL de extensión cuando el administrador de archivos está cargando el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="cf98b-104">Sent to an extension DLL when File Manager is loading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf98b-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf98b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf98b-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf98b-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf98b-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cf98b-107">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cf98b-108">*lpfmsld*</span><span class="sxs-lookup"><span data-stu-id="cf98b-108">*lpfmsld*</span></span> 
</dt> <dd>

<span data-ttu-id="cf98b-109">La dirección de una estructura de [**\_ carga de FMS**](fms-load.md) que especifica el valor Delta del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="cf98b-109">The address of an [**FMS\_LOAD**](fms-load.md) structure that specifies the menu item delta value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf98b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf98b-110">Return value</span></span>

<span data-ttu-id="cf98b-111">Un archivo DLL de extensión debe devolver **true** para continuar cargando el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="cf98b-111">An extension DLL must return **TRUE** to continue loading the DLL.</span></span> <span data-ttu-id="cf98b-112">Si el archivo DLL devuelve **false**, el administrador de archivos llama a la función [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) y finaliza cualquier comunicación con el archivo dll de extensión.</span><span class="sxs-lookup"><span data-stu-id="cf98b-112">If the DLL returns **FALSE**, File Manager calls the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function and ends any communication with the extension DLL.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf98b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf98b-113">Remarks</span></span>

<span data-ttu-id="cf98b-114">Una aplicación debe rellenar los miembros **dwSize**, **szMenuName** y **hMenu** en la estructura de [**\_ carga de FMS**](fms-load.md) .</span><span class="sxs-lookup"><span data-stu-id="cf98b-114">An application should fill the **dwSize**, **szMenuName**, and **hMenu** members in the [**FMS\_LOAD**](fms-load.md) structure.</span></span> <span data-ttu-id="cf98b-115">También debe guardar el valor del miembro **wMenuDelta** y usarlo para identificar los elementos de menú al modificar el menú.</span><span class="sxs-lookup"><span data-stu-id="cf98b-115">It should also save the value of the **wMenuDelta** member and use it to identify menu items when modifying the menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf98b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf98b-116">Requirements</span></span>



| <span data-ttu-id="cf98b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf98b-117">Requirement</span></span> | <span data-ttu-id="cf98b-118">Value</span><span class="sxs-lookup"><span data-stu-id="cf98b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf98b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf98b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cf98b-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cf98b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="cf98b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf98b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cf98b-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cf98b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cf98b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf98b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf98b-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf98b-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf98b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf98b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf98b-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="cf98b-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 
