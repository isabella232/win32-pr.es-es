---
description: El método ForceSourceListResolution del objeto de instalador obliga al Windows Installer a buscar en la lista de origen un origen de producto válido.
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: Instalador. ForceSourceListResolution (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ForceSourceListResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cadc27f3eaa90cd6fb2729f73d07cbcfa1f96b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653329"
---
# <a name="installerforcesourcelistresolution-method"></a><span data-ttu-id="1e9b6-103">Instalador. ForceSourceListResolution (método)</span><span class="sxs-lookup"><span data-stu-id="1e9b6-103">Installer.ForceSourceListResolution method</span></span>

<span data-ttu-id="1e9b6-104">El método **ForceSourceListResolution** del objeto de [**instalador**](installer-object.md) obliga al instalador a buscar en la lista de origen un origen de producto válido la próxima vez que se necesite un origen, por ejemplo, cuando el instalador realiza una instalación o una reinstalación, o cuando necesita la ruta de acceso de un conjunto de componentes para que se ejecute desde el origen.</span><span class="sxs-lookup"><span data-stu-id="1e9b6-104">The **ForceSourceListResolution** method of the [**Installer**](installer-object.md) object forces the installer to search the source list for a valid product source the next time a source is needed, such as when the installer performs an installation or a reinstallation, or when it needs the path for a component set to run from source.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e9b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e9b6-105">Syntax</span></span>


```JScript
Installer.ForceSourceListResolution(
  Product,
  User
)
```



## <a name="parameters"></a><span data-ttu-id="1e9b6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e9b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e9b6-107">*Producto*</span><span class="sxs-lookup"><span data-stu-id="1e9b6-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="1e9b6-108">Especifica el código de producto.</span><span class="sxs-lookup"><span data-stu-id="1e9b6-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="1e9b6-109">*User*</span><span class="sxs-lookup"><span data-stu-id="1e9b6-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="1e9b6-110">Nombre de usuario para la instalación por usuario; cadena nula o vacía para la instalación por máquina.</span><span class="sxs-lookup"><span data-stu-id="1e9b6-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e9b6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e9b6-111">Return value</span></span>

<span data-ttu-id="1e9b6-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1e9b6-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e9b6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e9b6-113">Requirements</span></span>



| <span data-ttu-id="1e9b6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e9b6-114">Requirement</span></span> | <span data-ttu-id="1e9b6-115">Value</span><span class="sxs-lookup"><span data-stu-id="1e9b6-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e9b6-116">Versión</span><span class="sxs-lookup"><span data-stu-id="1e9b6-116">Version</span></span><br/> | <span data-ttu-id="1e9b6-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1e9b6-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1e9b6-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1e9b6-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1e9b6-119">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e9b6-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1e9b6-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e9b6-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="1e9b6-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b6-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1e9b6-122">IID</span><span class="sxs-lookup"><span data-stu-id="1e9b6-122">IID</span></span><br/>     | <span data-ttu-id="1e9b6-123">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1e9b6-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="1e9b6-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e9b6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e9b6-125">**MsiSourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="1e9b6-125">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="1e9b6-126">Resistencia de origen</span><span class="sxs-lookup"><span data-stu-id="1e9b6-126">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




