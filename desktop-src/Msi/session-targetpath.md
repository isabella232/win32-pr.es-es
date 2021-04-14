---
description: La propiedad TargetPath del objeto de sesión es una propiedad de lectura y escritura que proporciona la ruta de acceso completa a la carpeta designada en la unidad de destino de la instalación.
ms.assetid: 563b874e-c669-4f5b-b3fa-eeb6b6e578f2
title: Session. TargetPath (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.TargetPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6c5917f845da0eec944e797d5f49f52d0ec26913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653971"
---
# <a name="sessiontargetpath-property"></a><span data-ttu-id="953b0-103">Session. TargetPath (propiedad)</span><span class="sxs-lookup"><span data-stu-id="953b0-103">Session.TargetPath property</span></span>

<span data-ttu-id="953b0-104">La propiedad **TargetPath** del objeto de [**sesión**](session-object.md) es una propiedad de lectura y escritura que proporciona la ruta de acceso completa a la carpeta designada en la unidad de destino de la instalación.</span><span class="sxs-lookup"><span data-stu-id="953b0-104">The **TargetPath** property of the [**Session**](session-object.md) object is a read-write property that provides the full path to the designated folder on the installation target drive.</span></span>

<span data-ttu-id="953b0-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="953b0-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="953b0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="953b0-106">Syntax</span></span>


```JScript
propVal = Session.TargetPath
Session.TargetPath = propVal 
```



## <a name="property-value"></a><span data-ttu-id="953b0-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="953b0-107">Property value</span></span>

<span data-ttu-id="953b0-108">Nombre obligatorio que distingue entre mayúsculas y minúsculas de una propiedad de carpeta según lo especificado por una clave principal de la [tabla de directorio](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="953b0-108">Required case-sensitive name of a folder property as specified by a primary key of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="953b0-109">Si la carpeta no existe, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="953b0-109">An error is generated if the folder does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="953b0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="953b0-110">Remarks</span></span>

<span data-ttu-id="953b0-111">No intente configurar la ruta de acceso de destino si los componentes que usan esas rutas ya están instalados para el usuario actual o para otro usuario.</span><span class="sxs-lookup"><span data-stu-id="953b0-111">Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user.</span></span> <span data-ttu-id="953b0-112">Compruebe la propiedad [**ProductState**](productstate.md) para determinar si el producto que contiene el componente está instalado.</span><span class="sxs-lookup"><span data-stu-id="953b0-112">Check the [**ProductState**](productstate.md) property to determine if the product that contains the component is installed.</span></span>

<span data-ttu-id="953b0-113">Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="953b0-113">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="953b0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="953b0-114">Requirements</span></span>



| <span data-ttu-id="953b0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="953b0-115">Requirement</span></span> | <span data-ttu-id="953b0-116">Value</span><span class="sxs-lookup"><span data-stu-id="953b0-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="953b0-117">Versión</span><span class="sxs-lookup"><span data-stu-id="953b0-117">Version</span></span><br/> | <span data-ttu-id="953b0-118">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="953b0-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="953b0-119">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="953b0-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="953b0-120">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="953b0-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="953b0-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="953b0-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="953b0-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="953b0-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="953b0-123">IID</span><span class="sxs-lookup"><span data-stu-id="953b0-123">IID</span></span><br/>     | <span data-ttu-id="953b0-124">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="953b0-124">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




