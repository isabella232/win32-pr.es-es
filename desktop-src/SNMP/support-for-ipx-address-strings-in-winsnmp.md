---
title: Compatibilidad con cadenas de direcciones IPX en WinSNMP
description: WinSNMP 2.0 formaliza el uso de cadenas de direcciones IPX.
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: debd25897c32515b880ff82f691aa0421af6358ae72c7e49de3408d55bcbd609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886085"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a>Compatibilidad con cadenas de direcciones IPX en WinSNMP

WinSNMP 2.0 formaliza el uso de cadenas de direcciones IPX. Si especifica una cadena de dirección IPX como parámetro de entrada para la función [**SnmpStrToEntity,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) debe dar formato a la cadena con los siguientes estándares:

-   Número de red que consta de ocho dígitos hexadecimales (relleno cero si es necesario)
-   Separador (":", "." o " – ")
-   Número de nodo que consta de 12 dígitos hexadecimales (relleno cero si es necesario)

Por ejemplo, 00000001:00081A0D01C2 o 00000001.00081a0d01c2. Los dígitos hexadecimales pueden estar en mayúsculas o minúsculas.

Este es el formato que [**usa la función SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) para devolver una cadena de dirección IPX. La cadena se devuelve cuando una aplicación que funciona en uno de los modos \_ SNMPAPI UNTRANSLATED llama a la **función SnmpEntityToStr.** La cadena también se puede devolver cuando la aplicación funciona en modo SNMPAPI TRANSLATED y no hay ningún nombre descriptivo \_ disponible para la entidad.

 

 




