---
description: Notifica a una aplicación que se ha completado una solicitud de conexión o desconexión programada previamente al dispositivo MTP/Bluetooth.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: 'Método IConnectionRequestCallback:: alcomplete (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback.OnComplete
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 922169b7e17335c47425665bb9a9e54891e68723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911141"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a><span data-ttu-id="44ea9-103">IConnectionRequestCallback:: alcomplete (método)</span><span class="sxs-lookup"><span data-stu-id="44ea9-103">IConnectionRequestCallback::OnComplete method</span></span>

<span data-ttu-id="44ea9-104">El método **alcomplete** notifica a una aplicación que se ha completado una solicitud de conexión o desconexión programada previamente al dispositivo MTP/Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="44ea9-104">The **OnComplete** method notifies an application that a previously scheduled Connect or Disconnect request to the MTP/Bluetooth device has completed</span></span>

## <a name="syntax"></a><span data-ttu-id="44ea9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44ea9-105">Syntax</span></span>


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a><span data-ttu-id="44ea9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44ea9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44ea9-107">*hrStatus* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="44ea9-107">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44ea9-108">El estado de la solicitud para conectar o desconectar un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="44ea9-108">The status of the request to connect or disconnect a given device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44ea9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44ea9-109">Return value</span></span>

<span data-ttu-id="44ea9-110">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="44ea9-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="44ea9-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="44ea9-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="44ea9-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="44ea9-112">Return code</span></span>                                                                          | <span data-ttu-id="44ea9-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="44ea9-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="44ea9-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="44ea9-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="44ea9-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="44ea9-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="44ea9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44ea9-116">Remarks</span></span>

<span data-ttu-id="44ea9-117">Una aplicación implementa la interfaz [**IConnectionRequestCallback**](iconnectionrequestcallback.md) para recibir notificaciones sobre las solicitudes completadas y cancelar las solicitudes pendientes.</span><span class="sxs-lookup"><span data-stu-id="44ea9-117">An application implements the [**IConnectionRequestCallback**](iconnectionrequestcallback.md) interface to receive notifications about completed requests and to cancel pending requests.</span></span>

<span data-ttu-id="44ea9-118">Dispositivos portátiles de Windows (WPD) llama a este método para notificar a una aplicación que se ha completado una solicitud programada previamente.</span><span class="sxs-lookup"><span data-stu-id="44ea9-118">Windows Portable Devices (WPD) calls this method to notify an application that a previously scheduled request has completed.</span></span> <span data-ttu-id="44ea9-119">La devolución de llamada proporcionada por la aplicación puede realizar un seguimiento de cada solicitud y cancelarla.</span><span class="sxs-lookup"><span data-stu-id="44ea9-119">Each request can be tracked and canceled by its application-supplied callback.</span></span> <span data-ttu-id="44ea9-120">Por lo tanto, si la aplicación necesita enviar varias solicitudes al mismo tiempo mediante el mismo objeto [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , se debe pasar a cada solicitud un objeto [**IConnectionRequestCallback**](iconnectionrequestcallback.md) único como parámetro de entrada a los métodos [**IPortableDeviceConnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) y [**IPortableDeviceConnector::D Ulta**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="44ea9-120">Therefore, if the application needs to send multiple requests at the same time using the same [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) object, each request should be passed a unique [**IConnectionRequestCallback**](iconnectionrequestcallback.md) object as the input parameter to the [**IPortableDeviceConnector::Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) and [**IPortableDeviceConnector::Disconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="44ea9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44ea9-121">Requirements</span></span>



| <span data-ttu-id="44ea9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="44ea9-122">Requirement</span></span> | <span data-ttu-id="44ea9-123">Value</span><span class="sxs-lookup"><span data-stu-id="44ea9-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44ea9-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44ea9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="44ea9-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="44ea9-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="44ea9-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44ea9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="44ea9-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="44ea9-127">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="44ea9-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44ea9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="44ea9-129"><dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="44ea9-129"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="44ea9-130">IDL</span><span class="sxs-lookup"><span data-stu-id="44ea9-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="44ea9-131"><dt>Portabledeviceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="44ea9-131"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="44ea9-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44ea9-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="44ea9-133"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44ea9-133"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="44ea9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="44ea9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44ea9-135">**IConnectionRequestCallback**</span><span class="sxs-lookup"><span data-stu-id="44ea9-135">**IConnectionRequestCallback**</span></span>](iconnectionrequestcallback.md)
</dt> </dl>

 

 




