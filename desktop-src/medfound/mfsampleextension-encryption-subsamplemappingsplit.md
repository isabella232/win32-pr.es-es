---
description: Establece la asignación de submuestra para el ejemplo que indica los bytes claros y cifrados de los datos de ejemplo.
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: MFSampleExtension_Encryption_SubSampleMappingSplit atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c90fb6ae22417f059bfa3268382877363178940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720449"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a><span data-ttu-id="d4862-103">MFSampleExtension \_ Encryption \_ SubSampleMappingSplit Attribute</span><span class="sxs-lookup"><span data-stu-id="d4862-103">MFSampleExtension\_Encryption\_SubSampleMappingSplit attribute</span></span>

<span data-ttu-id="d4862-104">Establece la asignación de submuestra para el ejemplo que indica los bytes claros y cifrados de los datos de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d4862-104">Sets the sub-sample mapping for the sample indicating the clear and encrypted bytes in the sample data.</span></span>

## <a name="data-type"></a><span data-ttu-id="d4862-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d4862-105">Data type</span></span>

<span data-ttu-id="d4862-106">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="d4862-106">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="d4862-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4862-107">Remarks</span></span>

<span data-ttu-id="d4862-108">El **BLOB** debe contener una matriz de intervalos de bytes como DWORD, donde cada dos DWORD crea un conjunto.</span><span class="sxs-lookup"><span data-stu-id="d4862-108">The **BLOB** should contain an array of byte ranges as DWORDs where every two DWORDs makes a set.</span></span> <span data-ttu-id="d4862-109">El primer valor DWORD de cada conjunto es el número de bytes claros y el segundo valor DWORD del conjunto es el número de bytes cifrados.</span><span class="sxs-lookup"><span data-stu-id="d4862-109">The first DWORD in each set is the number of clear bytes and the second DWORD of the set is the number of encrypted bytes.</span></span> <span data-ttu-id="d4862-110">Tenga en cuenta que un par de 0s no es un conjunto válido (el valor puede ser 0, pero no ambos).</span><span class="sxs-lookup"><span data-stu-id="d4862-110">Note that a pair of 0s is not a valid set (either value can be 0, but not both).</span></span> <span data-ttu-id="d4862-111">La matriz de intervalos de bytes indica qué rangos se van a descifrar, incluida la posibilidad de que no se pueda descifrar toda la muestra.</span><span class="sxs-lookup"><span data-stu-id="d4862-111">The array of byte ranges indicate which ranges to decrypt, including the possibility that the entire sample should not be decrypted.</span></span> <span data-ttu-id="d4862-112">Se recomienda no establecerlo en ejemplos claros, aunque es posible lograr el mismo resultado si se establece con los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="d4862-112">It is recommended that this should not be set on clear samples, though it is possible to achieve the same result by setting it with the appropriate values.</span></span>

## <a name="examples"></a><span data-ttu-id="d4862-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d4862-113">Examples</span></span>

<span data-ttu-id="d4862-114">En el ejemplo siguiente se muestra cómo establecer el \_ cifrado MFSampleExtension \_ SubSampleMappingSplit.</span><span class="sxs-lookup"><span data-stu-id="d4862-114">The following example shows how to set MFSampleExtension\_Encryption\_SubSampleMappingSplit.</span></span>


```C++
// m_spSample is a IMFSample
// pdwSubSampleMap is a DWORD*
// dwSubSampleMapSize is a DWORD

m_spSample->SetBlob( MFSampleExtension_Encryption_SubSampleMappingSplit,
                    (BYTE*)pdwSubSampleMap, 
                    dwSubSampleMapSize * sizeof(DWORD) );
```



## <a name="requirements"></a><span data-ttu-id="d4862-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4862-115">Requirements</span></span>



| <span data-ttu-id="d4862-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4862-116">Requirement</span></span> | <span data-ttu-id="d4862-117">Value</span><span class="sxs-lookup"><span data-stu-id="d4862-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4862-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4862-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d4862-119">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="d4862-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="d4862-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4862-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d4862-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="d4862-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d4862-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4862-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4862-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4862-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4862-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4862-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4862-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d4862-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d4862-126">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="d4862-126">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="d4862-127">ID. de contenido de MFSampleExtension \_ \_</span><span class="sxs-lookup"><span data-stu-id="d4862-127">MFSampleExtension\_Content\_KeyID</span></span>](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




