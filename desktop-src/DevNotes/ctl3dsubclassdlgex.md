---
description: Subclases de todos los controles de un cuadro de diálogo y de la propia ventana de diálogo.
ms.assetid: 4d3c298b-07ba-4668-badd-dddecc389e70
title: Ctl3dSubclassDlgEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassDlgEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 6e29f65d5ddc3d0d9a7de05eef88b7a662e0e43f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650119"
---
# <a name="ctl3dsubclassdlgex-function"></a><span data-ttu-id="6ad9b-103">Ctl3dSubclassDlgEx función)</span><span class="sxs-lookup"><span data-stu-id="6ad9b-103">Ctl3dSubclassDlgEx function</span></span>

<span data-ttu-id="6ad9b-104">Subclases de todos los controles de un cuadro de diálogo y de la propia ventana de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-104">Subclasses all controls in a dialog box and in the dialog window itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ad9b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ad9b-105">Syntax</span></span>


```C++
PUBLIC BOOL FAR PASCAL Ctl3dSubclassDlgEx(
   HWND  hwndDlg,
   DWORD grbit
);
```



## <a name="parameters"></a><span data-ttu-id="6ad9b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ad9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ad9b-107">*hwndDlg*</span><span class="sxs-lookup"><span data-stu-id="6ad9b-107">*hwndDlg*</span></span> 
</dt> <dd>

<span data-ttu-id="6ad9b-108">Identificador de la ventana de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-108">A handle to the dialog window.</span></span>

</dd> <dt>

<span data-ttu-id="6ad9b-109">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6ad9b-109">*grbit*</span></span> 
</dt> <dd>

<span data-ttu-id="6ad9b-110">Tipos de control de los que se van a crear subclases.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-110">The control types to be subclassed.</span></span> <span data-ttu-id="6ad9b-111">Este valor puede ser cualquiera de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-111">This value can be any of the following.</span></span>



| <span data-ttu-id="6ad9b-112">Value</span><span class="sxs-lookup"><span data-stu-id="6ad9b-112">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="6ad9b-113">Significado</span><span class="sxs-lookup"><span data-stu-id="6ad9b-113">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="CTL3D_BUTTONS"></span><span id="ctl3d_buttons"></span><dl> <span data-ttu-id="6ad9b-114"><dt>**CTL3D \_ BOTONES**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="6ad9b-114"><dt>**CTL3D\_BUTTONS**</dt> <dt>0x0001</dt></span></span> </dl>                 | <span data-ttu-id="6ad9b-115">Botones de subclase.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-115">Subclass buttons.</span></span><br/>                  |
| <span id="CTL3D_LISTBOXES"></span><span id="ctl3d_listboxes"></span><dl> <span data-ttu-id="6ad9b-116"><dt>**CTL3D \_ LISTBOXs**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="6ad9b-116"><dt>**CTL3D\_LISTBOXES**</dt> <dt>0x0002</dt></span></span> </dl>           | <span data-ttu-id="6ad9b-117">Cuadros de lista de subclases.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-117">Subclass list boxes.</span></span><br/>               |
| <span id="CTL3D_EDITS"></span><span id="ctl3d_edits"></span><dl> <span data-ttu-id="6ad9b-118"><dt>**CTL3D \_ EDITA**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="6ad9b-118"><dt>**CTL3D\_EDITS**</dt> <dt>0x0004</dt></span></span> </dl>                       | <span data-ttu-id="6ad9b-119">Controles de edición de subclase.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-119">Subclass edit controls.</span></span><br/>            |
| <span id="CTL3D_COMBOS"></span><span id="ctl3d_combos"></span><dl> <span data-ttu-id="6ad9b-120"><dt>**CTL3D \_**</dt> <dt>0x0008</dt> combinados</span><span class="sxs-lookup"><span data-stu-id="6ad9b-120"><dt>**CTL3D\_COMBOS**</dt> <dt>0x0008</dt></span></span> </dl>                    | <span data-ttu-id="6ad9b-121">Cuadros combinados de subclase.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-121">Subclass combo boxes.</span></span><br/>              |
| <span id="CTL3D_STATICTEXTS"></span><span id="ctl3d_statictexts"></span><dl> <span data-ttu-id="6ad9b-122"><dt>**CTL3D \_ STATICTEXTS**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="6ad9b-122"><dt>**CTL3D\_STATICTEXTS**</dt> <dt>0x0010</dt></span></span> </dl>     | <span data-ttu-id="6ad9b-123">Controles de texto estático de subclase.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-123">Subclass static text controls.</span></span><br/>     |
| <span id="CTL3D_STATICFRAMES"></span><span id="ctl3d_staticframes"></span><dl> <span data-ttu-id="6ad9b-124"><dt>**CTL3D \_ STATICFRAMES**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="6ad9b-124"><dt>**CTL3D\_STATICFRAMES**</dt> <dt>0x0020</dt></span></span> </dl>  | <span data-ttu-id="6ad9b-125">Marcos estáticos de subclase.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-125">Subclass static frames.</span></span><br/>            |
| <span id="CTL3D_ALL"></span><span id="ctl3d_all"></span><dl> <span data-ttu-id="6ad9b-126"><dt>**CTL3D \_ TODO**</dt> <dt>0xFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="6ad9b-126"><dt>**CTL3D\_ALL**</dt> <dt>0xffff</dt></span></span> </dl>                             | <span data-ttu-id="6ad9b-127">Subclase de todos los controles.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-127">Subclass all controls.</span></span><br/>             |
| <span id="CTL3D_NODLGWINDOW"></span><span id="ctl3d_nodlgwindow"></span><dl> <span data-ttu-id="6ad9b-128"><dt>**CTL3D \_ NODLGWINDOW**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="6ad9b-128"><dt>**CTL3D\_NODLGWINDOW**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="6ad9b-129">No debe subclaser la ventana de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-129">Do not subclass the dialog window.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ad9b-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ad9b-130">Return value</span></span>

<span data-ttu-id="6ad9b-131">Devuelve **true** si la función se ejecuta correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-131">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ad9b-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ad9b-132">Remarks</span></span>

<span data-ttu-id="6ad9b-133">Esta función es especialmente útil en aplicaciones basadas en C++.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-133">This function is especially useful in applications based on C++.</span></span>

<span data-ttu-id="6ad9b-134">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="6ad9b-134">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ad9b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ad9b-135">Requirements</span></span>



| <span data-ttu-id="6ad9b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ad9b-136">Requirement</span></span> | <span data-ttu-id="6ad9b-137">Value</span><span class="sxs-lookup"><span data-stu-id="6ad9b-137">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ad9b-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ad9b-138">DLL</span></span><br/> | <dl> <span data-ttu-id="6ad9b-139"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ad9b-139"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
