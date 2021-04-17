---
description: El método de archivo del objeto de instalador utiliza las llamadas de la API Win32 para devolver el tamaño del archivo especificado en la ruta de acceso.
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: Installer. método de archivo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 593319b88e3942ae6caa1399adbe2e596bf6e737
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653333"
---
# <a name="installerfilesize-method"></a><span data-ttu-id="eeb41-103">Installer. método de archivo</span><span class="sxs-lookup"><span data-stu-id="eeb41-103">Installer.FileSize method</span></span>

<span data-ttu-id="eeb41-104">El **método de archivo del** objeto de [**instalador**](installer-object.md) utiliza las llamadas de la API Win32 para devolver el tamaño del archivo especificado en la *ruta de acceso*.</span><span class="sxs-lookup"><span data-stu-id="eeb41-104">The **FileSize** method of the [**Installer**](installer-object.md) object uses Win32 API calls to return the size of the file specified in *Path*.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeb41-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eeb41-105">Syntax</span></span>


```JScript
Installer.FileSize(
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="eeb41-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eeb41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeb41-107">*Ruta de acceso*</span><span class="sxs-lookup"><span data-stu-id="eeb41-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="eeb41-108">Cadena requerida que contiene la ruta de acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="eeb41-108">Required string containing the path to the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeb41-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eeb41-109">Return value</span></span>

<span data-ttu-id="eeb41-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="eeb41-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeb41-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eeb41-111">Requirements</span></span>



| <span data-ttu-id="eeb41-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeb41-112">Requirement</span></span> | <span data-ttu-id="eeb41-113">Value</span><span class="sxs-lookup"><span data-stu-id="eeb41-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb41-114">Versión</span><span class="sxs-lookup"><span data-stu-id="eeb41-114">Version</span></span><br/> | <span data-ttu-id="eeb41-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="eeb41-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="eeb41-116">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eeb41-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="eeb41-117">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="eeb41-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="eeb41-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eeb41-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="eeb41-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeb41-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="eeb41-120">IID</span><span class="sxs-lookup"><span data-stu-id="eeb41-120">IID</span></span><br/>     | <span data-ttu-id="eeb41-121">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="eeb41-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




