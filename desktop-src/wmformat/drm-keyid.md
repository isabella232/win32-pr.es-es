---
title: DRM_KeyID
description: El atributo id. de clave de DRM \_ contiene el identificador de clave.
ms.assetid: 90406809-76d9-4559-afe8-6812efbc1477
keywords:
- DRM_KeyID formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a60afa330a7cf967b42a4d06009d9c921d8f56
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077348"
---
# <a name="drm_keyid"></a><span data-ttu-id="d959b-104">ID. de ID \_ de DRM</span><span class="sxs-lookup"><span data-stu-id="d959b-104">DRM\_KeyID</span></span>

<span data-ttu-id="d959b-105">El atributo id. de clave de **DRM \_** contiene el identificador de clave.</span><span class="sxs-lookup"><span data-stu-id="d959b-105">The **DRM\_KeyID** attribute contains the key identifier.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d959b-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="d959b-106">Global Constant</span></span>

<span data-ttu-id="d959b-107">ID. de \_ wszWMDRM g \_</span><span class="sxs-lookup"><span data-stu-id="d959b-107">g\_wszWMDRM\_KeyID</span></span>

## <a name="data-type"></a><span data-ttu-id="d959b-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d959b-108">Data Type</span></span>

<span data-ttu-id="d959b-109">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d959b-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="d959b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d959b-110">Remarks</span></span>

<span data-ttu-id="d959b-111">Este atributo solo está presente para el contenido de la versión 7 de DRM.</span><span class="sxs-lookup"><span data-stu-id="d959b-111">This attribute is present for DRM Version 7 content only.</span></span> <span data-ttu-id="d959b-112">Se puede establecer mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="d959b-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="d959b-113">Se puede recuperar el mismo atributo de archivo mediante el ID. de [**\_ \_ DRMHeader de DRM**](drm-drmheader-keyid.md).</span><span class="sxs-lookup"><span data-stu-id="d959b-113">The same file attribute can be retrieved using [**DRM\_DRMHeader\_KeyID**](drm-drmheader-keyid.md).</span></span>

<span data-ttu-id="d959b-114">El identificador de clave se utiliza junto con la inicialización de clave para crear la clave de contenido que se usa para cifrar y descifrar el archivo.</span><span class="sxs-lookup"><span data-stu-id="d959b-114">The key ID is used in conjunction with the key seed to create the content key which is used to encrypt and decrypt the file.</span></span> <span data-ttu-id="d959b-115">La aplicación de escritura usa el identificador de clave para cifrar el archivo y, a continuación, almacena el identificador de clave en el encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="d959b-115">The writer application uses the key ID to encrypt the file and then it stores the key ID in the file header.</span></span> <span data-ttu-id="d959b-116">Cuando una aplicación de reproducción solicita una licencia para un archivo, el componente DRM envía el identificador de clave (junto con el resto del encabezado DRM) al servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="d959b-116">When a player application requests a license for a file, the DRM component sends the key ID (along with the rest of the DRM header) to the license server.</span></span> <span data-ttu-id="d959b-117">El servidor de licencias, que tiene la clave secreta SEED, lo utiliza y el identificador de clave para crear una clave para el archivo, que después inserta en una licencia junto con los distintos derechos que se aplicarán al archivo.</span><span class="sxs-lookup"><span data-stu-id="d959b-117">The license server, which has the secret key seed, uses it and the key ID to create a key for the file, which it then inserts into a license along with the various rights that will be applied to the file.</span></span>

<span data-ttu-id="d959b-118">Normalmente, se usa una inicialización de clave con varios identificadores de clave.</span><span class="sxs-lookup"><span data-stu-id="d959b-118">Typically, one key seed is used with many key IDs.</span></span> <span data-ttu-id="d959b-119">La inicialización de clave es un secreto compartido solo por el creador de contenido y el distribuidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="d959b-119">The key seed is a secret shared only by the content creator and the license distributor.</span></span> <span data-ttu-id="d959b-120">El identificador de clave lo usan las aplicaciones cliente de DRM y se almacena en el encabezado DRM en el borrado.</span><span class="sxs-lookup"><span data-stu-id="d959b-120">The key ID is used by DRM client applications and is stored in the DRM header in the clear.</span></span>

<span data-ttu-id="d959b-121">Este atributo es igual que el ID. de [**\_ \_ DRMHeader de DRM**](drm-drmheader-keyid.md).</span><span class="sxs-lookup"><span data-stu-id="d959b-121">This attribute is the same as [**DRM\_DRMHeader\_KeyID**](drm-drmheader-keyid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d959b-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d959b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d959b-123">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="d959b-123">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




