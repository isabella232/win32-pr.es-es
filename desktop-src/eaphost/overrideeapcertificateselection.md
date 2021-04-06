---
title: OverrideEAPCertificateSelection
description: La clave del registro OverrideEAPCertificateSelection determina si el cliente invalidará el comportamiento de la selección de certificados de tarjeta inteligente predeterminada y proporcionará al usuario más certificados entre los que elegir.
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d958eeeffba96e7a060ee4dd3edaf8a9935a15d1
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "103904328"
---
# <a name="overrideeapcertificateselection"></a><span data-ttu-id="57523-103">OverrideEAPCertificateSelection</span><span class="sxs-lookup"><span data-stu-id="57523-103">OverrideEAPCertificateSelection</span></span>

<span data-ttu-id="57523-104">La clave del registro OverrideEAPCertificateSelection determina si el cliente invalidará el comportamiento de la selección de certificados de tarjeta inteligente predeterminada y proporcionará al usuario más certificados entre los que elegir.</span><span class="sxs-lookup"><span data-stu-id="57523-104">The OverrideEAPCertificateSelection registry key determines whether the client will override the default smart card certificate selection behavior and provide the user with more certificates to choose from.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="57523-105">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="57523-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a><span data-ttu-id="57523-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57523-106">Remarks</span></span>

<span data-ttu-id="57523-107">Se trata de un valor **\_ binario de registro** .</span><span class="sxs-lookup"><span data-stu-id="57523-107">This is a **REG\_BINARY** value.</span></span>



| <span data-ttu-id="57523-108">Value</span><span class="sxs-lookup"><span data-stu-id="57523-108">Value</span></span> | <span data-ttu-id="57523-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="57523-109">Description</span></span>                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57523-110">0x000</span><span class="sxs-lookup"><span data-stu-id="57523-110">0x000</span></span> | <span data-ttu-id="57523-111">No invalide el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="57523-111">Do not override the default behavior.</span></span>                                                                                                                                                                |
| <span data-ttu-id="57523-112">0x001</span><span class="sxs-lookup"><span data-stu-id="57523-112">0x001</span></span> | <span data-ttu-id="57523-113">Elija el último certificado adjunto de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="57523-113">Choose the last attached certificate from the smart card.</span></span>                                                                                                                                            |
| <span data-ttu-id="57523-114">0x010</span><span class="sxs-lookup"><span data-stu-id="57523-114">0x010</span></span> | <span data-ttu-id="57523-115">Muestra todos los certificados en la interfaz de usuario de selección de certificados de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="57523-115">Shows all certificates in the certificate selection UI from the smart card.</span></span>                                                                                                                          |
| <span data-ttu-id="57523-116">0x100</span><span class="sxs-lookup"><span data-stu-id="57523-116">0x100</span></span> | <span data-ttu-id="57523-117">Muestra todos los certificados en la interfaz de usuario de selección de certificados del registro.</span><span class="sxs-lookup"><span data-stu-id="57523-117">Shows all certificates in the certificate selection UI from the registry.</span></span>                                                                                                                            |
| <span data-ttu-id="57523-118">0x101</span><span class="sxs-lookup"><span data-stu-id="57523-118">0x101</span></span> | <span data-ttu-id="57523-119">Muestra todos los certificados de la interfaz de usuario de selección de certificados del registro y el último certificado adjunto de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="57523-119">Shows all certificates in the certificate selection UI from the registry and the last attached certificate from the smart card.</span></span> <span data-ttu-id="57523-120">Muestra el último certificado adjunto de la tarjeta inteligente como seleccionado.</span><span class="sxs-lookup"><span data-stu-id="57523-120">Shows the last attached certificate from the smart card as selected.</span></span> |
| <span data-ttu-id="57523-121">0x110</span><span class="sxs-lookup"><span data-stu-id="57523-121">0x110</span></span> | <span data-ttu-id="57523-122">Muestra todos los certificados en la interfaz de usuario de selección de certificados del registro y la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="57523-122">Shows all certificates in the certificate selection UI from the registry and the smart card.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="57523-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57523-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57523-124">Configuración del registro de EAPHost</span><span class="sxs-lookup"><span data-stu-id="57523-124">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




