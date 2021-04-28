---
description: 'MF_MT_FSSourceTypeDecoded atributo : especifica si un descodificador puede usar marcas de tiempo de descodificación (DTS) al establecer marcas de tiempo.'
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3799c11e3b921427ff4a3b05aa3d7f47e297ba14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093093"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a><span data-ttu-id="1e6f5-103">Atributo \_ MF MT \_ FSSourceTypeDecoded</span><span class="sxs-lookup"><span data-stu-id="1e6f5-103">MF\_MT\_FSSourceTypeDecoded attribute</span></span>

<span data-ttu-id="1e6f5-104">Especifica que un tipo de medio se descodifica automáticamente.</span><span class="sxs-lookup"><span data-stu-id="1e6f5-104">Specifies that a media type is auto-decoded.</span></span>

## <a name="data-type"></a><span data-ttu-id="1e6f5-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1e6f5-105">Data type</span></span>

<span data-ttu-id="1e6f5-106">**BOOL almacenado** como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="1e6f5-106">**BOOL** stored as **UINT32**</span></span>


## <a name="remarks"></a><span data-ttu-id="1e6f5-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e6f5-107">Remarks</span></span>
<span data-ttu-id="1e6f5-108">Un tipo de medio se marca como un atributo para indicar que esto no existe en el origen físico y se sintetiza mediante la canalización.</span><span class="sxs-lookup"><span data-stu-id="1e6f5-108">A media type is marked an attribute to indicate this doesn't exist on the physical source and is synthesized by the pipeline.</span></span> <span data-ttu-id="1e6f5-109">Un valor de 1 (TRUE) indica que el tipo de medio está sintetizado.</span><span class="sxs-lookup"><span data-stu-id="1e6f5-109">A value of 1 (TRUE) indicates that the media type is synthesized.</span></span> <span data-ttu-id="1e6f5-110">Un valor de 0 (FALSE) o el valor que no está presente indica que no lo está.</span><span class="sxs-lookup"><span data-stu-id="1e6f5-110">A value of 0 (FALSE), or the value not being present, indicates that it is not.</span></span>

<span data-ttu-id="1e6f5-111">En la versión actual, este atributo debe especificarse con el siguiente valor GUID en lugar de la MD_MT_FSSourceTypeDecoded constante:</span><span class="sxs-lookup"><span data-stu-id="1e6f5-111">In the current release, this attribute should be specified using the following GUID value rather than the MD_MT_FSSourceTypeDecoded constant:</span></span>

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a><span data-ttu-id="1e6f5-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e6f5-112">Requirements</span></span>



| <span data-ttu-id="1e6f5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e6f5-113">Requirement</span></span> | <span data-ttu-id="1e6f5-114">Valor</span><span class="sxs-lookup"><span data-stu-id="1e6f5-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e6f5-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e6f5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1e6f5-116">Windows 8 aplicaciones \[ de escritorio \| para aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="1e6f5-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="1e6f5-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e6f5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1e6f5-118">Aplicaciones de escritorio de Windows Server 2012 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="1e6f5-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |



## <a name="see-also"></a><span data-ttu-id="1e6f5-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1e6f5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e6f5-120">Lista alfabética de Media Foundation atributos</span><span class="sxs-lookup"><span data-stu-id="1e6f5-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




