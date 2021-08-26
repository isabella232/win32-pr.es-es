---
description: Cuando el método ITTAPIEventNotification::Event devuelve TAPI EVENT igual a TE TERMINAL, los métodos expuestos por la interfaz \_ ITTerminalEvent se pueden usar para recuperar información sobre el evento de terminal que se ha producido, si existe un \_ MSP.
ms.assetid: 5277776e-0471-41b6-b662-4346a9d237ec
title: ITTerminalEvent (MSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc5177fee1998639b4e01213eb1662f4046219e7c9093c6f2e1d1db5a6e0626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012815"
---
# <a name="itterminalevent-mspi"></a>ITTerminalEvent (MSPI)

Cuando el [**método ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) devuelve [**TAPI \_ EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) igual a **TE \_ TERMINAL**, los métodos expuestos por la interfaz **ITTerminalEvent** se pueden usar para recuperar información sobre el evento de terminal que se ha producido, si existe un MSP.

La **interfaz ITTerminalEvent** se implementa mediante un MSP y no está disponible si no hay ningún proveedor de servicios multimedia asociado a la dirección. Consulte **ITTerminalEvent en** la sección Interfaz MSP para obtener más información sobre esta interfaz.

 

 



