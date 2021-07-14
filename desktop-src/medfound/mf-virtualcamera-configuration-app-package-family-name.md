---
description: Especifica el nombre de familia del paquete de aplicación para una aplicación de configuración de cámara virtual.
title: MF_VIRTUALCAMERA_APP_PACKAGE_FAMILY_NAME atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/24/2021
ms.openlocfilehash: e821a273c44b1d5c9e654e34bbfb928ea707cdc0
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691870"
---
# <a name="mf_virtualcamera_app_package_family_name-attribute"></a><span data-ttu-id="615d8-103">Atributo MF \_ VIRTUALCAMERA \_ APP PACKAGE FAMILY \_ \_ \_ NAME</span><span class="sxs-lookup"><span data-stu-id="615d8-103">MF\_VIRTUALCAMERA\_APP\_PACKAGE\_FAMILY\_NAME attribute</span></span>

<span data-ttu-id="615d8-104">Especifica el nombre de familia del paquete de aplicación para una aplicación de configuración de cámara virtual.</span><span class="sxs-lookup"><span data-stu-id="615d8-104">Specifies the app package family name for a virtual camera configuration application.</span></span> <span data-ttu-id="615d8-105">Cuando se proporciona, la canalización asociará la aplicación de configuración a la cámara virtual y proporcionará un punto de inicio dentro de la página Configuración cámara.</span><span class="sxs-lookup"><span data-stu-id="615d8-105">When provided, the pipeline will associate the configuration application with the virtual camera and provide a launch point within the Camera Settings page.</span></span>

## <a name="data-type"></a><span data-ttu-id="615d8-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="615d8-106">Data type</span></span>

[<span data-ttu-id="615d8-107">MF_ATTRIBUTE_STRING</span><span class="sxs-lookup"><span data-stu-id="615d8-107">MF_ATTRIBUTE_STRING</span></span>](/windows/win32/api/mfobjects/ne-mfobjects-mf_attribute_type)

## <a name="remarks"></a><span data-ttu-id="615d8-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="615d8-108">Remarks</span></span>

<span data-ttu-id="615d8-109">El origen multimedia personalizado de la cámara virtual puede exponer este atributo desde el almacén de atributos de origen multimedia [IMFMediaSourceEx::GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).</span><span class="sxs-lookup"><span data-stu-id="615d8-109">This attribute may be exposed by the virtual camera custom media source from the media source attribute store [IMFMediaSourceEx::GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).</span></span>  

<span data-ttu-id="615d8-110">Si la aplicación de configuración aún no está instalada en el equipo, la aplicación Store se inicia y se navega a la página de la aplicación especificada por el nombre de familia del paquete.</span><span class="sxs-lookup"><span data-stu-id="615d8-110">If the configuration application is not yet installed on the machine, the Store application will be launched and navigated to the application page specified by the package family name.</span></span> <span data-ttu-id="615d8-111">De lo contrario, se inicia la aplicación instalada para el usuario.</span><span class="sxs-lookup"><span data-stu-id="615d8-111">Otherwise, the installed application will be launched for the user.</span></span>


## <a name="requirements"></a><span data-ttu-id="615d8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="615d8-112">Requirements</span></span>



| <span data-ttu-id="615d8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="615d8-113">Requirement</span></span> | <span data-ttu-id="615d8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="615d8-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="615d8-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="615d8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="615d8-116">Windows Compilación 22000</span><span class="sxs-lookup"><span data-stu-id="615d8-116">Windows Build 22000</span></span><br/>                          |
| <span data-ttu-id="615d8-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="615d8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="615d8-118">Windows Compilación 22000</span><span class="sxs-lookup"><span data-stu-id="615d8-118">Windows Build 22000</span></span><br/>                      |
| <span data-ttu-id="615d8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="615d8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="615d8-120"><dt>Mfapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="615d8-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="615d8-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="615d8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="615d8-122">Lista alfabética de Media Foundation atributos</span><span class="sxs-lookup"><span data-stu-id="615d8-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="615d8-123">**ATTRIBUTEAttributes::GetString**</span><span class="sxs-lookup"><span data-stu-id="615d8-123">**IMFAttributes::GetString**</span></span>](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="615d8-124">**ATTRIBUTEAttributes::SetString**</span><span class="sxs-lookup"><span data-stu-id="615d8-124">**IMFAttributes::SetString**</span></span>](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> 
</dl>
 




