---
title: Cadenas de estilo C
description: Una aplicación WinSNMP puede usar cadenas de estilo C terminadas en NULL para convertir objetos de entidad y de identificador de objeto (OID) a y desde sus representaciones de cadena.
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878398b6d8691982aa90b9f1376a38214030e52e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903009"
---
# <a name="c-style-strings"></a>Cadenas de estilo C

Una aplicación WinSNMP puede usar cadenas de estilo C terminadas en **null** para convertir objetos de entidad y de identificador de objeto (OID) a y desde sus representaciones de cadena.

Entre las funciones WinSNMP que manipulan cadenas de estilo C se incluyen [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)y [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr). Dado que [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) y [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) devuelven un puntero a una variable de cadena de estilo C, la aplicación WinSNMP debe pasar un valor adecuado en el parámetro *size* cuando realiza llamadas a estas funciones. Para obtener más información, vea las páginas de referencia de estas funciones.

> [!Note]  
> El parámetro de *contexto* de las funciones [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) y [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) debe ser una estructura de cadena de octetos, es decir, una estructura [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) . El parámetro de *contexto* no puede ser una cadena de estilo C. La cadena contenida en una estructura **smiOCTETS** no requiere un byte de terminación **null**.

 

 

 




