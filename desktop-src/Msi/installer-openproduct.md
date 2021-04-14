---
description: El método OpenProduct del objeto Installer abre un paquete de instalador para un producto instalado mediante el código de producto y devuelve un objeto de sesión.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Instalador. OpenProduct (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9fd25a1f204a6d42cd4cb6e330d7d69da2cddb07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653899"
---
# <a name="installeropenproduct-method"></a><span data-ttu-id="1ef17-103">Instalador. OpenProduct (método)</span><span class="sxs-lookup"><span data-stu-id="1ef17-103">Installer.OpenProduct method</span></span>

<span data-ttu-id="1ef17-104">El método **OpenProduct** del objeto [**Installer**](installer-object.md) abre un paquete de instalador para un producto instalado mediante el código de producto y devuelve un objeto de [**sesión**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="1ef17-104">The **OpenProduct** method of the [**Installer**](installer-object.md) object opens an installer package for an installed product using the product code and returns a [**Session**](session-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ef17-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ef17-105">Syntax</span></span>


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a><span data-ttu-id="1ef17-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ef17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ef17-107">*productCode*</span><span class="sxs-lookup"><span data-stu-id="1ef17-107">*productCode*</span></span> 
</dt> <dd>

<span data-ttu-id="1ef17-108">Cadena requerida que contiene el código de producto único (un [GUID](guid.md)) o un descriptor de activación escrito por el instalador.</span><span class="sxs-lookup"><span data-stu-id="1ef17-108">Required string containing the unique product code (a [GUID](guid.md)) or an activation descriptor written by the installer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ef17-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ef17-109">Return value</span></span>

<span data-ttu-id="1ef17-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1ef17-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ef17-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ef17-111">Remarks</span></span>

<span data-ttu-id="1ef17-112">Tenga en cuenta que solo un único proceso puede abrir un objeto de [**sesión**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="1ef17-112">Note that only one [**Session**](session-object.md) object can be opened by a single process.</span></span> <span data-ttu-id="1ef17-113">**OpenProduct** no se puede usar en una acción personalizada porque la instalación activa es la única sesión permitida.</span><span class="sxs-lookup"><span data-stu-id="1ef17-113">**OpenProduct** cannot be used in a custom action because the active installation is the only session allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ef17-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ef17-114">Requirements</span></span>



| <span data-ttu-id="1ef17-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ef17-115">Requirement</span></span> | <span data-ttu-id="1ef17-116">Value</span><span class="sxs-lookup"><span data-stu-id="1ef17-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef17-117">Versión</span><span class="sxs-lookup"><span data-stu-id="1ef17-117">Version</span></span><br/> | <span data-ttu-id="1ef17-118">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1ef17-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1ef17-119">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1ef17-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1ef17-120">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="1ef17-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1ef17-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1ef17-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="1ef17-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ef17-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1ef17-123">IID</span><span class="sxs-lookup"><span data-stu-id="1ef17-123">IID</span></span><br/>     | <span data-ttu-id="1ef17-124">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1ef17-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




