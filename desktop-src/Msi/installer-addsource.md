---
description: El método AddSource del objeto de instalador agrega un origen a la lista de orígenes de red válidos en el SourceList.
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: Instalador. AddSource (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3067ae287311c6ed26b509545523db75a3fed4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653624"
---
# <a name="installeraddsource-method"></a><span data-ttu-id="cb128-103">Instalador. AddSource (método)</span><span class="sxs-lookup"><span data-stu-id="cb128-103">Installer.AddSource method</span></span>

<span data-ttu-id="cb128-104">El método **AddSource** del objeto de [**instalador**](installer-object.md) agrega un origen a la lista de orígenes de red válidos en el SourceList.</span><span class="sxs-lookup"><span data-stu-id="cb128-104">The **AddSource** method of the [**Installer**](installer-object.md) object adds a source to the list of valid network sources in the sourcelist.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb128-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb128-105">Syntax</span></span>


```JScript
Installer.AddSource(
  Product,
  User,
  Source
)
```



## <a name="parameters"></a><span data-ttu-id="cb128-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb128-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb128-107">*Producto*</span><span class="sxs-lookup"><span data-stu-id="cb128-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="cb128-108">Especifica el código de producto.</span><span class="sxs-lookup"><span data-stu-id="cb128-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="cb128-109">*User*</span><span class="sxs-lookup"><span data-stu-id="cb128-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="cb128-110">Nombre de usuario para la instalación por usuario; cadena nula o vacía para la instalación por máquina.</span><span class="sxs-lookup"><span data-stu-id="cb128-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> <dt>

<span data-ttu-id="cb128-111">*Origen*</span><span class="sxs-lookup"><span data-stu-id="cb128-111">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="cb128-112">Puntero a la cadena que especifica el origen.</span><span class="sxs-lookup"><span data-stu-id="cb128-112">Pointer to the string specifying the source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb128-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb128-113">Return value</span></span>

<span data-ttu-id="cb128-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cb128-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb128-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb128-115">Requirements</span></span>



| <span data-ttu-id="cb128-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb128-116">Requirement</span></span> | <span data-ttu-id="cb128-117">Value</span><span class="sxs-lookup"><span data-stu-id="cb128-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb128-118">Versión</span><span class="sxs-lookup"><span data-stu-id="cb128-118">Version</span></span><br/> | <span data-ttu-id="cb128-119">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb128-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cb128-120">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cb128-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cb128-121">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb128-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="cb128-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb128-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="cb128-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb128-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="cb128-124">IID</span><span class="sxs-lookup"><span data-stu-id="cb128-124">IID</span></span><br/>     | <span data-ttu-id="cb128-125">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="cb128-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="cb128-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb128-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb128-127">**MsiSourceListAddSource**</span><span class="sxs-lookup"><span data-stu-id="cb128-127">**MsiSourceListAddSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[<span data-ttu-id="cb128-128">resistencia de origen</span><span class="sxs-lookup"><span data-stu-id="cb128-128">source resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




