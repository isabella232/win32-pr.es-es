---
description: Los dispositivos portátiles de Windows (WPD) admiten las siguientes propiedades de los parámetros de comando.
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: Parámetros de comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Command
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7687488c38f95fd6d7e7b69d64ad6ae32631700d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718877"
---
# <a name="command-parameters"></a><span data-ttu-id="a6fcc-103">Parámetros de comando</span><span class="sxs-lookup"><span data-stu-id="a6fcc-103">Command Parameters</span></span>

<span data-ttu-id="a6fcc-104">Los dispositivos portátiles de Windows (WPD) admiten las siguientes propiedades de los parámetros de comando.</span><span class="sxs-lookup"><span data-stu-id="a6fcc-104">Windows Portable Devices (WPD) supports the following properties of command parameters.</span></span>




| <span data-ttu-id="a6fcc-105">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-105">**Property**</span></span>                                            | <span data-ttu-id="a6fcc-106">**VarType**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-106">**VarType**</span></span>     | <span data-ttu-id="a6fcc-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-107">**Description**</span></span>                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6fcc-108">**\_información de \_ \_ cliente común \_ de la propiedad WPD**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-108">**WPD\_PROPERTY\_COMMON\_CLIENT\_INFORMATION**</span></span>          | <span data-ttu-id="a6fcc-109">**VT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-109">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="a6fcc-110">Interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) que el controlador usa para identificar al cliente.</span><span class="sxs-lookup"><span data-stu-id="a6fcc-110">An [**IPortableDeviceValues**](iportabledevicevalues.md) interface that the driver uses to identify the client.</span></span>                                                             |
| <span data-ttu-id="a6fcc-111">**\_contexto de \_ \_ información de cliente común \_ \_ de la propiedad WPD**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-111">**WPD\_PROPERTY\_COMMON\_CLIENT\_INFORMATION\_CONTEXT**</span></span> | <span data-ttu-id="a6fcc-112">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-112">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="a6fcc-113">Contexto especificado por el controlador que identifica a un cliente para todas las operaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a6fcc-113">A driver-specified context which identifies a client for all subsequent operations.</span></span>                                                                                          |
| <span data-ttu-id="a6fcc-114">**propiedad de la \_ \_ categoría de comandos comunes de propiedades de \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-114">**WPD\_PROPERTY\_COMMON\_COMMAND\_CATEGORY**</span></span>            | <span data-ttu-id="a6fcc-115">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-115">**VT\_CLSID**</span></span>   | <span data-ttu-id="a6fcc-116">Parte del **GUID** del valor de **PROPERTYKEY** del comando.</span><span class="sxs-lookup"><span data-stu-id="a6fcc-116">The **GUID** portion of the **PROPERTYKEY** value of the command.</span></span>                                                                                                            |
| <span data-ttu-id="a6fcc-117">**\_identificador de \_ \_ comando común \_ de la propiedad WPD**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-117">**WPD\_PROPERTY\_COMMON\_COMMAND\_ID**</span></span>                  | <span data-ttu-id="a6fcc-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-118">**VT\_UI4**</span></span>     | <span data-ttu-id="a6fcc-119">La parte del identificador único persistente (PID) del valor de **PROPERTYKEY** del comando.</span><span class="sxs-lookup"><span data-stu-id="a6fcc-119">The Persistent Unique ID (PID) portion of the **PROPERTYKEY** value of the command.</span></span>                                                                                          |
| <span data-ttu-id="a6fcc-120">**\_destino del \_ \_ comando común \_ de la propiedad WPD**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-120">**WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET**</span></span>              | <span data-ttu-id="a6fcc-121">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-121">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="a6fcc-122">Identificador del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="a6fcc-122">The target-object identifier.</span></span>                                                                                                                                                |
| <span data-ttu-id="a6fcc-123">**\_código de \_ \_ error del controlador común \_ \_ de la propiedad WPD**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-123">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>          | <span data-ttu-id="a6fcc-124">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-124">**VT\_UI4**</span></span>     | <span data-ttu-id="a6fcc-125">Código de error específico del controlador devuelto por un controlador de WPD.</span><span class="sxs-lookup"><span data-stu-id="a6fcc-125">A driver-specific error code returned by a WPD driver.</span></span>                                                                                                                       |
| <span data-ttu-id="a6fcc-126">**\_HRESULT de propiedad \_ común \_ de WPD**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-126">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                      | <span data-ttu-id="a6fcc-127">**ERROR de VT \_**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-127">**VT\_ERROR**</span></span>   | <span data-ttu-id="a6fcc-128">Valor **HRESULT** devuelto por un controlador de WPD para una operación determinada.</span><span class="sxs-lookup"><span data-stu-id="a6fcc-128">The **HRESULT** value returned by a WPD driver for a particular operation.</span></span>                                                                                                   |
| <span data-ttu-id="a6fcc-129">**\_ \_ \_ identificadores de objeto \_ comunes de la propiedad WPD**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-129">**WPD\_PROPERTY\_COMMON\_OBJECT\_IDS**</span></span>                  | <span data-ttu-id="a6fcc-130">**VT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-130">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="a6fcc-131">Una interfaz [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de tipo Variant **VT \_ LPWStr** que contiene una lista de identificadores de objeto.</span><span class="sxs-lookup"><span data-stu-id="a6fcc-131">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface of variant type **VT\_LPWSTR** that contains a list of object identifiers.</span></span> |
| <span data-ttu-id="a6fcc-132">**\_ \_ \_ \_ identificadores únicos persistentes \_ comunes de la propiedad WPD**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-132">**WPD\_PROPERTY\_COMMON\_PERSISTENT\_UNIQUE\_IDS**</span></span>      | <span data-ttu-id="a6fcc-133">**VT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-133">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="a6fcc-134">Una interfaz [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de tipo Variant **VT \_ LPWStr** que contiene una lista de PID.</span><span class="sxs-lookup"><span data-stu-id="a6fcc-134">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface of variant type **VT\_LPWSTR** that contains a list of PIDs.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="a6fcc-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6fcc-135">Requirements</span></span>



| <span data-ttu-id="a6fcc-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6fcc-136">Requirement</span></span> | <span data-ttu-id="a6fcc-137">Value</span><span class="sxs-lookup"><span data-stu-id="a6fcc-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6fcc-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6fcc-138">Header</span></span><br/> | <dl> <span data-ttu-id="a6fcc-139"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6fcc-139"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6fcc-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6fcc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6fcc-141">**Propiedades y atributos**</span><span class="sxs-lookup"><span data-stu-id="a6fcc-141">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




