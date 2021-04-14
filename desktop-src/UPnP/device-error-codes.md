---
title: Códigos de error de dispositivo
description: Los métodos InvokeAction y QueryStateVariable devuelven valores HRESULT que podrían indicar un error de dispositivo (es decir, un error que se recibe de un dispositivo certificado con UPnP).
ms.assetid: 4b18a5d4-f6e8-4670-93dd-ecd012940000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcd92d79897318ae6e45fac918dce6af2fe647b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104488434"
---
# <a name="device-error-codes"></a><span data-ttu-id="48316-103">Códigos de error de dispositivo</span><span class="sxs-lookup"><span data-stu-id="48316-103">Device Error Codes</span></span>

<span data-ttu-id="48316-104">Los métodos [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) y [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) devuelven valores **HRESULT** que podrían indicar un error de dispositivo (es decir, un error que se recibe de un dispositivo certificado con UPnP).</span><span class="sxs-lookup"><span data-stu-id="48316-104">The [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) and [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) methods return **HRESULT** values that might indicate a device error (that is, an error that is received from a UPnP-certified device).</span></span> <span data-ttu-id="48316-105">Si se recibe un error de un dispositivo, el método ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) o [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) devuelve un valor **HRESULT** que se basa en el código de error del dispositivo, tal como se explica en este tema.</span><span class="sxs-lookup"><span data-stu-id="48316-105">If an error is received from a device, the method ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) or [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) returns an **HRESULT** value that is based on the device error code, as explained in this topic.</span></span> <span data-ttu-id="48316-106">Dado que se aplica una conversión al código de error del dispositivo para generar un valor **HRESULT** , no se puede leer el código de error del dispositivo directamente desde el valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="48316-106">Because a conversion is applied to the device error code to produce an **HRESULT** value, you cannot read the device error code directly from the **HRESULT** value.</span></span>

## <a name="conversion-of-a-device-error-code-to-an-hresult"></a><span data-ttu-id="48316-107">Conversión de un código de error de dispositivo a un valor HRESULT</span><span class="sxs-lookup"><span data-stu-id="48316-107">Conversion of a Device Error Code to an HRESULT</span></span>

<span data-ttu-id="48316-108">Hay códigos de error de dispositivo estándar y no estándar.</span><span class="sxs-lookup"><span data-stu-id="48316-108">There are both standard and non-standard device error codes.</span></span> <span data-ttu-id="48316-109">Los códigos estándar tienen el mismo significado en todos los dispositivos certificados para UPnP y tienen valores inferiores a 600.</span><span class="sxs-lookup"><span data-stu-id="48316-109">The standard codes have the same meaning across all UPnP-certified devices and have values that are less than 600.</span></span> <span data-ttu-id="48316-110">Los códigos no estándar son específicos del proveedor y tienen valores comprendidos entre 600 y 899.</span><span class="sxs-lookup"><span data-stu-id="48316-110">The non-standard codes are vendor-specific and have values ranging from 600 through 899.</span></span>

<span data-ttu-id="48316-111">Tanto si el código de error del dispositivo es estándar como si no, determina cómo se genera el valor **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="48316-111">Whether or not the device error code is standard determines how the **HRESULT** value is generated:</span></span>

-   <span data-ttu-id="48316-112">Un código de error de dispositivo estándar se asigna a un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="48316-112">A standard device error code is mapped to an **HRESULT** value.</span></span>

<!-- -->

-   <span data-ttu-id="48316-113">Un código de error de dispositivo no estándar se incrusta en el valor **HRESULT** aplicando una fórmula.</span><span class="sxs-lookup"><span data-stu-id="48316-113">A non-standard device error code is embedded in the **HRESULT** value by applying a formula.</span></span>

<span data-ttu-id="48316-114">Ambos procedimientos se pueden invertir para determinar el código de error de dispositivo a partir de un valor **HRESULT** determinado.</span><span class="sxs-lookup"><span data-stu-id="48316-114">Both of these procedures can be reversed to determine the device error code from a particular **HRESULT** value.</span></span>

## <a name="deriving-a-device-error-code-from-an-hresult-value"></a><span data-ttu-id="48316-115">Derivar un código de error de dispositivo de un valor HRESULT</span><span class="sxs-lookup"><span data-stu-id="48316-115">Deriving a Device Error Code from an HRESULT Value</span></span>

