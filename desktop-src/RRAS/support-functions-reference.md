---
title: Referencia de funciones de soporte técnico
description: El administrador de enrutadores proporciona las siguientes funciones a los protocolos de enrutamiento.
ms.assetid: 4e88c9fe-f6ec-4f9c-88b1-8726e10d0f6d
keywords:
- Interface de protocolo de enrutamiento RRAS, funciones de compatibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fa2af1b38e88e9f3b7a55e8026ad42f4b1d0cff26de3798fb04621a1288ad9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073715"
---
# <a name="support-functions-reference"></a>Referencia de funciones de soporte técnico

El administrador de enrutadores proporciona las siguientes funciones a los protocolos de enrutamiento. Cuando el administrador de enrutadores llama a la función [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) (implementada por el protocolo de enrutamiento), el administrador de enrutadores pasa al protocolo de enrutamiento una estructura [**SUPPORT \_ FUNCTIONS**](/windows/desktop/api/Routprot/ns-routprot-support_functions_50) que contiene punteros a estas funciones:

[**DemandDialRequest**](/previous-versions/windows/desktop/legacy/aa373924(v=vs.85))

[**MIBEntryCreate**](/previous-versions/windows/desktop/legacy/aa374538(v=vs.85))

[**MIBEntryDelete**](/previous-versions/windows/desktop/legacy/aa374539(v=vs.85))

[**MIBEntryGet**](/previous-versions/windows/desktop/legacy/aa374540(v=vs.85))

[**MIBEntryGetFirst**](/previous-versions/windows/desktop/legacy/aa374541(v=vs.85))

[**MIBEntryGetNext**](/previous-versions/windows/desktop/legacy/aa374542(v=vs.85))

[**MIBEntrySet**](/previous-versions/windows/desktop/legacy/aa374543(v=vs.85))

[**SetInterfaceReceiveType**](/previous-versions/windows/desktop/legacy/aa382181(v=vs.85))

[**ValidateRoute**](/previous-versions/windows/desktop/legacy/aa382342(v=vs.85))

 

 