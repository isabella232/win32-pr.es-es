---
description: Las operaciones de finalización permiten a una aplicación especificar cómo desea controlar una sesión cuando factores como un destino de ocupado impiden la conexión normal.
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: Completar una sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5736b6be452413811f3530f44db280fe4e2a682f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687020"
---
# <a name="complete-a-session"></a>Completar una sesión

Las operaciones de finalización permiten a una aplicación especificar cómo desea controlar una sesión cuando factores como un destino de ocupado impiden la conexión normal.

Las [ \_ constantes LINECALLCOMPLMODE](./linecallcomplmode--constants.md) definen las posibles opciones que podría tener una aplicación, en función de las capacidades del proveedor de servicios.

Puede haber varias solicitudes de finalización de llamada pendientes para una dirección determinada en cualquier momento. Para identificar solicitudes individuales, la implementación devuelve un [identificador de finalización](completion-id-ovr.md). La cancelación de una solicitud de finalización de llamada en curso también utiliza este identificador de finalización de llamada.

**TAPI 2. x:** Vea [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).

**TAPI 3. x:** Vea [**ITBasicCallControl:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::D Ulta**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
