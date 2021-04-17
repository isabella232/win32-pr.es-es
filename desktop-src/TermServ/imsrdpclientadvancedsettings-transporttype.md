---
title: Propiedad TransportType de IMsRdpClientAdvancedSettings
description: Especifica el tipo de transporte utilizado por el cliente.
ms.assetid: 752f5fbc-eb5a-48eb-8750-fc25c8a2f024
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad TransportType
- Propiedad TransportType Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad TransportType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.TransportType
- IMsRdpClientAdvancedSettings.get_TransportType
- IMsRdpClientAdvancedSettings.put_TransportType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0664e0c792725dc112baf786d63c5175eb450dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676559"
---
# <a name="imsrdpclientadvancedsettingstransporttype-property"></a><span data-ttu-id="be4d4-106">IMsRdpClientAdvancedSettings:: TransportType (propiedad)</span><span class="sxs-lookup"><span data-stu-id="be4d4-106">IMsRdpClientAdvancedSettings::TransportType property</span></span>

<span data-ttu-id="be4d4-107">Especifica el tipo de transporte utilizado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="be4d4-107">Specifies the transport type used by the client.</span></span> <span data-ttu-id="be4d4-108">El control ActiveX Escritorio remoto no usa esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="be4d4-108">This property is not used by the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="be4d4-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="be4d4-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="be4d4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be4d4-110">Syntax</span></span>


```C++
HRESULT put_TransportType(
  [in]  LONG transportType
);

HRESULT get_TransportType(
  [out] LONG *ptransportType
);
```



## <a name="property-value"></a><span data-ttu-id="be4d4-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="be4d4-111">Property value</span></span>

<span data-ttu-id="be4d4-112">Establece el tipo de transporte.</span><span class="sxs-lookup"><span data-stu-id="be4d4-112">Sets the transport type.</span></span> <span data-ttu-id="be4d4-113">Este método puede realizarse correctamente, pero el control ActiveX de Escritorio remoto nunca usa el valor establecido.</span><span class="sxs-lookup"><span data-stu-id="be4d4-113">This method may succeed, but the value set is never used by the Remote Desktop ActiveX control.</span></span>

## <a name="remarks"></a><span data-ttu-id="be4d4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be4d4-114">Remarks</span></span>

<span data-ttu-id="be4d4-115">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="be4d4-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be4d4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be4d4-116">Requirements</span></span>



| <span data-ttu-id="be4d4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="be4d4-117">Requirement</span></span> | <span data-ttu-id="be4d4-118">Value</span><span class="sxs-lookup"><span data-stu-id="be4d4-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be4d4-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be4d4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="be4d4-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be4d4-120">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="be4d4-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be4d4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="be4d4-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be4d4-122">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="be4d4-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="be4d4-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="be4d4-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be4d4-124"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="be4d4-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="be4d4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be4d4-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be4d4-126"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="be4d4-127">IID</span><span class="sxs-lookup"><span data-stu-id="be4d4-127">IID</span></span><br/>                      | <span data-ttu-id="be4d4-128">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="be4d4-128">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="be4d4-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="be4d4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be4d4-130">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="be4d4-130">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





