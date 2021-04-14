---
description: Crea un enumerador que se usa para determinar los comandos y eventos que admite un dispositivo de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: 'IWiaItem2:: EnumDeviceCapabilities (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumDeviceCapabilities
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3e771aa636b42d9cd7e4024a1684ebe3edf02eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541982"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a><span data-ttu-id="8abdf-103">IWiaItem2:: EnumDeviceCapabilities (método)</span><span class="sxs-lookup"><span data-stu-id="8abdf-103">IWiaItem2::EnumDeviceCapabilities method</span></span>

<span data-ttu-id="8abdf-104">Crea un enumerador que se usa para determinar los comandos y eventos que admite un dispositivo de adquisición de imágenes de Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="8abdf-104">Creates an enumerator that is used to ascertain the commands and events a Windows Image Acquisition (WIA) 2.0 device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="8abdf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8abdf-105">Syntax</span></span>


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a><span data-ttu-id="8abdf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8abdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8abdf-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8abdf-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8abdf-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="8abdf-108">Type: **LONG**</span></span>

<span data-ttu-id="8abdf-109">Especifica una marca que selecciona el tipo de funcionalidad que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="8abdf-109">Specifies a flag that selects the type of capabilities to enumerate.</span></span> <span data-ttu-id="8abdf-110">Es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8abdf-110">It is one of the following values.</span></span>

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span data-ttu-id="8abdf-111"><span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**\_comandos de dispositivo WIA \_**</span><span class="sxs-lookup"><span data-stu-id="8abdf-111"><span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**WIA\_DEVICE\_COMMANDS**</span></span>


</dt> <dd>

<span data-ttu-id="8abdf-112">Enumerar comandos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8abdf-112">Enumerate device commands.</span></span>

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span data-ttu-id="8abdf-113"><span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**\_eventos de dispositivo WIA \_**</span><span class="sxs-lookup"><span data-stu-id="8abdf-113"><span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**WIA\_DEVICE\_EVENTS**</span></span>


</dt> <dd>

<span data-ttu-id="8abdf-114">Enumerar eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8abdf-114">Enumerate device events.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8abdf-115">*ppIEnumWIA \_ DISP \_* . de desarrollo \[\]</span><span class="sxs-lookup"><span data-stu-id="8abdf-115">*ppIEnumWIA\_DEV\_CAPS* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8abdf-116">Tipo: **[ **IEnumWIA \_ dev \_ caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span><span class="sxs-lookup"><span data-stu-id="8abdf-116">Type: **[**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span></span>

<span data-ttu-id="8abdf-117">Recibe un puntero a la interfaz [**IEnumWIA \_ dev \_ caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) creada por este método.</span><span class="sxs-lookup"><span data-stu-id="8abdf-117">Receives a pointer to the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface created by this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8abdf-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8abdf-118">Return value</span></span>

<span data-ttu-id="8abdf-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8abdf-119">Type: **HRESULT**</span></span>

<span data-ttu-id="8abdf-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8abdf-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8abdf-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8abdf-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8abdf-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8abdf-122">Remarks</span></span>

<span data-ttu-id="8abdf-123">Este método se usa para crear un objeto de enumerador para obtener el conjunto de comandos y eventos que admite un dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="8abdf-123">This method is used to create an enumerator object to obtain the set of commands and events that a WIA 2.0 device supports.</span></span> <span data-ttu-id="8abdf-124">El parámetro *lFlags* se usa para especificar los tipos de funcionalidades de dispositivo que se van a enumerar.</span><span class="sxs-lookup"><span data-stu-id="8abdf-124">The *lFlags* parameter is used to specify which kinds of device capabilities to enumerate.</span></span> <span data-ttu-id="8abdf-125">El método **IWiaItem2:: EnumDeviceCapabilities** almacena la dirección de la interfaz del objeto enumerador en el parámetro *ppIEnumWIA \_ dev \_ caps* .</span><span class="sxs-lookup"><span data-stu-id="8abdf-125">The **IWiaItem2::EnumDeviceCapabilities** method stores the address of the interface of the enumerator object in the *ppIEnumWIA\_DEV\_CAPS* parameter.</span></span>

<span data-ttu-id="8abdf-126">Solo se puede llamar a este método en el elemento raíz de los objetos [**IWiaItem2**](-wia-iwiaitem2.md) de un árbol de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8abdf-126">This method can only be called on the root item of [**IWiaItem2**](-wia-iwiaitem2.md) objects of a device tree.</span></span>

<span data-ttu-id="8abdf-127">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIEnumWIA \_ dev \_ caps* .</span><span class="sxs-lookup"><span data-stu-id="8abdf-127">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnumWIA\_DEV\_CAPS* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8abdf-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8abdf-128">Requirements</span></span>



| <span data-ttu-id="8abdf-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8abdf-129">Requirement</span></span> | <span data-ttu-id="8abdf-130">Value</span><span class="sxs-lookup"><span data-stu-id="8abdf-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8abdf-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8abdf-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8abdf-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8abdf-132">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8abdf-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8abdf-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8abdf-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8abdf-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8abdf-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8abdf-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8abdf-136"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="8abdf-136"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="8abdf-137">IDL</span><span class="sxs-lookup"><span data-stu-id="8abdf-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8abdf-138"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8abdf-138"><dt>Wia.idl</dt></span></span> </dl> |



 

 
