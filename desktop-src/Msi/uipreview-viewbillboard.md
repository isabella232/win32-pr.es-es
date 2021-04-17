---
description: El método ViewBillboard del objeto UIPreview muestra una cartelera creada mediante el control host del cuadro de diálogo que se muestra actualmente.
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: UIPreview. ViewBillboard, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewBillboard
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9cf1c6ee2a47fdb246fcc847627bb63432b8a67f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653606"
---
# <a name="uipreviewviewbillboard-method"></a><span data-ttu-id="19003-103">UIPreview. ViewBillboard, método</span><span class="sxs-lookup"><span data-stu-id="19003-103">UIPreview.ViewBillboard method</span></span>

<span data-ttu-id="19003-104">El método **ViewBillboard** del objeto [**UIPreview**](uipreview-object.md) muestra una cartelera creada mediante el control host del cuadro de diálogo que se muestra actualmente.</span><span class="sxs-lookup"><span data-stu-id="19003-104">The **ViewBillboard** method of the [**UIPreview**](uipreview-object.md) object displays an authored billboard using the host control in the currently displayed dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="19003-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19003-105">Syntax</span></span>


```JScript
UIPreview.ViewBillboard(
  control,
  billboard
)
```



## <a name="parameters"></a><span data-ttu-id="19003-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19003-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19003-107">*control*</span><span class="sxs-lookup"><span data-stu-id="19003-107">*control*</span></span> 
</dt> <dd>

<span data-ttu-id="19003-108">Nombre necesario del control que hospeda la cartelera, con distinción de mayúsculas y minúsculas, junto con el cuadro de diálogo y las claves principales de la tabla de base de datos de control.</span><span class="sxs-lookup"><span data-stu-id="19003-108">Required name of the control hosting the billboard, case-sensitive, along with the dialog box, and the primary keys of the Control database table.</span></span>

</dd> <dt>

<span data-ttu-id="19003-109">*valla*</span><span class="sxs-lookup"><span data-stu-id="19003-109">*billboard*</span></span> 
</dt> <dd>

<span data-ttu-id="19003-110">Nombre necesario de la cartelera que se va a mostrar mediante el control especificado y el cuadro de diálogo actual, y la clave principal de la tabla de la base de datos de la cartelera.</span><span class="sxs-lookup"><span data-stu-id="19003-110">Required name of the billboard to display using the specified control and current dialog box, and the primary key of the Billboard database table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19003-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19003-111">Return value</span></span>

<span data-ttu-id="19003-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="19003-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="19003-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19003-113">Requirements</span></span>



| <span data-ttu-id="19003-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="19003-114">Requirement</span></span> | <span data-ttu-id="19003-115">Value</span><span class="sxs-lookup"><span data-stu-id="19003-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19003-116">Versión</span><span class="sxs-lookup"><span data-stu-id="19003-116">Version</span></span><br/> | <span data-ttu-id="19003-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="19003-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="19003-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="19003-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="19003-119">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="19003-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="19003-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="19003-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="19003-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19003-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="19003-122">IID</span><span class="sxs-lookup"><span data-stu-id="19003-122">IID</span></span><br/>     | <span data-ttu-id="19003-123">IID \_ IUIPreview se define como 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="19003-123">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




