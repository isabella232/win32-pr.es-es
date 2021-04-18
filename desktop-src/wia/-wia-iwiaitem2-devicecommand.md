---
description: Emite un comando para un dispositivo de hardware de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: IWiaItem2::D método eviceCommand (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceCommand
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2961a3c0e0d1b75a487b9bf112e76bee8c937a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715195"
---
# <a name="iwiaitem2devicecommand-method"></a><span data-ttu-id="45b0b-103">IWiaItem2::D método eviceCommand</span><span class="sxs-lookup"><span data-stu-id="45b0b-103">IWiaItem2::DeviceCommand method</span></span>

<span data-ttu-id="45b0b-104">Emite un comando para un dispositivo de hardware de adquisición de imágenes de Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="45b0b-104">Issues a command to a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b0b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45b0b-105">Syntax</span></span>


```C++
HRESULT DeviceCommand(
  [in]            LONG      lFlags,
  [in]      const GUID      *pCmdGUID,
  [in, out]       IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="45b0b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45b0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45b0b-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45b0b-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45b0b-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="45b0b-108">Type: **LONG**</span></span>

<span data-ttu-id="45b0b-109">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="45b0b-109">Currently unused.</span></span> <span data-ttu-id="45b0b-110">Debe establecerse como cero.</span><span class="sxs-lookup"><span data-stu-id="45b0b-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="45b0b-111">*pCmdGUID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45b0b-111">*pCmdGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45b0b-112">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="45b0b-112">Type: \**const GUID\** _</span></span>

<span data-ttu-id="45b0b-113">Especifica el comando que se va a enviar al dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="45b0b-113">Specifies the command to send to the WIA 2.0 device.</span></span> <span data-ttu-id="45b0b-114">Consulte [_ *comandos* \* de dispositivo WIA](-wia-wia-device-commands.md).</span><span class="sxs-lookup"><span data-stu-id="45b0b-114">See [_ *WIA Device Commands*\*](-wia-wia-device-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="45b0b-115">*ppIWiaItem2* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="45b0b-115">*ppIWiaItem2* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="45b0b-116">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="45b0b-116">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="45b0b-117">Recibe la dirección de un puntero al elemento [**IWiaItem2**](-wia-iwiaitem2.md) creado por el comando, si existe.</span><span class="sxs-lookup"><span data-stu-id="45b0b-117">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) item created by the command, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45b0b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45b0b-118">Return value</span></span>

<span data-ttu-id="45b0b-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="45b0b-119">Type: **HRESULT**</span></span>

<span data-ttu-id="45b0b-120">Además de los códigos de error COM estándar, el método puede devolver el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="45b0b-120">In addition to the standard COM error codes, the method may return the following value.</span></span>



| <span data-ttu-id="45b0b-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="45b0b-121">Return code</span></span>                                                                                       | <span data-ttu-id="45b0b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="45b0b-122">Description</span></span>                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="45b0b-123"><dt>**E \_ CMDNOTSUPPORTED**</dt></span><span class="sxs-lookup"><span data-stu-id="45b0b-123"><dt>**E\_CMDNOTSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="45b0b-124">El comando no está implementado para la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) en la que se llama al método.</span><span class="sxs-lookup"><span data-stu-id="45b0b-124">The command is not implemented for the [**IWiaItem2**](-wia-iwiaitem2.md) interface on which the method is called.</span></span> <span data-ttu-id="45b0b-125">El valor numérico de este error aún no se ha definido.</span><span class="sxs-lookup"><span data-stu-id="45b0b-125">The numeric value for this error is not yet defined.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="45b0b-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45b0b-126">Remarks</span></span>

<span data-ttu-id="45b0b-127">El comportamiento de este método es diferente en función de la categoría del nodo en el que se llama al método.</span><span class="sxs-lookup"><span data-stu-id="45b0b-127">The behavior of this method is different depending on the category of the node on which the method is called.</span></span>

<span data-ttu-id="45b0b-128">Cuando la aplicación envía el comando [**WIA \_ cmd \_ Take \_ Picture**](-wia-wia-device-commands.md) al dispositivo mediante el método **IWiaItem2::D evicecommand** , el sistema en tiempo de ejecución de WIA 2,0 crea un objeto [**IWiaItem2**](-wia-iwiaitem2.md) para representar la imagen.</span><span class="sxs-lookup"><span data-stu-id="45b0b-128">When the application sends the [**WIA\_CMD\_TAKE\_PICTURE**](-wia-wia-device-commands.md) command to the device using the **IWiaItem2::DeviceCommand** method, the WIA 2.0 run-time system creates an [**IWiaItem2**](-wia-iwiaitem2.md) object to represent the image.</span></span> <span data-ttu-id="45b0b-129">El método **IWiaItem2::D evicecommand** almacena la dirección de la interfaz en el parámetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="45b0b-129">The **IWiaItem2::DeviceCommand** method stores the address of the interface in the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="45b0b-130">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="45b0b-130">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="45b0b-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45b0b-131">Requirements</span></span>



| <span data-ttu-id="45b0b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="45b0b-132">Requirement</span></span> | <span data-ttu-id="45b0b-133">Value</span><span class="sxs-lookup"><span data-stu-id="45b0b-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="45b0b-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45b0b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="45b0b-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="45b0b-135">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="45b0b-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45b0b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="45b0b-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="45b0b-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="45b0b-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45b0b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="45b0b-139"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="45b0b-139"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="45b0b-140">IDL</span><span class="sxs-lookup"><span data-stu-id="45b0b-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="45b0b-141"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="45b0b-141"><dt>Wia.idl</dt></span></span> </dl> |



 

 
