---
description: Muestra un cuadro de diálogo que permite a los usuarios crear, modificar y eliminar perfiles de digitalización.
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: 'IScanProfileUI:: ScanProfileDialog (método) (Scanprofileui. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI.ScanProfileDialog
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: bc8707378f1debc322fea258ceb8aad0c6400ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276857"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a><span data-ttu-id="bb148-103">IScanProfileUI:: ScanProfileDialog (método)</span><span class="sxs-lookup"><span data-stu-id="bb148-103">IScanProfileUI::ScanProfileDialog method</span></span>

<span data-ttu-id="bb148-104">Muestra un cuadro de diálogo que permite a los usuarios crear, modificar y eliminar perfiles de digitalización.</span><span class="sxs-lookup"><span data-stu-id="bb148-104">Displays a dialog box that enables users to create, modify, and delete scan profiles.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb148-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb148-105">Syntax</span></span>


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a><span data-ttu-id="bb148-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb148-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb148-107">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb148-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb148-108">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="bb148-108">Type: **HWND**</span></span>

<span data-ttu-id="bb148-109">Identificador de la ventana primaria que posee el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bb148-109">The handle of the parent window that owns the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb148-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb148-110">Return value</span></span>

<span data-ttu-id="bb148-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bb148-111">Type: **HRESULT**</span></span>

<span data-ttu-id="bb148-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="bb148-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb148-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bb148-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb148-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb148-114">Remarks</span></span>

<span data-ttu-id="bb148-115">El cuadro de diálogo es modal; el usuario no puede cambiar a la ventana primaria hasta que se cierre el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bb148-115">The dialog box is modal; the user cannot switch to the parent window until the dialog box closes.</span></span>

<span data-ttu-id="bb148-116">Los valores del `<ProfileName>` elemento y el `<WiaItem>` elemento se pueden cambiar en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bb148-116">The values of the `<ProfileName>` element and the `<WiaItem>` element can be changed in the dialog box.</span></span> <span data-ttu-id="bb148-117">`<Default>`Se puede Agregar o eliminar el elemento.</span><span class="sxs-lookup"><span data-stu-id="bb148-117">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="bb148-118">No se puede realizar ningún otro cambio en el perfil de digitalización en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bb148-118">No other changes to the scan profile can be made in the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb148-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb148-119">Requirements</span></span>



| <span data-ttu-id="bb148-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb148-120">Requirement</span></span> | <span data-ttu-id="bb148-121">Value</span><span class="sxs-lookup"><span data-stu-id="bb148-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb148-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb148-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bb148-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bb148-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="bb148-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb148-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bb148-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb148-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb148-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb148-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb148-127"><dt>Scanprofileui. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb148-127"><dt>Scanprofileui.h</dt></span></span> </dl>  |
| <span data-ttu-id="bb148-128">IDL</span><span class="sxs-lookup"><span data-stu-id="bb148-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bb148-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bb148-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb148-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb148-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb148-131">**IScanProfileUI**</span><span class="sxs-lookup"><span data-stu-id="bb148-131">**IScanProfileUI**</span></span>](-wia-iscanprofileui.md)
</dt> <dt>

[<span data-ttu-id="bb148-132">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="bb148-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




