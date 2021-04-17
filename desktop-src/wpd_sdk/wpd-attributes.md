---
description: En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos de parámetro para los métodos y eventos de un servicio de dispositivo.
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: Atributos de parámetro (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Parameter
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 113b2b35a5b6e61cd2cc1d3666d1a13fbade5ec7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718603"
---
# <a name="parameter-attributes"></a><span data-ttu-id="279b4-103">Atributos de parámetro</span><span class="sxs-lookup"><span data-stu-id="279b4-103">Parameter Attributes</span></span>

<span data-ttu-id="279b4-104">En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos de parámetro para los métodos y eventos de un servicio de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="279b4-104">For Windows 7, Windows Portable Devices supports the following parameter attributes for methods and events of a device service.</span></span> <span data-ttu-id="279b4-105">Estos atributos son devueltos por estos métodos:</span><span class="sxs-lookup"><span data-stu-id="279b4-105">These attributes are returned by the these methods:</span></span>

-   [<span data-ttu-id="279b4-106">**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**</span><span class="sxs-lookup"><span data-stu-id="279b4-106">**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [<span data-ttu-id="279b4-107">**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**</span><span class="sxs-lookup"><span data-stu-id="279b4-107">**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| <span data-ttu-id="279b4-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="279b4-108">Attribute</span></span>                                            | <span data-ttu-id="279b4-109">VarType</span><span class="sxs-lookup"><span data-stu-id="279b4-109">VarType</span></span>         | <span data-ttu-id="279b4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="279b4-110">Description</span></span>                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="279b4-111">**\_ \_ valor predeterminado del atributo de parámetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="279b4-111">**WPD\_PARAMETER\_ATTRIBUTE\_DEFAULT\_VALUE**</span></span>        | <span data-ttu-id="279b4-112">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="279b4-112">VT\_*XXXX*</span></span>      | <span data-ttu-id="279b4-113">Valor predeterminado del parámetro.</span><span class="sxs-lookup"><span data-stu-id="279b4-113">The default value of the parameter.</span></span>                                                                                                                                                         |
| <span data-ttu-id="279b4-114">**\_elementos de \_ \_ enumeración de atributo de parámetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="279b4-114">**WPD\_PARAMETER\_ATTRIBUTE\_ENUMERATION\_ELEMENTS**</span></span> | <span data-ttu-id="279b4-115">**VT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="279b4-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="279b4-116">Una interfaz [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contiene los valores de enumeración para el parámetro.</span><span class="sxs-lookup"><span data-stu-id="279b4-116">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface that contains the enumeration values for the parameter.</span></span>                                   |
| <span data-ttu-id="279b4-117">**\_formulario de \_ atributo de parámetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="279b4-117">**WPD\_PARAMETER\_ATTRIBUTE\_FORM**</span></span>                  | <span data-ttu-id="279b4-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="279b4-118">**VT\_UI4**</span></span>     | <span data-ttu-id="279b4-119">Forma de valores de parámetro válidos permitidos.</span><span class="sxs-lookup"><span data-stu-id="279b4-119">The form of valid parameter values allowed.</span></span>                                                                                                                                                 |
| <span data-ttu-id="279b4-120">**\_ \_ tamaño máximo del atributo de parámetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="279b4-120">**WPD\_PARAMETER\_ATTRIBUTE\_MAX\_SIZE**</span></span>             | <span data-ttu-id="279b4-121">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="279b4-121">**VT\_UI8**</span></span>     | <span data-ttu-id="279b4-122">Tamaño máximo del parámetro, en bytes.</span><span class="sxs-lookup"><span data-stu-id="279b4-122">The maximum size of the parameter, in bytes .</span></span>                                                                                                                                               |
| <span data-ttu-id="279b4-123">**\_nombre del \_ atributo del parámetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="279b4-123">**WPD\_PARAMETER\_ATTRIBUTE\_NAME**</span></span>                  | <span data-ttu-id="279b4-124">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="279b4-124">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="279b4-125">Cadena que especifica el nombre descriptivo del script de un parámetro de método o evento.</span><span class="sxs-lookup"><span data-stu-id="279b4-125">A string that specifies the script-friendly name of an event or method parameter.</span></span> <span data-ttu-id="279b4-126">Los caracteres válidos son alfanuméricos a \[ -Za-z0-9 \] y ' \_ '.</span><span class="sxs-lookup"><span data-stu-id="279b4-126">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span>                                                 |
| <span data-ttu-id="279b4-127">**\_orden de \_ atributo del parámetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="279b4-127">**WPD\_PARAMETER\_ATTRIBUTE\_ORDER**</span></span>                 | <span data-ttu-id="279b4-128">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="279b4-128">**VT\_UI4**</span></span>     | <span data-ttu-id="279b4-129">Índice de orden de parámetro basado en cero, de modo que un valor de orden de 0 corresponde al primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="279b4-129">The zero-based parameter-order index, so that an order value of 0 corresponds to the first parameter.</span></span>                                                                                       |
| <span data-ttu-id="279b4-130">**\_ \_ \_ intervalo mínimo de atributo de parámetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="279b4-130">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_MIN**</span></span>            | <span data-ttu-id="279b4-131">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="279b4-131">VT\_*XXXX*</span></span>      | <span data-ttu-id="279b4-132">El valor máximo de un parámetro con el formato del formulario de atributo de parámetro de WPD del formulario \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="279b4-132">The maximum value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                       |
| <span data-ttu-id="279b4-133">**rango de atributo de parámetro de WPD \_ \_ \_ \_ máx.**</span><span class="sxs-lookup"><span data-stu-id="279b4-133">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_MAX**</span></span>            | <span data-ttu-id="279b4-134">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="279b4-134">VT\_*XXXX*</span></span>      | <span data-ttu-id="279b4-135">El valor mínimo para un parámetro con el formato del formulario de atributo de parámetro de WPD del formulario \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="279b4-135">The minimum value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                       |
| <span data-ttu-id="279b4-136">**\_paso de \_ intervalo de atributo de parámetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="279b4-136">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_STEP**</span></span>           | <span data-ttu-id="279b4-137">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="279b4-137">VT\_*XXXX*</span></span>      | <span data-ttu-id="279b4-138">El valor de paso para un parámetro con el formato de tipo de atributo del parámetro WPD del formulario \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="279b4-138">The step value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                          |
| <span data-ttu-id="279b4-139">**\_ \_ expresión regular de atributo de parámetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="279b4-139">**WPD\_PARAMETER\_ATTRIBUTE\_REGULAR\_EXPRESSION**</span></span>   | <span data-ttu-id="279b4-140">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="279b4-140">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="279b4-141">Una expresión regular que especifica valores aceptables para los parámetros de la \_ forma \_ expresión regular del formulario de atributo de parámetro WPD \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="279b4-141">A regular expression that specifies acceptable values for parameters of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION.</span></span>                                                      |
| <span data-ttu-id="279b4-142">**\_tipo de \_ uso de atributo de parámetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="279b4-142">**WPD\_PARAMETER\_ATTRIBUTE\_USAGE\_TYPE**</span></span>           | <span data-ttu-id="279b4-143">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="279b4-143">**VT\_UI4**</span></span>     | <span data-ttu-id="279b4-144">Un entero que especifica el uso de un parámetro de método, por ejemplo, in/out. Los valores válidos son del tipo de enumeración de [**tipos de uso de parámetros de WPD \_ \_ \_**](wpd-parameter-usage-types.md) .</span><span class="sxs-lookup"><span data-stu-id="279b4-144">An integer that specifies the usage of a method parameter, for example, in/out. Valid values are of the [**WPD\_PARAMETER\_USAGE\_TYPES**](wpd-parameter-usage-types.md) enumeration type.</span></span> |
| <span data-ttu-id="279b4-145">**atributo de parámetro de WPD \_ \_ \_ VARTYPE**</span><span class="sxs-lookup"><span data-stu-id="279b4-145">**WPD\_PARAMETER\_ATTRIBUTE\_VARTYPE**</span></span>               | <span data-ttu-id="279b4-146">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="279b4-146">**VT\_UI4**</span></span>     | <span data-ttu-id="279b4-147">Parámetro VarType.</span><span class="sxs-lookup"><span data-stu-id="279b4-147">The parameter VarType.</span></span>                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="279b4-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="279b4-148">Requirements</span></span>



| <span data-ttu-id="279b4-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="279b4-149">Requirement</span></span> | <span data-ttu-id="279b4-150">Value</span><span class="sxs-lookup"><span data-stu-id="279b4-150">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="279b4-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="279b4-151">Header</span></span><br/> | <dl> <span data-ttu-id="279b4-152"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="279b4-152"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="279b4-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="279b4-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="279b4-154">**Propiedades y atributos**</span><span class="sxs-lookup"><span data-stu-id="279b4-154">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




