---
title: Abrir y cerrar una sesión WinSNMP
description: Para abrir una sesión, una aplicación llama a la función SnmpCreateSession.
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e006ffb81f6c2508b3505678b28c3ace8e60c85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076046"
---
# <a name="opening-and-closing-a-winsnmp-session"></a>Abrir y cerrar una sesión WinSNMP

Para abrir una sesión, una aplicación llama a la función [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) . Si la función se completa correctamente, la implementación de Microsoft WinSNMP abre una sesión y la función devuelve un identificador de sesión en forma de un identificador **de \_ sesión HSNMP** . Todas las funciones WinSNMP que devuelven variables de identificador incluyen el identificador de sesión como parámetro de entrada. Esto permite a la implementación utilizar el identificador para administrar de forma eficaz los recursos en el nivel de sesión.

Una aplicación puede tener varias sesiones abiertas al mismo tiempo. Varias sesiones dentro de una aplicación pueden compartir variables de identificador.

Si la implementación no puede abrir una sesión debido a las limitaciones de recursos, devuelve un error de SNMPAPI \_ cuando la aplicación llama a [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession). Si la aplicación llama a la función [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) , devuelve snmpapi \_ error de asignación \_ .

Una llamada a la función [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) permite a la implementación liberar los recursos restantes y cerrar la sesión.

Para obtener más información, vea [objetos de identificador de recursos](resource-handle-objects.md) y [sesiones WinSNMP](winsnmp-sessions.md).

 

 




