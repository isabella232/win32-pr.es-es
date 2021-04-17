---
description: El comando de WPD de comando de la \_ \_ extensión de código de \_ \_ \_ \_ \_ desbloqueo de comandos de la extensión de código de la extensión de comando No hay ninguna fase de datos subsiguiente asociada a este comando.
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: Comando WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8713c739da98c179ecc2b7bf042905e4fd06ad7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709030"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a><span data-ttu-id="f5668-104">Comando de WPD comando \_ \_ ext de proveedor de \_ \_ \_ \_ códigos de descompatibilidad \_</span><span class="sxs-lookup"><span data-stu-id="f5668-104">WPD\_COMMAND\_MTP\_EXT\_GET\_SUPPORTED\_VENDOR\_OPCODES Command</span></span>

<span data-ttu-id="f5668-105">El comando de WPD de comando de la extensión de código de desbloqueo de comandos de la **\_ extensión de \_ \_ \_ \_ \_ código \_** de la extensión de comando</span><span class="sxs-lookup"><span data-stu-id="f5668-105">The **WPD\_COMMAND\_MTP\_EXT\_GET\_SUPPORTED\_VENDOR\_OPCODES** command sends an MTP command block.</span></span> <span data-ttu-id="f5668-106">No hay ninguna fase de datos subsiguiente asociada a este comando.</span><span class="sxs-lookup"><span data-stu-id="f5668-106">There is no subsequent data phase associated with this command.</span></span>

## <a name="command-category"></a><span data-ttu-id="f5668-107">Categoría de comando</span><span class="sxs-lookup"><span data-stu-id="f5668-107">Command category</span></span>

<span data-ttu-id="f5668-108">**Categoría de WPD de \_ \_ \_ operaciones de proveedor ext MTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f5668-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="f5668-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5668-109">Parameters</span></span>

<span data-ttu-id="f5668-110">Este comando no contiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f5668-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5668-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5668-111">Return Value</span></span>

<span data-ttu-id="f5668-112">El controlador devuelve los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="f5668-112">The driver returns the following results.</span></span>



| <span data-ttu-id="f5668-113">Resultado</span><span class="sxs-lookup"><span data-stu-id="f5668-113">Result</span></span>                                                | <span data-ttu-id="f5668-114">VarType</span><span class="sxs-lookup"><span data-stu-id="f5668-114">VarType</span></span> | <span data-ttu-id="f5668-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5668-115">Description</span></span>                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5668-116">**propiedad de WPD \_ \_ \_ códigos de \_ operación ext VENDOR \_ \_ MTP**</span><span class="sxs-lookup"><span data-stu-id="f5668-116">**WPD\_PROPERTY\_MTP\_EXT\_VENDOR\_OPERATION\_CODES**</span></span> | <span data-ttu-id="f5668-117">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="f5668-117">VT\_UI4</span></span> | <span data-ttu-id="f5668-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f5668-118">Required.</span></span> <span data-ttu-id="f5668-119">Un **IPortableDevicePropVariantCollection** que contiene todos los códigos de operación ampliados por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f5668-119">An **IPortableDevicePropVariantCollection** that contains all vendor-extended operation codes.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="f5668-120">Llamar a métodos</span><span class="sxs-lookup"><span data-stu-id="f5668-120">Calling Methods</span></span>

<span data-ttu-id="f5668-121">Solo se puede llamar directamente mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="f5668-121">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5668-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5668-122">Requirements</span></span>



| <span data-ttu-id="f5668-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5668-123">Requirement</span></span> | <span data-ttu-id="f5668-124">Value</span><span class="sxs-lookup"><span data-stu-id="f5668-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5668-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5668-125">Header</span></span><br/> | <dl> <span data-ttu-id="f5668-126"><dt>WpdMtpExtensions. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5668-126"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5668-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5668-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5668-128">Compatibilidad con extensiones MTP</span><span class="sxs-lookup"><span data-stu-id="f5668-128">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




