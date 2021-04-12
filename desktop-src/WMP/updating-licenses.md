---
title: Actualización de licencias
description: Actualización de licencias
ms.assetid: b298badf-efcf-423c-8cc7-c3f50ab288a0
keywords:
- Windows Media Player tiendas en línea, actualizar licencias
- tiendas en línea, actualizar licencias
- tipo 1 almacenes en línea, actualizar licencias
- Windows Media Player tiendas en línea, actualización de licencias
- tiendas en línea, actualización de licencias
- tipo 1 almacenes en línea, actualización de licencias
- actualización de licencias
- licencias, actualizar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154959b01c93719184e310b60dffaa91fe2dcfa0
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358686"
---
# <a name="updating-licenses"></a><span data-ttu-id="957c1-111">Actualización de licencias</span><span class="sxs-lookup"><span data-stu-id="957c1-111">Updating Licenses</span></span>

<span data-ttu-id="957c1-112">Las tiendas en línea pueden proporcionar contenido con licencia durante un período de tiempo específico o hasta una fecha determinada.</span><span class="sxs-lookup"><span data-stu-id="957c1-112">Online stores can deliver content that is licensed for a specific period of time or until a certain date.</span></span> <span data-ttu-id="957c1-113">Esto sería normal para el contenido de música que se entrega como parte de un acuerdo de servicio de suscripción.</span><span class="sxs-lookup"><span data-stu-id="957c1-113">This would be normal for music content delivered as part of a subscription service agreement.</span></span> <span data-ttu-id="957c1-114">En este caso, la tienda en línea tiene la oportunidad de actualizar estas licencias antes de que expiren, suponiendo que el usuario ha pagado por renovar su suscripción.</span><span class="sxs-lookup"><span data-stu-id="957c1-114">In this case, the online store needs an opportunity to update these licenses before they expire, assuming, of course, that the user has paid to renew his or her subscription.</span></span> <span data-ttu-id="957c1-115">(Si el usuario no ha renovado la suscripción, las licencias solo pueden dejar de ser válidas).</span><span class="sxs-lookup"><span data-stu-id="957c1-115">(If the user has not renewed the subscription, the licenses can simply be left to expire.)</span></span>

<span data-ttu-id="957c1-116">Windows Media Player consulta el complemento de asociado de contenido sobre la cantidad de advertencia anticipada que el reproductor debe proporcionar sobre una licencia que está a punto de expirar.</span><span class="sxs-lookup"><span data-stu-id="957c1-116">Windows Media Player queries the content partner plug-in about how much advance warning the Player should provide about a license that is about to expire.</span></span> <span data-ttu-id="957c1-117">Para ello, llama a [IWMPContentPartner:: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), pasando la constante g \_ szContentPartnerInfo \_ LicenseRefreshAdvanceWarning a través del parámetro *bstrInfoName* .</span><span class="sxs-lookup"><span data-stu-id="957c1-117">It does this by calling [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), passing the constant g\_szContentPartnerInfo\_LicenseRefreshAdvanceWarning through the *bstrInfoName* parameter.</span></span> <span data-ttu-id="957c1-118">Para avisar al complemento acerca de las licencias que están a punto de expirar, Windows Media Player llama a [IWMPContentPartner:: RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense).</span><span class="sxs-lookup"><span data-stu-id="957c1-118">To alert the plug-in about licenses that are about to expire, Windows Media Player calls [IWMPContentPartner::RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense).</span></span> <span data-ttu-id="957c1-119">Esta llamada toma parámetros que proporcionan detalles sobre el archivo que se está actualizando, por ejemplo, si el archivo está en el equipo del usuario y la ruta de acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="957c1-119">This call takes parameters that provide details about the file being refreshed, such as whether the file is on the user's computer, and the path to the file.</span></span> <span data-ttu-id="957c1-120">Si la licencia se actualiza como parte de una operación de sincronización de dispositivos, el parámetro *pReasonContext* proporciona el nombre no cañón del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="957c1-120">If the license is being refreshed as part of a device synchronization operation, the *pReasonContext* parameter supplies the cannonical name of the device</span></span>

<span data-ttu-id="957c1-121">Cuando Windows Media Player llama a **RefreshLicence**, pasa una cookie que identifica la solicitud de actualización.</span><span class="sxs-lookup"><span data-stu-id="957c1-121">When Windows Media Player calls **RefreshLicence**, it passes a cookie that identifies the update request.</span></span> <span data-ttu-id="957c1-122">Cuando el complemento ha terminado de procesar la solicitud de actualización, notifica a Windows Media Player llamando a [IWMPContentPartnerCallback:: RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), pasando la cookie, el identificador del elemento multimedia y un **valor HRESULT** que indica si la actualización se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="957c1-122">When the plug-in has finished processing the update request, it notifies Windows Media Player by calling [IWMPContentPartnerCallback::RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), passing the cookie, the ID of the media item, and an **HRESULT** that indicates whether the update was successful.</span></span>

<span data-ttu-id="957c1-123">Los complementos de la tienda en línea también pueden realizar la inspección de licencias y las actualizaciones como un proceso en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="957c1-123">Online store plug-ins can also do license inspection and updates as a background process.</span></span> <span data-ttu-id="957c1-124">Windows Media Player notifica el complemento sobre los momentos en los que se permite realizar tareas de procesamiento en segundo plano mediante una llamada a [IWMPContentPartner:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify).</span><span class="sxs-lookup"><span data-stu-id="957c1-124">Windows Media Player notifies the plug-in about times when it is permissible to perform background processing tasks by calling [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify).</span></span> <span data-ttu-id="957c1-125">Para indicar al complemento que inicie el procesamiento en segundo plano, el reproductor pasa el valor de enumeración [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) wmpsnBackgroundProcessingBegin; para indicar al complemento que detenga el procesamiento en segundo plano, el reproductor pasa el valor wmpsnBackgroundProcessingEnd.</span><span class="sxs-lookup"><span data-stu-id="957c1-125">To signal the plug-in to start background processing, the Player passes the [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) enumeration value wmpsnBackgroundProcessingBegin; to signal the plug-in to stop background processing, the Player passes the value wmpsnBackgroundProcessingEnd.</span></span>

## <a name="related-topics"></a><span data-ttu-id="957c1-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="957c1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="957c1-127">**Guía de programación para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="957c1-127">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




