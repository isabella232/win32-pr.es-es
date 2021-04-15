---
description: El \_ comando de \_ WPD \_ \_ \_ de extensión de proveedor ext Get Vendor \_ Extension \_ Description recupera la cadena de descripción de extensión de proveedor. Esta cadena se define mediante un conjunto de DeviceInfo.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: Comando WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b98d5b8bce699537bc261e915d8233be6082c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709028"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a><span data-ttu-id="72e3e-104">Comando de WPD comando \_ \_ \_ ext \_ get de \_ extensión de proveedor \_ \_</span><span class="sxs-lookup"><span data-stu-id="72e3e-104">WPD\_COMMAND\_MTP\_EXT\_GET\_VENDOR\_EXTENSION\_DESCRIPTION Command</span></span>

<span data-ttu-id="72e3e-105">El comando de **WPD de \_ extensión de \_ \_ \_ proveedor ext Get \_ Vendor \_ Extension \_ Description** recupera la cadena de descripción de extensión de proveedor.</span><span class="sxs-lookup"><span data-stu-id="72e3e-105">The **WPD\_COMMAND\_MTP\_EXT\_GET\_VENDOR\_EXTENSION\_DESCRIPTION** command retrieves the vendor-extension description string.</span></span> <span data-ttu-id="72e3e-106">Esta cadena se define mediante un conjunto de **DeviceInfo** .</span><span class="sxs-lookup"><span data-stu-id="72e3e-106">This string is defined by a **DeviceInfo** dataset.</span></span>

## <a name="command-category"></a><span data-ttu-id="72e3e-107">Categoría de comando</span><span class="sxs-lookup"><span data-stu-id="72e3e-107">Command category</span></span>

<span data-ttu-id="72e3e-108">**Categoría de WPD de \_ \_ \_ operaciones de proveedor ext MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="72e3e-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="72e3e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72e3e-109">Parameters</span></span>

<span data-ttu-id="72e3e-110">Este comando no contiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="72e3e-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72e3e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72e3e-111">Return Value</span></span>

<span data-ttu-id="72e3e-112">El controlador devuelve los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="72e3e-112">The driver returns the following results.</span></span>



| <span data-ttu-id="72e3e-113">Resultado</span><span class="sxs-lookup"><span data-stu-id="72e3e-113">Result</span></span>                                                      | <span data-ttu-id="72e3e-114">VarType</span><span class="sxs-lookup"><span data-stu-id="72e3e-114">VarType</span></span>    | <span data-ttu-id="72e3e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="72e3e-115">Description</span></span>                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| <span data-ttu-id="72e3e-116">**propiedad de WPD \_ \_ \_ extensión del proveedor ext de MTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="72e3e-116">**WPD\_PROPERTY\_MTP\_EXT\_VENDOR\_EXTENSION\_DESCRIPTION**</span></span> | <span data-ttu-id="72e3e-117">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="72e3e-117">VT\_LPWSTR</span></span> | <span data-ttu-id="72e3e-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="72e3e-118">Required.</span></span> <span data-ttu-id="72e3e-119">Especifica la cadena de descripción de la extensión de proveedor.</span><span class="sxs-lookup"><span data-stu-id="72e3e-119">Specifies the vendor-extension description string.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="72e3e-120">Llamar a métodos</span><span class="sxs-lookup"><span data-stu-id="72e3e-120">Calling Methods</span></span>

<span data-ttu-id="72e3e-121">Solo se puede llamar directamente mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="72e3e-121">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="72e3e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72e3e-122">Requirements</span></span>



| <span data-ttu-id="72e3e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="72e3e-123">Requirement</span></span> | <span data-ttu-id="72e3e-124">Value</span><span class="sxs-lookup"><span data-stu-id="72e3e-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="72e3e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72e3e-125">Header</span></span><br/> | <dl> <span data-ttu-id="72e3e-126"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="72e3e-126"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72e3e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="72e3e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e3e-128">Compatibilidad con extensiones MTP</span><span class="sxs-lookup"><span data-stu-id="72e3e-128">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




