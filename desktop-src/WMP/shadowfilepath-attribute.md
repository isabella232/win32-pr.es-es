---
title: Atributo ShadowFilePath
description: El atributo ShadowFilePath es la ruta de acceso completa a un archivo de instantáneas.
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- ShadowFilePath Media Player de Windows
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef79271995e9817315fb918049fc22491e232a5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653569"
---
# <a name="shadowfilepath-attribute"></a><span data-ttu-id="4fb76-104">Atributo ShadowFilePath</span><span class="sxs-lookup"><span data-stu-id="4fb76-104">ShadowFilePath Attribute</span></span>

<span data-ttu-id="4fb76-105">El atributo **ShadowFilePath** es la ruta de acceso completa a un archivo de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="4fb76-105">The **ShadowFilePath** attribute is the fully qualified path to a shadow file.</span></span>

## <a name="applies-to"></a><span data-ttu-id="4fb76-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="4fb76-106">Applies To</span></span>

-   [<span data-ttu-id="4fb76-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="4fb76-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="4fb76-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fb76-108">Remarks</span></span>

<span data-ttu-id="4fb76-109">Un *archivo de instantánea* se crea como parte de una conversión de formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="4fb76-109">A *shadow file* is created as part of a file format conversion.</span></span> <span data-ttu-id="4fb76-110">Es la copia de un archivo que usa el reproductor cuando el usuario sincroniza el contenido del equipo con un dispositivo que requiere que el contenido esté en el formato de archivo original.</span><span class="sxs-lookup"><span data-stu-id="4fb76-110">It is the copy of a file that the Player uses when the user syncs content from the computer to a device that requires the content to be in the original file format.</span></span> <span data-ttu-id="4fb76-111">Este atributo se establece para que el archivo convertido señale a la ubicación del archivo de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="4fb76-111">This attribute is set for the converted file to point to the location of the shadow file.</span></span>

<span data-ttu-id="4fb76-112">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="4fb76-112">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fb76-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fb76-113">Requirements</span></span>



| <span data-ttu-id="4fb76-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fb76-114">Requirement</span></span> | <span data-ttu-id="4fb76-115">Value</span><span class="sxs-lookup"><span data-stu-id="4fb76-115">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="4fb76-116">Versión</span><span class="sxs-lookup"><span data-stu-id="4fb76-116">Version</span></span><br/> | <span data-ttu-id="4fb76-117">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="4fb76-117">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4fb76-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fb76-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb76-119">**Acerca del proceso de conversión**</span><span class="sxs-lookup"><span data-stu-id="4fb76-119">**About the Conversion Process**</span></span>](about-the-conversion-process.md)
</dt> <dt>

[<span data-ttu-id="4fb76-120">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="4fb76-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





