---
description: Una aplicación llama al método SetExternalT120Address para configurar una dirección T. 120 externa para el intercambio de datos.
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: 'IH323LineEx:: SetExternalT120Address (método) (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09756aaf77ba36497b3059f7e93829d7d6a57b42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690168"
---
# <a name="ih323lineexsetexternalt120address-method"></a><span data-ttu-id="4b1c5-103">IH323LineEx:: SetExternalT120Address (método)</span><span class="sxs-lookup"><span data-stu-id="4b1c5-103">IH323LineEx::SetExternalT120Address method</span></span>

<span data-ttu-id="4b1c5-104">\[**SetExternalT120Address** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4b1c5-104">\[**SetExternalT120Address** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4b1c5-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="4b1c5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4b1c5-106">Una aplicación llama al método **SetExternalT120Address** para configurar una dirección T. 120 externa para el intercambio de datos.</span><span class="sxs-lookup"><span data-stu-id="4b1c5-106">The **SetExternalT120Address** method is called by an application to configure an external T.120 address for data exchange.</span></span> <span data-ttu-id="4b1c5-107">La capacidad t. 120 se anunciará durante la negociación H. 245 y la dirección se usará en la confirmación de canal de lógica abierta para que el otro punto de conexión pueda configurar las sesiones de T. 120 con el servicio escuchando en esa dirección.</span><span class="sxs-lookup"><span data-stu-id="4b1c5-107">T.120 capability will be advertised during the H.245 negotiation, and the address will be used in the open logic channel acknowledgement so that the other endpoint can set up T.120 sessions with the service listening on that address.</span></span> <span data-ttu-id="4b1c5-108">Si no se llama a esta función, el proveedor de servicios H. 323 no anunciará la capacidad T. 120.</span><span class="sxs-lookup"><span data-stu-id="4b1c5-108">If this function is not called, the H.323 service provider will not advertise T.120 capability.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b1c5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b1c5-109">Syntax</span></span>


```C++
HRESULT SetExternalT120Address(
  [in] BOOL  fEnable,
  [in] DWORD dwIP,
  [in] WORD  wPort
);
```



## <a name="parameters"></a><span data-ttu-id="4b1c5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b1c5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b1c5-111">*fEnable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b1c5-111">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b1c5-112">**True** para habilitar la capacidad T. 120; **False** para deshabilitar la capacidad T. 120.</span><span class="sxs-lookup"><span data-stu-id="4b1c5-112">**TRUE** to enable T.120 capability; **FALSE** to disable T.120 capability.</span></span>

</dd> <dt>

<span data-ttu-id="4b1c5-113">*dwIP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b1c5-113">*dwIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b1c5-114">**DWORD** que contiene la dirección IP en el orden de bytes de host del servicio T. 120 externo.</span><span class="sxs-lookup"><span data-stu-id="4b1c5-114">**DWORD** containing the IP address in host byte order of the external T.120 service.</span></span>

</dd> <dt>

<span data-ttu-id="4b1c5-115">*wPort* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b1c5-115">*wPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b1c5-116">**Palabra** que contiene el puerto del servicio T. 120 externo.</span><span class="sxs-lookup"><span data-stu-id="4b1c5-116">**WORD** containing the port of the external T.120 service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b1c5-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b1c5-117">Return value</span></span>

<span data-ttu-id="4b1c5-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="4b1c5-118">This method can return one of these values.</span></span>



| <span data-ttu-id="4b1c5-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4b1c5-119">Return code</span></span>                                                                          | <span data-ttu-id="4b1c5-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b1c5-120">Description</span></span>                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="4b1c5-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4b1c5-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4b1c5-122">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="4b1c5-122">Method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4b1c5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b1c5-123">Requirements</span></span>



| <span data-ttu-id="4b1c5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b1c5-124">Requirement</span></span> | <span data-ttu-id="4b1c5-125">Value</span><span class="sxs-lookup"><span data-stu-id="4b1c5-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b1c5-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="4b1c5-126">TAPI version</span></span><br/> | <span data-ttu-id="4b1c5-127">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="4b1c5-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4b1c5-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b1c5-128">Header</span></span><br/>       | <dl> <span data-ttu-id="4b1c5-129"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b1c5-129"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="4b1c5-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b1c5-130">Library</span></span><br/>      | <dl> <span data-ttu-id="4b1c5-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b1c5-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4b1c5-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4b1c5-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="4b1c5-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b1c5-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




