---
description: El método FileVersion del objeto Installer devuelve la cadena de versión o la cadena de idioma de la ruta de acceso especificada en path con el formato en el que el instalador espera encontrarlos en la base de datos.
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Installer. FileVersion (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileVersion
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a36a92b42815a1b2df913ba6bd9f687cdd1b609b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653332"
---
# <a name="installerfileversion-method"></a><span data-ttu-id="32aee-103">Installer. FileVersion (método)</span><span class="sxs-lookup"><span data-stu-id="32aee-103">Installer.FileVersion method</span></span>

<span data-ttu-id="32aee-104">El método **fileversion** del objeto [**Installer**](installer-object.md) devuelve la cadena de versión o la cadena de idioma de la ruta de acceso especificada en *path* con el formato en el que el instalador espera encontrarlos en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="32aee-104">The **FileVersion** method of the [**Installer**](installer-object.md) object returns the version string or language string of the path specified in *Path* using the format in which the installer expects to find them in the database.</span></span> <span data-ttu-id="32aee-105">En el caso de las versiones, se trata de una cadena con el \# formato ". \# . \# . \# ".</span><span class="sxs-lookup"><span data-stu-id="32aee-105">For versions, this is a string in "\#.\#.\#.\#" format.</span></span> <span data-ttu-id="32aee-106">En idioma, es el identificador de idioma decimal.</span><span class="sxs-lookup"><span data-stu-id="32aee-106">For language, this is the decimal language ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="32aee-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32aee-107">Syntax</span></span>


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a><span data-ttu-id="32aee-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32aee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32aee-109">*Ruta de acceso*</span><span class="sxs-lookup"><span data-stu-id="32aee-109">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="32aee-110">Cadena requerida que contiene la ruta de acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="32aee-110">Required string containing the path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="32aee-111">*Lenguaje*</span><span class="sxs-lookup"><span data-stu-id="32aee-111">*Language*</span></span> 
</dt> <dd>

<span data-ttu-id="32aee-112">Marca que designa si el valor devuelto es un identificador de idioma o una cadena de versión.</span><span class="sxs-lookup"><span data-stu-id="32aee-112">Flag for designating whether the returned value is a language ID or version string.</span></span> <span data-ttu-id="32aee-113">TRUE devuelve el idioma, FALSE devuelve la versión.</span><span class="sxs-lookup"><span data-stu-id="32aee-113">TRUE returns the language, FALSE returns the version.</span></span> <span data-ttu-id="32aee-114">Este parámetro es opcional y su valor predeterminado es FALSE.</span><span class="sxs-lookup"><span data-stu-id="32aee-114">This parameter is optional, with a default value of FALSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32aee-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32aee-115">Return value</span></span>

<span data-ttu-id="32aee-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="32aee-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="32aee-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32aee-117">Requirements</span></span>



| <span data-ttu-id="32aee-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="32aee-118">Requirement</span></span> | <span data-ttu-id="32aee-119">Value</span><span class="sxs-lookup"><span data-stu-id="32aee-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32aee-120">Versión</span><span class="sxs-lookup"><span data-stu-id="32aee-120">Version</span></span><br/> | <span data-ttu-id="32aee-121">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="32aee-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="32aee-122">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="32aee-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="32aee-123">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="32aee-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="32aee-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32aee-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="32aee-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32aee-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="32aee-126">IID</span><span class="sxs-lookup"><span data-stu-id="32aee-126">IID</span></span><br/>     | <span data-ttu-id="32aee-127">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="32aee-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




