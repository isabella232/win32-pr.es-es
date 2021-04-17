---
description: El método InstallProduct del objeto Installer abre un paquete del instalador e inicializa una sesión de instalación.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Instalador. InstallProduct (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.InstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 08bab1081aae186b40494cff777163679847b44b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653328"
---
# <a name="installerinstallproduct-method"></a><span data-ttu-id="41b32-103">Instalador. InstallProduct (método)</span><span class="sxs-lookup"><span data-stu-id="41b32-103">Installer.InstallProduct method</span></span>

<span data-ttu-id="41b32-104">El método **InstallProduct** del objeto [**Installer**](installer-object.md) abre un paquete del instalador e inicializa una sesión de instalación.</span><span class="sxs-lookup"><span data-stu-id="41b32-104">The **InstallProduct** method of the [**Installer**](installer-object.md) object opens an installer package and initializes an install session.</span></span>

## <a name="syntax"></a><span data-ttu-id="41b32-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41b32-105">Syntax</span></span>


```JScript
Installer.InstallProduct(
  packagePath,
  propertyValues
)
```



## <a name="parameters"></a><span data-ttu-id="41b32-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41b32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41b32-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="41b32-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="41b32-108">Cadena requerida que contiene la ruta de acceso al paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="41b32-108">Required string containing the path to the install package.</span></span>

</dd> <dt>

<span data-ttu-id="41b32-109">*propertyValues*</span><span class="sxs-lookup"><span data-stu-id="41b32-109">*propertyValues*</span></span> 
</dt> <dd>

<span data-ttu-id="41b32-110">Cadena opcional que contiene pares propiedad = valor separados por espacios en blanco.</span><span class="sxs-lookup"><span data-stu-id="41b32-110">Optional string containing property=value pairs separated by white space.</span></span>

<span data-ttu-id="41b32-111">Para realizar una instalación administrativa, incluya ACTION = ADMIN en *propertyValues*.</span><span class="sxs-lookup"><span data-stu-id="41b32-111">To perform an administrative installation, include ACTION=ADMIN in *propertyValues*.</span></span> <span data-ttu-id="41b32-112">Para obtener más información, vea la propiedad [**acción**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="41b32-112">For more information, see the [**ACTION**](action.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41b32-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41b32-113">Return value</span></span>

<span data-ttu-id="41b32-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="41b32-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41b32-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41b32-115">Remarks</span></span>

<span data-ttu-id="41b32-116">Para quitar completamente un producto, establezca REMOVE = ALL en *propertyValues*.</span><span class="sxs-lookup"><span data-stu-id="41b32-116">To completely remove a product, set REMOVE=ALL in *propertyValues*.</span></span> <span data-ttu-id="41b32-117">Para obtener más información, vea [**Remove**](remove.md) Property.</span><span class="sxs-lookup"><span data-stu-id="41b32-117">For more information, see [**REMOVE**](remove.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="41b32-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41b32-118">Requirements</span></span>



| <span data-ttu-id="41b32-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="41b32-119">Requirement</span></span> | <span data-ttu-id="41b32-120">Value</span><span class="sxs-lookup"><span data-stu-id="41b32-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41b32-121">Versión</span><span class="sxs-lookup"><span data-stu-id="41b32-121">Version</span></span><br/> | <span data-ttu-id="41b32-122">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="41b32-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="41b32-123">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="41b32-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="41b32-124">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="41b32-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="41b32-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="41b32-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="41b32-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41b32-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="41b32-127">IID</span><span class="sxs-lookup"><span data-stu-id="41b32-127">IID</span></span><br/>     | <span data-ttu-id="41b32-128">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="41b32-128">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




