---
title: Interfaz IWMDRMIndividualizationStatus
description: La interfaz IWMDRMIndividualizationStatus permite recuperar información de estado avanzada sobre el progreso de la individualización. Esta interfaz se entrega con eventos MEWMDRMIndividualizationProgress.
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- IWMDRMIndividualizationStatus interface windows Media Format
- IWMDRMIndividualizationStatus interfaz windows Media Format , descrito
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19a369bf9b70d9a43af8a48f13f1b8bbb87525b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256268"
---
# <a name="iwmdrmindividualizationstatus-interface"></a>Interfaz IWMDRMIndividualizationStatus

La **interfaz IWMDRMIndividualizationStatus** permite recuperar información de estado avanzada sobre el progreso de la individualización.

Esta interfaz se entrega con eventos MEWMDRMIndividualizationProgress. Muchos de estos eventos se generan entre una llamada a [**IWMDRMSecurity::P erformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) y la finalización del proceso de individualización, que se señala mediante la generación de un evento **MEWMDRMIndividualizationCompleted.**

Para recuperar un puntero a una instancia de la interfaz **IWMDRMIndividualizationStatus,** primero debe llamar al método **IMFMediaEvent::GetValue** del evento progress. El valor que se recupera del evento es un puntero a la interfaz **IUnknown** del objeto que implementa la **interfaz IWMDRMIndividualizationStatus.**

## <a name="members"></a>Members

La **interfaz IWMDRMIndividualizationStatus** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMIndividualizationStatus** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMDRMIndividualizationStatus** tiene estos métodos.



| Método                                                       | Descripción                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [**GetStatus**](iwmdrmindividualizationstatus-getstatus.md) | Recupera información detallada sobre la individualización.<br/> |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

