---
description: Las operaciones de finalización permiten a una aplicación especificar cómo quiere controlar una sesión cuando factores como un destino ocupado impiden la conexión normal.
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: Completar una sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5736b6be452413811f3530f44db280fe4e2a682f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361785"
---
# <a name="complete-a-session"></a>Completar una sesión

Las operaciones de finalización permiten a una aplicación especificar cómo quiere controlar una sesión cuando factores como un destino ocupado impiden la conexión normal.

Las [constantes LINECALLCOMPLMODE definen las \_ posibles](./linecallcomplmode--constants.md) opciones que podría tener una aplicación, en función de las funcionalidades del proveedor de servicios.

Es posible que haya varias solicitudes de finalización de llamadas pendientes para una dirección determinada en cualquier momento. Para identificar solicitudes individuales, la implementación devuelve un [identificador de finalización](completion-id-ovr.md). La cancelación de una solicitud de finalización de llamada en curso también usa este identificador de finalización de llamada.

**TAPI 2.x:** Vea [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).

**TAPI 3.x:** Vea [**ITBasicCallControl::Conectar**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
