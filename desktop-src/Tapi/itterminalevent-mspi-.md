---
description: Cuando el método ITTAPIEventNotification::Event devuelve TAPI EVENT igual a TE TERMINAL, los métodos expuestos por la interfaz \_ ITTerminalEvent se pueden usar para recuperar información sobre el evento de terminal que se ha producido, si existe un \_ MSP.
ms.assetid: 5277776e-0471-41b6-b662-4346a9d237ec
title: ITTerminalEvent (MSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593b9a7d048db9843825ccde8b22d0585a0c07fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160626"
---
# <a name="itterminalevent-mspi"></a>ITTerminalEvent (MSPI)

Cuando el [**método ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) devuelve [**TAPI \_ EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) igual a **TE \_ TERMINAL**, los métodos expuestos por la interfaz **ITTerminalEvent** se pueden usar para recuperar información sobre el evento de terminal que se ha producido, si existe un MSP.

La **interfaz ITTerminalEvent** se implementa mediante un MSP y no está disponible si no hay ningún proveedor de servicios multimedia asociado a la dirección. Consulte **ITTerminalEvent en** la sección Interfaz MSP para obtener más información sobre esta interfaz.

 

 