<span data-ttu-id="48316-116">Si el valor **HRESULT** es mayor o igual que la **\_ \_ \_ \_ base específica de la acción de UPnP e** (0x80040300) y es menor o igual que el **\_ \_ \_ \_ número máximo específico de acciones de UPnP e** (0x8004042B), el código de error del dispositivo no es estándar. Use la fórmula de la sección siguiente para determinar el código de error.</span><span class="sxs-lookup"><span data-stu-id="48316-116">If the **HRESULT** value is greater than or equal to **UPNP\_E\_ACTION\_SPECIFIC\_BASE** (0x80040300) and less than or equal to **UPNP\_E\_ACTION\_SPECIFIC\_MAX** (0x8004042B), the device error code is nonstandard — use the formula in the following section to determine the error code.</span></span> <span data-ttu-id="48316-117">De lo contrario, el código de error del dispositivo es estándar. Use la tabla de la sección asignación de códigos de error de dispositivo estándar, que proporciona la asignación del valor **HRESULT** al código de error del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48316-117">Otherwise, the device error code is standard — use the table in the Mapping for Standard Device Error Codes section, which provides the mapping from the **HRESULT** value to the device error code.</span></span>

<span data-ttu-id="48316-118">Para obtener una descripción de texto del error después de una llamada a [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), establezca el parámetro *pvarRetVal* en una matriz vacía.</span><span class="sxs-lookup"><span data-stu-id="48316-118">For a text description of the error after a call to [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), set the *pvarRetVal* parameter to an empty array.</span></span> <span data-ttu-id="48316-119">En el momento de la devolución, este parámetro contendrá una descripción de texto del error, si se produjo alguno.</span><span class="sxs-lookup"><span data-stu-id="48316-119">Upon return, this parameter will contain a text description of the error, if any occurred.</span></span>

### <a name="formula-for-nonstandard-device-error-codes"></a><span data-ttu-id="48316-120">Fórmula para códigos de error de dispositivo no estándar</span><span class="sxs-lookup"><span data-stu-id="48316-120">Formula for Nonstandard Device Error Codes</span></span>

<span data-ttu-id="48316-121">Use la siguiente fórmula si **la \_ \_ \_ \_ base específica de la acción UPnP e** no es el **valor** **\_ \_ \_ \_ máximo específico de la acción de UPnP e**.</span><span class="sxs-lookup"><span data-stu-id="48316-121">Use the following formula if **UPNP\_E\_ACTION\_SPECIFIC\_BASE** ≤ **HRESULT** ≤**UPNP\_E\_ACTION\_SPECIFIC\_MAX**.</span></span>

