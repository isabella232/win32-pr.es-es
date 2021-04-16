---
description: El método EnableUIPreview del objeto de base de datos facilita la creación de cuadros de diálogo e cartelera al proporcionar la compatibilidad necesaria para ver los cuadros de diálogo de la interfaz de usuario almacenados en la base de datos del instalador.
ms.assetid: c4687de7-8ab4-4377-ac5c-1fed7c915519
title: Database. EnableUIPreview (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.EnableUIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1224bb100e0403e8df9f3bdb0cc0b5dbe017233f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671452"
---
# <a name="databaseenableuipreview-method"></a><span data-ttu-id="949d7-103">Database. EnableUIPreview (método)</span><span class="sxs-lookup"><span data-stu-id="949d7-103">Database.EnableUIPreview method</span></span>

<span data-ttu-id="949d7-104">El método **EnableUIPreview** del objeto de [**base de datos**](database-object.md) facilita la creación de cuadros de diálogo e cartelera al proporcionar la compatibilidad necesaria para ver los cuadros de diálogo de la interfaz de usuario almacenados en la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="949d7-104">The **EnableUIPreview** method of the [**Database**](database-object.md) object facilitates the authoring of dialog boxes and billboards by providing the support needed to view user interface dialog boxes stored in the installer database.</span></span> <span data-ttu-id="949d7-105">El método inicia el modo de vista previa devolviendo un objeto de **base de datos** de vista previa.</span><span class="sxs-lookup"><span data-stu-id="949d7-105">The method starts the preview mode by returning a preview **Database** object.</span></span> <span data-ttu-id="949d7-106">El modo de vista previa finaliza cuando se libera el objeto de vista previa.</span><span class="sxs-lookup"><span data-stu-id="949d7-106">The preview mode ends when the preview object is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="949d7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="949d7-107">Syntax</span></span>


```JScript
Database.EnableUIPreview()
```



## <a name="parameters"></a><span data-ttu-id="949d7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="949d7-108">Parameters</span></span>

<span data-ttu-id="949d7-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="949d7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="949d7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="949d7-110">Return value</span></span>

<span data-ttu-id="949d7-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="949d7-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="949d7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="949d7-112">Requirements</span></span>



| <span data-ttu-id="949d7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="949d7-113">Requirement</span></span> | <span data-ttu-id="949d7-114">Value</span><span class="sxs-lookup"><span data-stu-id="949d7-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="949d7-115">Versión</span><span class="sxs-lookup"><span data-stu-id="949d7-115">Version</span></span><br/> | <span data-ttu-id="949d7-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="949d7-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="949d7-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="949d7-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="949d7-118">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="949d7-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="949d7-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="949d7-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="949d7-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="949d7-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="949d7-121">IID</span><span class="sxs-lookup"><span data-stu-id="949d7-121">IID</span></span><br/>     | <span data-ttu-id="949d7-122">IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="949d7-122">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




