---
title: Apertura y cierre de una sesión winSNMP
description: Para abrir una sesión, una aplicación llama a la función SnmpCreateSession.
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41871c9adc2f7fcefc04b5816b29685ad6b1516a6238c1855ed41e878d5b2736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009203"
---
# <a name="opening-and-closing-a-winsnmp-session"></a>Apertura y cierre de una sesión winSNMP

Para abrir una sesión, una aplicación llama a la [**función SnmpCreateSession.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) Si la función se completa correctamente, la implementación de Microsoft WinSNMP abre una sesión y la función devuelve un identificador de sesión en forma de identificador session de **HSNMP. \_** Todas las funciones de WinSNMP que devuelven variables de identificador incluyen el identificador de sesión como parámetro de entrada. Esto permite que la implementación use el identificador para administrar eficazmente los recursos en el nivel de sesión.

Una aplicación puede tener varias sesiones abiertas a la vez. Varias sesiones dentro de una aplicación pueden compartir variables de identificador.

Si la implementación no puede abrir una sesión debido a limitaciones de recursos, devuelve SNMPAPI FAILURE cuando la aplicación llama a \_ [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession). Si la aplicación llama a la [**función SnmpGetLastError,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) devuelve SNMPAPI \_ ALLOC \_ ERROR.

Una llamada a la [**función SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) permite a la implementación liberar los recursos restantes y cerrar la sesión.

Para obtener más información, vea [Objetos de identificador de recursos](resource-handle-objects.md) y Sesiones de [WinSNMP.](winsnmp-sessions.md)

 

 