<span data-ttu-id="48316-122">Código de error de dispositivo **= (**  -  **\_ \_ \_ \_ base específica de la acción de UPnP E** **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48316-122">Device Error Code = (**HRESULT** - **UPNP\_E\_ACTION\_SPECIFIC\_BASE**) + **FAULT\_ACTION\_SPECIFIC\_BASE**</span></span>

<span data-ttu-id="48316-123">Sustituir los valores numéricos reales, la ecuación es: código de error de dispositivo = (**HRESULT** -0x80040300) + 0x0258</span><span class="sxs-lookup"><span data-stu-id="48316-123">Substituting the actual numeric values, the equation is: Device Error Code = (**HRESULT** - 0x80040300) + 0x0258</span></span>

### <a name="mapping-for-standard-device-error-codes"></a><span data-ttu-id="48316-124">Asignación de códigos de error de dispositivo estándar</span><span class="sxs-lookup"><span data-stu-id="48316-124">Mapping for Standard Device Error Codes</span></span>

<span data-ttu-id="48316-125">Use la siguiente **asignación si la**  <  **\_ \_ \_ \_ base específica de la acción de UPnP E** de la acción.</span><span class="sxs-lookup"><span data-stu-id="48316-125">Use the following mapping if **HRESULT** < **UPNP\_E\_ACTION\_SPECIFIC\_BASE**.</span></span>



| <span data-ttu-id="48316-126">Valor HRESULT</span><span class="sxs-lookup"><span data-stu-id="48316-126">HRESULT value</span></span>                    | <span data-ttu-id="48316-127">Código de error de dispositivo</span><span class="sxs-lookup"><span data-stu-id="48316-127">Device Error Code</span></span>                | <span data-ttu-id="48316-128">Valor real</span><span class="sxs-lookup"><span data-stu-id="48316-128">Actual value</span></span> |
|----------------------------------|----------------------------------|--------------|
| <span data-ttu-id="48316-129">\_ \_ acción no válida de UPnP E \_</span><span class="sxs-lookup"><span data-stu-id="48316-129">UPNP\_E\_INVALID\_ACTION</span></span>         | <span data-ttu-id="48316-130">\_acción no válida de error \_</span><span class="sxs-lookup"><span data-stu-id="48316-130">FAULT\_INVALID\_ACTION</span></span>           | <span data-ttu-id="48316-131">401</span><span class="sxs-lookup"><span data-stu-id="48316-131">401</span></span>          |
| <span data-ttu-id="48316-132">\_ \_ argumentos no válidos de UPnP E \_</span><span class="sxs-lookup"><span data-stu-id="48316-132">UPNP\_E\_INVALID\_ARGUMENTS</span></span>      | <span data-ttu-id="48316-133">argumento de error \_ no válido \_</span><span class="sxs-lookup"><span data-stu-id="48316-133">FAULT\_INVALID\_ARG</span></span>              | <span data-ttu-id="48316-134">402</span><span class="sxs-lookup"><span data-stu-id="48316-134">402</span></span>          |
| <span data-ttu-id="48316-135">UPNP \_ E \_ no \_ \_ sincronizados</span><span class="sxs-lookup"><span data-stu-id="48316-135">UPNP\_E\_OUT\_OF\_SYNC</span></span>           | <span data-ttu-id="48316-136">ERROR \_ de \_ número de secuencia no válido \_</span><span class="sxs-lookup"><span data-stu-id="48316-136">FAULT\_INVALID\_SEQUENCE\_NUMBER</span></span> | <span data-ttu-id="48316-137">403</span><span class="sxs-lookup"><span data-stu-id="48316-137">403</span></span>          |
| <span data-ttu-id="48316-138">\_ \_ variable no válida de UPnP E \_</span><span class="sxs-lookup"><span data-stu-id="48316-138">UPNP\_E\_INVALID\_VARIABLE</span></span>       | <span data-ttu-id="48316-139">ERROR \_ de \_ variable no válida</span><span class="sxs-lookup"><span data-stu-id="48316-139">FAULT\_INVALID\_VARIABLE</span></span>         | <span data-ttu-id="48316-140">404</span><span class="sxs-lookup"><span data-stu-id="48316-140">404</span></span>          |
| <span data-ttu-id="48316-141">\_error de \_ solicitud de acción \_ \_ de UPnP E</span><span class="sxs-lookup"><span data-stu-id="48316-141">UPNP\_E\_ACTION\_REQUEST\_FAILED</span></span> | <span data-ttu-id="48316-142">\_ \_ error interno del dispositivo de error \_</span><span class="sxs-lookup"><span data-stu-id="48316-142">FAULT\_DEVICE\_INTERNAL\_ERROR</span></span>   | <span data-ttu-id="48316-143">501</span><span class="sxs-lookup"><span data-stu-id="48316-143">501</span></span>          |



 

## <a name="more-information"></a><span data-ttu-id="48316-144">Más información</span><span class="sxs-lookup"><span data-stu-id="48316-144">More Information</span></span>

<span data-ttu-id="48316-145">Los códigos de error de dispositivo se especifican en la [versión 1,0 de la arquitectura del dispositivo UPnP](https://openconnectivity.org/resources/documents.asp).</span><span class="sxs-lookup"><span data-stu-id="48316-145">Device error codes are specified in [UPnP Device Architecture version 1.0](https://openconnectivity.org/resources/documents.asp).</span></span> <span data-ttu-id="48316-146">Las constantes mencionadas en este tema se definen en los archivos UPnP. h y UPnP. idl.</span><span class="sxs-lookup"><span data-stu-id="48316-146">The constants mentioned in this topic are defined in the files Upnp.h and Upnp.idl.</span></span>

 

 




