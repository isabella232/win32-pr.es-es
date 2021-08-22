---
title: Cadenas de estilo C
description: Una aplicación WinSNMP puede usar cadenas de estilo C terminadas en NULL para convertir objetos de identificador de entidad y objeto (OID) a y desde sus representaciones de cadena.
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6449514d4c08baae638d950a42f7f553e0037efe6bdc45b8045dbd315c1a2c65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009762"
---
# <a name="c-style-strings"></a>Cadenas de estilo C

Una aplicación WinSNMP puede usar cadenas de estilo C terminadas en **NULL** para convertir objetos de identificador de entidad y objeto (OID) a y desde sus representaciones de cadena.

Las funciones winSNMP que manipulan cadenas de estilo C incluyen [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)y [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr). Dado que [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) y [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) devuelven un puntero a una variable de cadena de  estilo C, la aplicación WinSNMP debe pasar un valor adecuado en el parámetro size cuando realiza llamadas a estas funciones. Para obtener más información, vea las páginas de referencia de estas funciones.

> [!Note]  
> El *parámetro* de contexto de las [**funciones SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) y [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) debe ser una estructura de cadena de octeto, es decir, una estructura [**smiOCTETS.**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) El *parámetro context* no puede ser una cadena de estilo C. La cadena contenida en una **estructura smiOCTETS** no requiere un byte de terminación **NULL.**

 

 

 




