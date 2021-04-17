---
description: Especifica si un descodificador puede usar marcas de tiempo de descodificación (DTS) al establecer las marcas de tiempo.
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ad80b0b7b29677ed0bee2f86a2c12c56c08441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720764"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a><span data-ttu-id="9b97b-103">\_Atributo MF MT \_ FSSourceTypeDecoded</span><span class="sxs-lookup"><span data-stu-id="9b97b-103">MF\_MT\_FSSourceTypeDecoded attribute</span></span>

<span data-ttu-id="9b97b-104">Especifica que un tipo de medio se descodifica automáticamente.</span><span class="sxs-lookup"><span data-stu-id="9b97b-104">Specifies that a media type is auto-decoded.</span></span>

## <a name="data-type"></a><span data-ttu-id="9b97b-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9b97b-105">Data type</span></span>

<span data-ttu-id="9b97b-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="9b97b-106">**BOOL** stored as **UINT32**</span></span>


## <a name="remarks"></a><span data-ttu-id="9b97b-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b97b-107">Remarks</span></span>
<span data-ttu-id="9b97b-108">Un tipo de medio se marca como atributo para indicar que no existe en el origen físico y está sintetizado por la canalización.</span><span class="sxs-lookup"><span data-stu-id="9b97b-108">A media type is marked an attribute to indicate this doesn't exist on the physical source and is synthesized by the pipeline.</span></span> <span data-ttu-id="9b97b-109">Un valor de 1 (TRUE) indica que el tipo de medio es sintetizado.</span><span class="sxs-lookup"><span data-stu-id="9b97b-109">A value of 1 (TRUE) indicates that the media type is synthesized.</span></span> <span data-ttu-id="9b97b-110">Un valor de 0 (FALSE) o el valor que no está presente indica que no lo está.</span><span class="sxs-lookup"><span data-stu-id="9b97b-110">A value of 0 (FALSE), or the value not being present, indicates that it is not.</span></span>

<span data-ttu-id="9b97b-111">En la versión actual, este atributo se debe especificar utilizando el siguiente valor de GUID en lugar de la constante MD_MT_FSSourceTypeDecoded:</span><span class="sxs-lookup"><span data-stu-id="9b97b-111">In the current release, this attribute should be specified using the following GUID value rather than the MD_MT_FSSourceTypeDecoded constant:</span></span>

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a><span data-ttu-id="9b97b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b97b-112">Requirements</span></span>



| <span data-ttu-id="9b97b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b97b-113">Requirement</span></span> | <span data-ttu-id="9b97b-114">Value</span><span class="sxs-lookup"><span data-stu-id="9b97b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b97b-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b97b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9b97b-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="9b97b-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="9b97b-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b97b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9b97b-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="9b97b-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |



## <a name="see-also"></a><span data-ttu-id="9b97b-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b97b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b97b-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9b97b-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




