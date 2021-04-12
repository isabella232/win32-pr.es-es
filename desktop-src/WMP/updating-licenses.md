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
# <a name="updating-licenses"></a>Actualización de licencias

Las tiendas en línea pueden proporcionar contenido con licencia durante un período de tiempo específico o hasta una fecha determinada. Esto sería normal para el contenido de música que se entrega como parte de un acuerdo de servicio de suscripción. En este caso, la tienda en línea tiene la oportunidad de actualizar estas licencias antes de que expiren, suponiendo que el usuario ha pagado por renovar su suscripción. (Si el usuario no ha renovado la suscripción, las licencias solo pueden dejar de ser válidas).

Windows Media Player consulta el complemento de asociado de contenido sobre la cantidad de advertencia anticipada que el reproductor debe proporcionar sobre una licencia que está a punto de expirar. Para ello, llama a [IWMPContentPartner:: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), pasando la constante g \_ szContentPartnerInfo \_ LicenseRefreshAdvanceWarning a través del parámetro *bstrInfoName* . Para avisar al complemento acerca de las licencias que están a punto de expirar, Windows Media Player llama a [IWMPContentPartner:: RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense). Esta llamada toma parámetros que proporcionan detalles sobre el archivo que se está actualizando, por ejemplo, si el archivo está en el equipo del usuario y la ruta de acceso al archivo. Si la licencia se actualiza como parte de una operación de sincronización de dispositivos, el parámetro *pReasonContext* proporciona el nombre no cañón del dispositivo.

Cuando Windows Media Player llama a **RefreshLicence**, pasa una cookie que identifica la solicitud de actualización. Cuando el complemento ha terminado de procesar la solicitud de actualización, notifica a Windows Media Player llamando a [IWMPContentPartnerCallback:: RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), pasando la cookie, el identificador del elemento multimedia y un **valor HRESULT** que indica si la actualización se realizó correctamente.

Los complementos de la tienda en línea también pueden realizar la inspección de licencias y las actualizaciones como un proceso en segundo plano. Windows Media Player notifica el complemento sobre los momentos en los que se permite realizar tareas de procesamiento en segundo plano mediante una llamada a [IWMPContentPartner:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify). Para indicar al complemento que inicie el procesamiento en segundo plano, el reproductor pasa el valor de enumeración [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) wmpsnBackgroundProcessingBegin; para indicar al complemento que detenga el procesamiento en segundo plano, el reproductor pasa el valor wmpsnBackgroundProcessingEnd.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación para las tiendas en línea de tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




