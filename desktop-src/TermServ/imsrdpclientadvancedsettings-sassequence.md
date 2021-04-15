---
title: Propiedad SasSequence de IMsRdpClientAdvancedSettings
description: Especifica la secuencia de acceso seguro (SAS) que el cliente usará para tener acceso a la pantalla de inicio de sesión en el servidor.
ms.assetid: ec1dc7b1-2bf1-447b-a768-08f28982a995
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad SasSequence
- Propiedad SasSequence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad SasSequence
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SasSequence
- IMsRdpClientAdvancedSettings.get_SasSequence
- IMsRdpClientAdvancedSettings.put_SasSequence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf38a4e1f048e67613b92b3629aa96cca281b1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489125"
---
# <a name="imsrdpclientadvancedsettingssassequence-property"></a><span data-ttu-id="088e4-106">IMsRdpClientAdvancedSettings:: SasSequence (propiedad)</span><span class="sxs-lookup"><span data-stu-id="088e4-106">IMsRdpClientAdvancedSettings::SasSequence property</span></span>

<span data-ttu-id="088e4-107">Especifica la secuencia de acceso seguro (SAS) que el cliente usará para tener acceso a la pantalla de inicio de sesión en el servidor.</span><span class="sxs-lookup"><span data-stu-id="088e4-107">Specifies the secure access sequence (SAS) the client will use to access the login screen on the server.</span></span>

<span data-ttu-id="088e4-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="088e4-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="088e4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="088e4-109">Syntax</span></span>


```C++
HRESULT put_SasSequence(
  [in]  LONG sasSequence
);

HRESULT get_SasSequence(
  [out] LONG *psasSequence
);
```



## <a name="property-value"></a><span data-ttu-id="088e4-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="088e4-110">Property value</span></span>

<span data-ttu-id="088e4-111">Un valor **Long** que contiene el indicador SAS.</span><span class="sxs-lookup"><span data-stu-id="088e4-111">A **LONG** value that contains the SAS indicator.</span></span> <span data-ttu-id="088e4-112">El único valor admitido es 0xaa03, que indica la secuencia CTRL + ALT + SUPR estándar.</span><span class="sxs-lookup"><span data-stu-id="088e4-112">The only supported value is 0xaa03, which indicates the standard CTRL+ALT+DELETE sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="088e4-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="088e4-113">Remarks</span></span>

<span data-ttu-id="088e4-114">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="088e4-114">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="088e4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="088e4-115">Requirements</span></span>



| <span data-ttu-id="088e4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="088e4-116">Requirement</span></span> | <span data-ttu-id="088e4-117">Value</span><span class="sxs-lookup"><span data-stu-id="088e4-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="088e4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="088e4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="088e4-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="088e4-119">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="088e4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="088e4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="088e4-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="088e4-121">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="088e4-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="088e4-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="088e4-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="088e4-123"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="088e4-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="088e4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="088e4-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="088e4-125"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="088e4-126">IID</span><span class="sxs-lookup"><span data-stu-id="088e4-126">IID</span></span><br/>                      | <span data-ttu-id="088e4-127">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="088e4-127">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="088e4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="088e4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="088e4-129">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="088e4-129">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





