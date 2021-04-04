---
title: DRM_HeaderSignPrivKey
description: La \_ propiedad HeaderSignPrivKey de DRM contiene la clave privada utilizada para firmar el encabezado ASF.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- DRM_HeaderSignPrivKey formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af73ea90acca6c20817f35a035f8f297aa56e90b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788757"
---
# <a name="drm_headersignprivkey"></a><span data-ttu-id="b5310-104">\_HEADERSIGNPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="b5310-104">DRM\_HeaderSignPrivKey</span></span>

<span data-ttu-id="b5310-105">La **propiedad \_ HeaderSignPrivKey de DRM** contiene la clave privada utilizada para firmar el encabezado ASF.</span><span class="sxs-lookup"><span data-stu-id="b5310-105">The **DRM\_HeaderSignPrivKey** property contains the private key used to sign the ASF header.</span></span>

## <a name="global-constant"></a><span data-ttu-id="b5310-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="b5310-106">Global Constant</span></span>

<span data-ttu-id="b5310-107">g \_ wszWMDRM \_ HeaderSignPrivKey</span><span class="sxs-lookup"><span data-stu-id="b5310-107">g\_wszWMDRM\_HeaderSignPrivKey</span></span>

## <a name="data-type"></a><span data-ttu-id="b5310-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b5310-108">Data Type</span></span>

<span data-ttu-id="b5310-109">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b5310-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="b5310-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5310-110">Remarks</span></span>

<span data-ttu-id="b5310-111">Esta propiedad se genera mediante [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).</span><span class="sxs-lookup"><span data-stu-id="b5310-111">This property is generated using the [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).</span></span> <span data-ttu-id="b5310-112">Mantenga esta clave secreta y comparta la clave pública solo con el servicio de licencias.</span><span class="sxs-lookup"><span data-stu-id="b5310-112">Keep this key secret and share the public key only with the license service.</span></span> <span data-ttu-id="b5310-113">Después de establecer esta clave, el componente DRM la usará para firmar el encabezado del archivo ASF (no el encabezado DRM que está firmado con los valores del objeto de firma digital como \_ LASIGNATUREPRIVKEY DRM).</span><span class="sxs-lookup"><span data-stu-id="b5310-113">After you set this key, the DRM component will use it to sign the ASF file header (not the DRM header which is signed with the digital signature object values such as DRM\_LASignaturePrivKey).</span></span> <span data-ttu-id="b5310-114">Obviamente, **DRM \_ HeaderSignPrivKey** no se incluye en el encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="b5310-114">Obviously, **DRM\_HeaderSignPrivKey** is not included in the file headert.</span></span>

<span data-ttu-id="b5310-115">No se puede obtener acceso a esta propiedad desde el objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="b5310-115">This property is not accessible from the reader object.</span></span> <span data-ttu-id="b5310-116">Se puede establecer desde el objeto escritor mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="b5310-116">It can be set from the writer object using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span>

## <a name="see-also"></a><span data-ttu-id="b5310-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5310-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5310-118">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="b5310-118">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




