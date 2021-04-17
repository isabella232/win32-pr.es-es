---
description: El método OpenPackage del objeto Installer abre un paquete del instalador para su uso con funciones que tienen acceso a la base de datos del producto e instalan el motor, y devuelven un objeto de sesión.
ms.assetid: 22b03bde-29ae-4dd4-a41c-d55b3a4f424c
title: Instalador. OpenPackage (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenPackage
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 621fac51155b2ac89eba40d39da6d5af6c305e67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653323"
---
# <a name="installeropenpackage-method"></a><span data-ttu-id="fbcb4-103">Instalador. OpenPackage (método)</span><span class="sxs-lookup"><span data-stu-id="fbcb4-103">Installer.OpenPackage method</span></span>

<span data-ttu-id="fbcb4-104">El método **OpenPackage** del objeto [**Installer**](installer-object.md) abre un paquete del instalador para su uso con funciones que tienen acceso a la base de datos del producto e instalan el motor, y devuelven un objeto de [**sesión**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="fbcb4-104">The **OpenPackage** method of the [**Installer**](installer-object.md) object opens an installer package for use with functions that access the product database and install engine, returning an [**Session**](session-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbcb4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fbcb4-105">Syntax</span></span>


```JScript
Installer.OpenPackage(
  packagePath,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="fbcb4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbcb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbcb4-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="fbcb4-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="fbcb4-108">Cadena requerida que contiene el nombre de la ruta de acceso del paquete.</span><span class="sxs-lookup"><span data-stu-id="fbcb4-108">Required string containing the path name of the package.</span></span>

</dd> <dt>

<span data-ttu-id="fbcb4-109">*options*</span><span class="sxs-lookup"><span data-stu-id="fbcb4-109">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="fbcb4-110">Valor entero opcional que especifica si **OpenPackage** debe omitir el estado actual del equipo al crear el objeto de sesión.</span><span class="sxs-lookup"><span data-stu-id="fbcb4-110">An optional integer value that specifies whether or not **OpenPackage** should ignore the current computer state when creating the Session object.</span></span> <span data-ttu-id="fbcb4-111">Ningún valor o un valor de 0 para Options tiene como valor predeterminado el comportamiento original.</span><span class="sxs-lookup"><span data-stu-id="fbcb4-111">No value or a value of 0 for options defaults to the original behavior.</span></span> <span data-ttu-id="fbcb4-112">Cuando Options es 1, el método **OpenPackage** omite el estado actual del equipo al abrir el paquete.</span><span class="sxs-lookup"><span data-stu-id="fbcb4-112">When options is 1, the **OpenPackage** Method ignores the current computer state when opening the package.</span></span> <span data-ttu-id="fbcb4-113">Un valor de 1 impide que se realicen cambios en el estado actual del equipo.</span><span class="sxs-lookup"><span data-stu-id="fbcb4-113">A value of 1 prevents changes to the current computer state.</span></span> <span data-ttu-id="fbcb4-114">Para obtener más información, vea [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span><span class="sxs-lookup"><span data-stu-id="fbcb4-114">For more information, see [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbcb4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fbcb4-115">Return value</span></span>

<span data-ttu-id="fbcb4-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fbcb4-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbcb4-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fbcb4-117">Remarks</span></span>

<span data-ttu-id="fbcb4-118">El método **OpenPackage** puede aceptar el identificador de la base de datos directamente en lugar de la cadena de la ruta de acceso del paquete.</span><span class="sxs-lookup"><span data-stu-id="fbcb4-118">The **OpenPackage** method can accept the database handle directly instead of the string for the package path.</span></span>

<span data-ttu-id="fbcb4-119">Tenga en cuenta que solo un único proceso puede abrir un objeto de [**sesión**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="fbcb4-119">Note that only one [**Session**](session-object.md) object can be opened by a single process.</span></span> <span data-ttu-id="fbcb4-120">**OpenPackage** no se puede usar en una acción personalizada porque la instalación activa es la única sesión permitida.</span><span class="sxs-lookup"><span data-stu-id="fbcb4-120">**OpenPackage** cannot be used in a custom action because the active installation is the only session allowed.</span></span>

<span data-ttu-id="fbcb4-121">Un objeto de [**sesión**](session-object.md) segura omite el estado actual del equipo al abrir el paquete y evita los cambios en el estado actual del equipo.</span><span class="sxs-lookup"><span data-stu-id="fbcb4-121">A safe [**Session**](session-object.md) object ignores the current computer state when opening the package and prevents changes to the current computer state.</span></span> <span data-ttu-id="fbcb4-122">Para obtener más información, vea [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span><span class="sxs-lookup"><span data-stu-id="fbcb4-122">For more information, see [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbcb4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbcb4-123">Requirements</span></span>



| <span data-ttu-id="fbcb4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbcb4-124">Requirement</span></span> | <span data-ttu-id="fbcb4-125">Value</span><span class="sxs-lookup"><span data-stu-id="fbcb4-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbcb4-126">Versión</span><span class="sxs-lookup"><span data-stu-id="fbcb4-126">Version</span></span><br/> | <span data-ttu-id="fbcb4-127">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fbcb4-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fbcb4-128">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fbcb4-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fbcb4-129">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="fbcb4-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="fbcb4-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fbcb4-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="fbcb4-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbcb4-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="fbcb4-132">IID</span><span class="sxs-lookup"><span data-stu-id="fbcb4-132">IID</span></span><br/>     | <span data-ttu-id="fbcb4-133">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fbcb4-133">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




