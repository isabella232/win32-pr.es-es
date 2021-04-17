---
description: La propiedad SourcePath del objeto de sesión es una propiedad de solo lectura que proporciona la ruta de acceso completa a la carpeta designada en el medio de origen o la imagen del servidor.
ms.assetid: ed8eea4f-e15e-4d56-ac0c-e18f9cb46d07
title: Session. SourcePath (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SourcePath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a868e68e26f28d4fc2137e735ddc6d4c6ab0066
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681123"
---
# <a name="sessionsourcepath-property"></a><span data-ttu-id="f20a3-103">Session. SourcePath (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f20a3-103">Session.SourcePath property</span></span>

<span data-ttu-id="f20a3-104">La propiedad **SourcePath** del objeto de [**sesión**](session-object.md) es una propiedad de solo lectura que proporciona la ruta de acceso completa a la carpeta designada en el medio de origen o la imagen del servidor.</span><span class="sxs-lookup"><span data-stu-id="f20a3-104">The **SourcePath** property of the [**Session**](session-object.md) object is a read-only property that provides the full path to the designated folder on the source media or server image.</span></span>

<span data-ttu-id="f20a3-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f20a3-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f20a3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f20a3-106">Syntax</span></span>


```JScript
propVal = Session.SourcePath
```



## <a name="property-value"></a><span data-ttu-id="f20a3-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f20a3-107">Property value</span></span>

<span data-ttu-id="f20a3-108">Nombre obligatorio que distingue entre mayúsculas y minúsculas de una propiedad de carpeta según lo especificado por una clave principal de la [tabla de directorio](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="f20a3-108">Required case-sensitive name of a folder property as specified by a primary key of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="f20a3-109">Si la carpeta no existe, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="f20a3-109">An error is generated if the folder does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="f20a3-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f20a3-110">Remarks</span></span>

<span data-ttu-id="f20a3-111">Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="f20a3-111">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f20a3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f20a3-112">Requirements</span></span>



| <span data-ttu-id="f20a3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f20a3-113">Requirement</span></span> | <span data-ttu-id="f20a3-114">Value</span><span class="sxs-lookup"><span data-stu-id="f20a3-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f20a3-115">Versión</span><span class="sxs-lookup"><span data-stu-id="f20a3-115">Version</span></span><br/> | <span data-ttu-id="f20a3-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f20a3-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f20a3-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f20a3-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f20a3-118">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="f20a3-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f20a3-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f20a3-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="f20a3-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f20a3-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f20a3-121">IID</span><span class="sxs-lookup"><span data-stu-id="f20a3-121">IID</span></span><br/>     | <span data-ttu-id="f20a3-122">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f20a3-122">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




