---
description: El método CollectUserInfo del objeto de instalador invoca una secuencia del Asistente para interfaz de usuario que recopila y almacena la información de usuario y el código de producto.
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: Instalador. CollectUserInfo (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CollectUserInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d7286fdbc9fab6b3db6752284bf86db05f920bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653696"
---
# <a name="installercollectuserinfo-method"></a><span data-ttu-id="ada3c-103">Instalador. CollectUserInfo (método)</span><span class="sxs-lookup"><span data-stu-id="ada3c-103">Installer.CollectUserInfo method</span></span>

<span data-ttu-id="ada3c-104">El método **CollectUserInfo** del objeto de [**instalador**](installer-object.md) invoca una secuencia del Asistente para interfaz de usuario que recopila y almacena la información de usuario y el código de producto.</span><span class="sxs-lookup"><span data-stu-id="ada3c-104">The **CollectUserInfo** method of the [**Installer**](installer-object.md) object invokes a user interface wizard sequence which collects and stores both user information and the product code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ada3c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ada3c-105">Syntax</span></span>


```JScript
Installer.CollectUserInfo(
  Product
)
```



## <a name="parameters"></a><span data-ttu-id="ada3c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ada3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ada3c-107">*Producto*</span><span class="sxs-lookup"><span data-stu-id="ada3c-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="ada3c-108">Especifica el [**código de producto**](productcode.md) del producto.</span><span class="sxs-lookup"><span data-stu-id="ada3c-108">Specifies the [**product code**](productcode.md) of the product.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ada3c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ada3c-109">Return value</span></span>

<span data-ttu-id="ada3c-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ada3c-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ada3c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ada3c-111">Remarks</span></span>

<span data-ttu-id="ada3c-112">Una aplicación debe llamar al método **CollectUserInfo** la primera vez que se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="ada3c-112">An application should call the **CollectUserInfo** method the first time it is run.</span></span> <span data-ttu-id="ada3c-113">El método **CollectUserInfo** abre el paquete de instalación del producto e invoca una secuencia del Asistente para la interfaz de usuario creada que recopila información del usuario.</span><span class="sxs-lookup"><span data-stu-id="ada3c-113">The **CollectUserInfo** method opens the product's installation package and invokes an authored user interface wizard sequence which collects user information.</span></span> <span data-ttu-id="ada3c-114">Una vez finalizada la secuencia del asistente, se registra la información de usuario recopilada.</span><span class="sxs-lookup"><span data-stu-id="ada3c-114">Upon completion of the wizard sequence, the collected user information is registered.</span></span> <span data-ttu-id="ada3c-115">La propiedad [**elemento uilevel**](installer-uilevel.md) debe establecerse en msiUILevelFull porque esta API requiere una interfaz de usuario creada.</span><span class="sxs-lookup"><span data-stu-id="ada3c-115">The [**UILevel**](installer-uilevel.md) property should be set to msiUILevelFull because this API requires an authored user interface.</span></span>

<span data-ttu-id="ada3c-116">El método **CollectUserInfo** invoca el [cuadro de diálogo FirstRun](firstrun-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="ada3c-116">The **CollectUserInfo** method invokes the [FirstRun Dialog](firstrun-dialog.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ada3c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ada3c-117">Requirements</span></span>



| <span data-ttu-id="ada3c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ada3c-118">Requirement</span></span> | <span data-ttu-id="ada3c-119">Value</span><span class="sxs-lookup"><span data-stu-id="ada3c-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ada3c-120">Versión</span><span class="sxs-lookup"><span data-stu-id="ada3c-120">Version</span></span><br/> | <span data-ttu-id="ada3c-121">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ada3c-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ada3c-122">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ada3c-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ada3c-123">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="ada3c-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ada3c-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ada3c-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="ada3c-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ada3c-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ada3c-126">IID</span><span class="sxs-lookup"><span data-stu-id="ada3c-126">IID</span></span><br/>     | <span data-ttu-id="ada3c-127">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ada3c-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="ada3c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ada3c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ada3c-129">**MsiCollectUserInfo**</span><span class="sxs-lookup"><span data-stu-id="ada3c-129">**MsiCollectUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 




