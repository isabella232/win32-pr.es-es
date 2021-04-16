---
description: Especifica la clase del servicio Programador de clases multimedia (MMCSS) para el subproceso de descodificación.
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: Propiedad AVDecMmcss (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0092ac516f9600929a9772d044f51e7e375548d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671624"
---
# <a name="avdecmmcss-property"></a><span data-ttu-id="ed957-103">Propiedad AVDecMmcss</span><span class="sxs-lookup"><span data-stu-id="ed957-103">AVDecMmcss property</span></span>

<span data-ttu-id="ed957-104">Especifica la clase del servicio Programador de clases multimedia (MMCSS) para el subproceso de descodificación.</span><span class="sxs-lookup"><span data-stu-id="ed957-104">Specifies the Multimedia Class Scheduler Service (MMCSS) class for the decoding thread.</span></span>

<span data-ttu-id="ed957-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ed957-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="ed957-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ed957-106">Data type</span></span>

<span data-ttu-id="ed957-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="ed957-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ed957-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="ed957-108">Property GUID</span></span>

<span data-ttu-id="ed957-109">**CODECAPI \_ AVDecMmcssClass**</span><span class="sxs-lookup"><span data-stu-id="ed957-109">**CODECAPI\_AVDecMmcssClass**</span></span>

## <a name="property-value"></a><span data-ttu-id="ed957-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ed957-110">Property value</span></span>

<span data-ttu-id="ed957-111">El valor de esta propiedad es el nombre de la clase MMCSS.</span><span class="sxs-lookup"><span data-stu-id="ed957-111">The value of this property is the name of the MMCSS class.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed957-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed957-112">Remarks</span></span>

<span data-ttu-id="ed957-113">MMCSS permite a las aplicaciones asegurarse de que el procesamiento dependiente del tiempo ha priorizado el acceso a los recursos de la CPU.</span><span class="sxs-lookup"><span data-stu-id="ed957-113">MMCSS enables applications to ensure that time-sensitive processing has prioritized access to CPU resources.</span></span> <span data-ttu-id="ed957-114">Funciona mediante la elevación de subprocesos registrados a prioridades de subprocesos mayores, a la vez que reduce periódicamente sus prioridades para dar tiempo a otros procesos.</span><span class="sxs-lookup"><span data-stu-id="ed957-114">It works by elevating registered threads to higher thread priorities while periodically decreasing their priorities to yield time to other processes.</span></span>

<span data-ttu-id="ed957-115">El valor recomendado para los descodificadores de audio es "audio", y el valor recomendado para los descodificadores de vídeo es "reproducción".</span><span class="sxs-lookup"><span data-stu-id="ed957-115">The recommended value for audio decoders is "Audio," and the recommended value for video decoders is "Playback."</span></span>

<span data-ttu-id="ed957-116">Si el servicio MMCSS no está disponible o la clase de MMCSS especificada no existe, el establecimiento de la propiedad no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="ed957-116">If the MMCSS service is not available or the specified MMCSS class does not exist, setting the property has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed957-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed957-117">Requirements</span></span>



| <span data-ttu-id="ed957-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed957-118">Requirement</span></span> | <span data-ttu-id="ed957-119">Value</span><span class="sxs-lookup"><span data-stu-id="ed957-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed957-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed957-120">Header</span></span><br/> | <dl> <span data-ttu-id="ed957-121"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed957-121"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed957-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed957-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed957-123">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="ed957-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ed957-124">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="ed957-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




