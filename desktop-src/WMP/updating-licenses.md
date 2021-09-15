---
title: Actualizar licencias
description: Actualizar licencias
ms.assetid: b298badf-efcf-423c-8cc7-c3f50ab288a0
keywords:
- Reproductor de Windows Media en línea, actualizar licencias
- tiendas en línea, actualizar licencias
- tiendas en línea de tipo 1, actualizar licencias
- Reproductor de Windows Media en línea, actualización de licencias
- tiendas en línea, actualización de licencias
- tiendas en línea de tipo 1, actualización de licencias
- actualizar licencias
- licenses,updating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154959b01c93719184e310b60dffaa91fe2dcfa0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465798"
---
# <a name="updating-licenses"></a>Actualizar licencias

Las tiendas en línea pueden entregar contenido con licencia durante un período de tiempo específico o hasta una fecha determinada. Esto sería normal para el contenido de música entregado como parte de un contrato de servicio de suscripción. En este caso, la tienda en línea necesita una oportunidad para actualizar estas licencias antes de que expiren, suponiendo, por supuesto, que el usuario haya pagado para renovar su suscripción. (Si el usuario no ha renovado la suscripción, las licencias simplemente se pueden dejar para que expiren).

Reproductor de Windows Media consulta el complemento del asociado de contenido sobre la cantidad de advertencia anticipada que debe proporcionar el reproductor sobre una licencia que está a punto de expirar. Para ello, llama a [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo)y pasa la constante g \_ szContentPartnerInfo \_ LicenseRefreshAdvanceWarning a través del *parámetro bstrInfoName.* Para alertar al complemento sobre las licencias que están a punto de expirar, Reproductor de Windows Media llama a [IWMPContentPartner::RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense). Esta llamada toma parámetros que proporcionan detalles sobre el archivo que se va a actualizar, como si el archivo está en el equipo del usuario y la ruta de acceso al archivo. Si la licencia se actualiza como parte de una operación de sincronización de dispositivos, el parámetro *pReasonContext* proporciona el nombre del dispositivo.

Cuando Reproductor de Windows Media **llama a RefreshLicence**, pasa una cookie que identifica la solicitud de actualización. Cuando el complemento ha terminado de procesar la solicitud de actualización, notifica a Reproductor de Windows Media mediante una llamada a [IWMPContentPartnerCallback::RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), pasando la cookie, el identificador del elemento multimedia y un **HRESULT** que indica si la actualización se ha realizado correctamente.

Los complementos de tienda en línea también pueden realizar la inspección de licencias y las actualizaciones como un proceso en segundo plano. Reproductor de Windows Media notifica al complemento las horas en las que está permitido realizar tareas de procesamiento en segundo plano mediante una llamada a [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify). Para indicar al complemento que inicie el procesamiento en segundo plano, el reproductor pasa el valor de enumeración [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) wmpsnBackgroundProcessingBegin; Para indicar al complemento que detenga el procesamiento en segundo plano, el reproductor pasa el valor wmpsnBackgroundProcessingEnd.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación para almacenes en línea de tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




