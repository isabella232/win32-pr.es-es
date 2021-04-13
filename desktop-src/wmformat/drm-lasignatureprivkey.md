---
title: DRM_LASignaturePrivKey
description: La \_ propiedad LASignaturePrivKey de DRM contiene la clave privada que se usa para cifrar el encabezado DRM.
ms.assetid: b7083237-da11-4f31-a143-c0278a54b5a6
keywords:
- DRM_LASignaturePrivKey formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_LASignaturePrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdb22f3abc57fc2331ff87bd05bc05d580d607c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420309"
---
# <a name="drm_lasignatureprivkey"></a><span data-ttu-id="9904c-104">\_LASIGNATUREPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="9904c-104">DRM\_LASignaturePrivKey</span></span>

<span data-ttu-id="9904c-105">La **propiedad \_ LASignaturePrivKey de DRM** contiene la clave privada que se usa para cifrar el encabezado DRM.</span><span class="sxs-lookup"><span data-stu-id="9904c-105">The **DRM\_LASignaturePrivKey** property contains the private key that is used to encrypt the DRM header.</span></span>

## <a name="global-constant"></a><span data-ttu-id="9904c-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="9904c-106">Global Constant</span></span>

<span data-ttu-id="9904c-107">g \_ wszWMDRM \_ LASignaturePrivKey</span><span class="sxs-lookup"><span data-stu-id="9904c-107">g\_wszWMDRM\_LASignaturePrivKey</span></span>

## <a name="data-type"></a><span data-ttu-id="9904c-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9904c-108">Data Type</span></span>

<span data-ttu-id="9904c-109">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="9904c-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="9904c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9904c-110">Remarks</span></span>

<span data-ttu-id="9904c-111">Esta propiedad se puede generar mediante el método [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) .</span><span class="sxs-lookup"><span data-stu-id="9904c-111">This property can be generated using the [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) method.</span></span> <span data-ttu-id="9904c-112">Esta propiedad debe ser un secreto conocido solo por el creador del contenido.</span><span class="sxs-lookup"><span data-stu-id="9904c-112">This property should remain a secret known only by the content creator.</span></span> <span data-ttu-id="9904c-113">Esta propiedad se puede establecer con el método [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) .</span><span class="sxs-lookup"><span data-stu-id="9904c-113">This property can be set with the [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) method.</span></span> <span data-ttu-id="9904c-114">No es accesible para el objeto lector.</span><span class="sxs-lookup"><span data-stu-id="9904c-114">It is not accessible to the reader object.</span></span>

## <a name="see-also"></a><span data-ttu-id="9904c-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="9904c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9904c-116">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="9904c-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




