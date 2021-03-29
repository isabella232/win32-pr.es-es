---
title: Compatibilidad con cadenas de direcciones IPX en WinSNMP
description: WinSNMP 2,0 formaliza el uso de cadenas de direcciones IPX.
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc33c3ff3b589f9614b139260cef993e232f4343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772847"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a>Compatibilidad con cadenas de direcciones IPX en WinSNMP

WinSNMP 2,0 formaliza el uso de cadenas de direcciones IPX. Si especifica una cadena de dirección IPX como parámetro de entrada para la función [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) , debe dar formato a la cadena mediante los siguientes estándares:

-   Un número de red que consta de ocho dígitos hexadecimales (relleno de cero si es necesario).
-   Un separador (":", "." o "–")
-   Un número de nodo que consta de 12 dígitos hexadecimales (relleno de cero si es necesario).

Por ejemplo, 00000001:00081A0D01C2 o 00000001.00081 a0d01c2. Los dígitos hexadecimales pueden estar en mayúsculas o minúsculas.

Este es el formato que usa la función [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) para devolver una cadena de dirección IPX. La cadena se devuelve cuando una aplicación que funciona en uno de los modos sin \_ traducir snmpapi llama a la función **SnmpEntityToStr** . También se puede devolver la cadena cuando la aplicación funciona en el \_ modo traducido de snmpapi y no hay ningún nombre descriptivo disponible para la entidad.

 

 




