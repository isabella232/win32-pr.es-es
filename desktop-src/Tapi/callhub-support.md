---
description: El seguimiento de CallHub es una nueva característica de TAPI versión 3.0.
ms.assetid: 29b6e585-6da8-46a2-a612-f42d0f65f68e
title: Soporte técnico de CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36df37db8c57542a5b504f660070c45423f7694340a4677b8cf7570251b848b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117947659"
---
# <a name="callhub-support"></a>Soporte técnico de CallHub

El seguimiento de CallHub es una nueva característica de TAPI versión 3.0. La funcionalidad callHub se agregó a los elementos de programación tapi 2.1 con la entrega de Windows 2000. Un *CallHub* representa una vista de terceros de una llamada y los identificadores de llamada de TAPI representan la vista de primera parte de una llamada. Con el seguimiento de CallHub, se solicita al proveedor de servicios que siga CallHubs y que le dé información sobre la llamada durante la vigencia de un CallHub. A medida que las nuevas partes se unen y salen de CallHub, el proveedor de servicios debe informar a TAPI.

Un proveedor de servicios no necesita implementar ninguna función nueva para admitir CallHub. Simplemente necesita rellenar el miembro **dwCallID** de la [**estructura LINECALLINFO.**](/windows/win32/api/tapi/ns-tapi-linecallinfo) En TAPI 3, TAPI recopila todas las llamadas con el mismo **dwCallID** y crea un identificador de CallHub que la aplicación puede usar para realizar el seguimiento de la llamada.

 

 
