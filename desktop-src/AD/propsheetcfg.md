---
title: Estructura PROPSHEETCFG
description: Se usa para contener los datos de configuración de la hoja de propiedades.
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- Active Directory de la estructura PROPSHEETCFG
- Puntero de estructura PPROPSHEETCFG Active Directory
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f4a1186cc756435cc49ed7c81592385faaee60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079408"
---
# <a name="propsheetcfg-structure"></a><span data-ttu-id="b451f-105">Estructura PROPSHEETCFG</span><span class="sxs-lookup"><span data-stu-id="b451f-105">PROPSHEETCFG structure</span></span>

<span data-ttu-id="b451f-106">La estructura **PROPSHEETCFG** se usa para contener los datos de configuración de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b451f-106">The **PROPSHEETCFG** structure is used to contain property sheet configuration data.</span></span> <span data-ttu-id="b451f-107">Esta estructura se incluye en el formato del portapapeles [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="b451f-107">This structure is contained in the [**CFSTR\_DS\_PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) clipboard format.</span></span>

> [!Note]  
> <span data-ttu-id="b451f-108">Esta estructura no está definida en un archivo de encabezado publicado.</span><span class="sxs-lookup"><span data-stu-id="b451f-108">This structure is not defined in a published header file.</span></span> <span data-ttu-id="b451f-109">Para usar esta estructura, debe definirla usted mismo en el formato exacto que se muestra.</span><span class="sxs-lookup"><span data-stu-id="b451f-109">To use this structure, you must define it yourself in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b451f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b451f-110">Syntax</span></span>


```C++
typedef struct {
  LONG_PTR lNotifyHandle;
  HWND     hwndParentSheet;
  HWND     hwndHidden;
  WPARAM   wParamSheetClose;
} PROPSHEETCFG, *PPROPSHEETCFG;
```



## <a name="members"></a><span data-ttu-id="b451f-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b451f-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="b451f-112">**lNotifyHandle**</span><span class="sxs-lookup"><span data-stu-id="b451f-112">**lNotifyHandle**</span></span>
</dt> <dd>

<span data-ttu-id="b451f-113">Contiene el identificador de notificación.</span><span class="sxs-lookup"><span data-stu-id="b451f-113">Contains the notification handle.</span></span> <span data-ttu-id="b451f-114">Es idéntico al identificador pasado para el parámetro *Handle* en el método [**IExtendPropertySheet2:: CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b451f-114">This is identical to the handle passed for the *handle* parameter in the [**IExtendPropertySheet2::CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) method.</span></span>

</dd> <dt>

<span data-ttu-id="b451f-115">**hwndParentSheet**</span><span class="sxs-lookup"><span data-stu-id="b451f-115">**hwndParentSheet**</span></span>
</dt> <dd>

<span data-ttu-id="b451f-116">Contiene el identificador de ventana de la hoja de propiedades primaria.</span><span class="sxs-lookup"><span data-stu-id="b451f-116">Contains the window handle of the parent property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="b451f-117">**hwndHidden**</span><span class="sxs-lookup"><span data-stu-id="b451f-117">**hwndHidden**</span></span>
</dt> <dd>

<span data-ttu-id="b451f-118">Contiene el identificador de la ventana oculta.</span><span class="sxs-lookup"><span data-stu-id="b451f-118">Contains the handle of the hidden window.</span></span>

</dd> <dt>

<span data-ttu-id="b451f-119">**wParamSheetClose**</span><span class="sxs-lookup"><span data-stu-id="b451f-119">**wParamSheetClose**</span></span>
</dt> <dd>

<span data-ttu-id="b451f-120">Contiene un valor de 32 bits definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b451f-120">Contains an application-defined 32-bit value.</span></span> <span data-ttu-id="b451f-121">Este valor se devuelve a la aplicación en el *wParam* del mensaje de [**notificación de cierre de la \_ \_ hoja \_ \_ DSA de WM**](wm-dsa-sheet-close-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b451f-121">This value is passed back to the application in the *wParam* of the [**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**](wm-dsa-sheet-close-notify.md) message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b451f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b451f-122">Requirements</span></span>



| <span data-ttu-id="b451f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b451f-123">Requirement</span></span> | <span data-ttu-id="b451f-124">Value</span><span class="sxs-lookup"><span data-stu-id="b451f-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b451f-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b451f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b451f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b451f-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b451f-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b451f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b451f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b451f-128">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b451f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b451f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b451f-130">**CFSTR \_ DS \_ PROPSHEETCONFIG**</span><span class="sxs-lookup"><span data-stu-id="b451f-130">**CFSTR\_DS\_PROPSHEETCONFIG**</span></span>](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[<span data-ttu-id="b451f-131">**\_notificación de \_ cierre de hoja DSA \_ de WM \_**</span><span class="sxs-lookup"><span data-stu-id="b451f-131">**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**</span></span>](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 

