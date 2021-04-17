---
description: El método ViewDialog del objeto UIPreview muestra un cuadro de diálogo de interfaz de usuario creado almacenado en la base de datos actual.
ms.assetid: 5bc935ac-38ca-4a51-a1dc-6879dee97b05
title: UIPreview. ViewDialog, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewDialog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d9ad3772ced2dba952a3d3b068aaa307d1c06398
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679279"
---
# <a name="uipreviewviewdialog-method"></a><span data-ttu-id="f8d67-103">UIPreview. ViewDialog, método</span><span class="sxs-lookup"><span data-stu-id="f8d67-103">UIPreview.ViewDialog method</span></span>

<span data-ttu-id="f8d67-104">El método **ViewDialog** del objeto [**UIPreview**](uipreview-object.md) muestra un cuadro de diálogo de interfaz de usuario creado almacenado en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="f8d67-104">The **ViewDialog** method of the [**UIPreview**](uipreview-object.md) object displays an authored user interface dialog box stored in the current database.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8d67-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8d67-105">Syntax</span></span>


```JScript
UIPreview.ViewDialog(
  dialog
)
```



## <a name="parameters"></a><span data-ttu-id="f8d67-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8d67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8d67-107">*diálogo*</span><span class="sxs-lookup"><span data-stu-id="f8d67-107">*dialog*</span></span> 
</dt> <dd>

<span data-ttu-id="f8d67-108">Nombre necesario del cuadro de diálogo, con distinción de mayúsculas y minúsculas, y la clave principal de la tabla de base de datos de cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f8d67-108">Required name of the dialog box, case-sensitive, and the primary key of the Dialog database table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8d67-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8d67-109">Return value</span></span>

<span data-ttu-id="f8d67-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f8d67-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8d67-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8d67-111">Requirements</span></span>



| <span data-ttu-id="f8d67-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8d67-112">Requirement</span></span> | <span data-ttu-id="f8d67-113">Value</span><span class="sxs-lookup"><span data-stu-id="f8d67-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d67-114">Versión</span><span class="sxs-lookup"><span data-stu-id="f8d67-114">Version</span></span><br/> | <span data-ttu-id="f8d67-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f8d67-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f8d67-116">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f8d67-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f8d67-117">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="f8d67-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f8d67-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8d67-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="f8d67-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8d67-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f8d67-120">IID</span><span class="sxs-lookup"><span data-stu-id="f8d67-120">IID</span></span><br/>     | <span data-ttu-id="f8d67-121">IID \_ IUIPreview se define como 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f8d67-121">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




