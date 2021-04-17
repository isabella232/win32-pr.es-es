---
description: El método ClearSourceList del objeto Installer quita todos los orígenes de red de la lista de origen.
ms.assetid: a4e4beb2-a4d7-48e7-9c8d-dd1ae19fe92a
title: Instalador. ClearSourceList (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClearSourceList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f9468775c75533b766a160a390410908d04bf6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653538"
---
# <a name="installerclearsourcelist-method"></a><span data-ttu-id="11337-103">Instalador. ClearSourceList (método)</span><span class="sxs-lookup"><span data-stu-id="11337-103">Installer.ClearSourceList method</span></span>

<span data-ttu-id="11337-104">El método **ClearSourceList** del objeto [**Installer**](installer-object.md) quita todos los orígenes de red de la lista de origen.</span><span class="sxs-lookup"><span data-stu-id="11337-104">The **ClearSourceList** method of the [**Installer**](installer-object.md) object removes all network sources from the source list.</span></span>

## <a name="syntax"></a><span data-ttu-id="11337-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11337-105">Syntax</span></span>


```JScript
Installer.ClearSourceList(
  Product,
  User
)
```



## <a name="parameters"></a><span data-ttu-id="11337-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11337-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11337-107">*Producto*</span><span class="sxs-lookup"><span data-stu-id="11337-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="11337-108">Especifica el código de producto.</span><span class="sxs-lookup"><span data-stu-id="11337-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="11337-109">*User*</span><span class="sxs-lookup"><span data-stu-id="11337-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="11337-110">Nombre de usuario para la instalación por usuario; cadena nula o vacía para la instalación por máquina.</span><span class="sxs-lookup"><span data-stu-id="11337-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11337-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11337-111">Return value</span></span>

<span data-ttu-id="11337-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="11337-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="11337-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11337-113">Requirements</span></span>



| <span data-ttu-id="11337-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="11337-114">Requirement</span></span> | <span data-ttu-id="11337-115">Value</span><span class="sxs-lookup"><span data-stu-id="11337-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11337-116">Versión</span><span class="sxs-lookup"><span data-stu-id="11337-116">Version</span></span><br/> | <span data-ttu-id="11337-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="11337-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="11337-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="11337-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="11337-119">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="11337-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="11337-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="11337-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="11337-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11337-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="11337-122">IID</span><span class="sxs-lookup"><span data-stu-id="11337-122">IID</span></span><br/>     | <span data-ttu-id="11337-123">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="11337-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="11337-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="11337-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11337-125">**MsiSourceListClearAll**</span><span class="sxs-lookup"><span data-stu-id="11337-125">**MsiSourceListClearAll**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)
</dt> <dt>

[<span data-ttu-id="11337-126">Resistencia de origen</span><span class="sxs-lookup"><span data-stu-id="11337-126">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




