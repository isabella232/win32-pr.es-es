---
title: DRM_KeySeed
description: La \_ propiedad KeySeed de DRM contiene la inicialización de clave que se utilizará junto con el ID. de clave para crear la clave.
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- DRM_KeySeed formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 698db5fe5a1123af0a7b4623d304bf0569bbf253
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105676345"
---
# <a name="drm_keyseed"></a><span data-ttu-id="3de59-104">\_KEYSEED DRM</span><span class="sxs-lookup"><span data-stu-id="3de59-104">DRM\_KeySeed</span></span>

<span data-ttu-id="3de59-105">La **propiedad \_ KeySeed de DRM** contiene la inicialización de clave que se utilizará junto con el ID. de clave para crear la clave.</span><span class="sxs-lookup"><span data-stu-id="3de59-105">The **DRM\_KeySeed** property contains the key seed that will be used in conjunction with the KeyID to create the key.</span></span>

## <a name="global-constant"></a><span data-ttu-id="3de59-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="3de59-106">Global Constant</span></span>

<span data-ttu-id="3de59-107">g \_ wszWMDRM \_ KeySeed</span><span class="sxs-lookup"><span data-stu-id="3de59-107">g\_wszWMDRM\_KeySeed</span></span>

## <a name="data-type"></a><span data-ttu-id="3de59-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3de59-108">Data Type</span></span>

<span data-ttu-id="3de59-109">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="3de59-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="3de59-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3de59-110">Remarks</span></span>

<span data-ttu-id="3de59-111">Esta propiedad se puede establecer mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="3de59-111">This property can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span> <span data-ttu-id="3de59-112">No es accesible para el objeto lector.</span><span class="sxs-lookup"><span data-stu-id="3de59-112">It is not accessible by the reader object.</span></span>

<span data-ttu-id="3de59-113">Una inicialización de clave se usa normalmente para proteger varios archivos o conjuntos de archivos, por ejemplo, todos los archivos emitidos por un servidor de licencias, o quizás todos los archivos de un intérprete determinado.</span><span class="sxs-lookup"><span data-stu-id="3de59-113">A key seed is typically used to protect multiple files or sets of files, for example all the files issued by a license server, or perhaps all the files by a particular artist.</span></span> <span data-ttu-id="3de59-114">Sin embargo, el ID. de la archivo es único para cada archivo.</span><span class="sxs-lookup"><span data-stu-id="3de59-114">The KeyID, however, is unique for each file.</span></span>

<span data-ttu-id="3de59-115">La inicialización de clave debe ser un secreto que solo se comparta entre el creador de contenido y el distribuidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="3de59-115">The key seed must remain a secret that is shared only between the content creator and the license distributor.</span></span> <span data-ttu-id="3de59-116">Este valor no se almacena en el encabezado DRM y no es necesario ni está accesible para las aplicaciones de reproductor DRM.</span><span class="sxs-lookup"><span data-stu-id="3de59-116">This value is not stored in the DRM header and it is neither needed by nor accessible to DRM player applications.</span></span>

<span data-ttu-id="3de59-117">Se puede generar un nuevo inicialización de clave mediante el método [**IWMDRMWriter:: GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) o cualquier otro medio adecuado.</span><span class="sxs-lookup"><span data-stu-id="3de59-117">A new key seed can be generated using the [**IWMDRMWriter::GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) method or by any other suitable means.</span></span>

## <a name="see-also"></a><span data-ttu-id="3de59-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="3de59-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de59-119">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="3de59-119">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




