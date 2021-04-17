---
description: Describe los errores del proveedor SNMP de WMI de 1101 a 1110.
ms.assetid: ffb3da80-0ffa-4f05-a35e-c51dba38a7fe
ms.tgt_platform: multiple
title: Errores de 1101 a 1110
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ee87e1e0288bf58dea8df2d0f29fc2634bccca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717201"
---
# <a name="errors-1101-through-1110"></a>Errores de 1101 a 1110

Describe los errores del proveedor SNMP de WMI de 1101 a 1110.

[Error irrecuperable 1101](#fatal-error-1101)

## <a name="fatal-error-1101"></a>Error irrecuperable 1101

<dl> <dt>

<span id="_1101__Fatal_____fileName__line____The_length_of_the_range_is_too_long_for_the_compiler__Does_not_fit_into_4_bytes__"></span><span id="_1101__fatal_____filename__line____the_length_of_the_range_is_too_long_for_the_compiler__does_not_fit_into_4_bytes__"></span><span id="_1101__FATAL_____FILENAME__LINE____THE_LENGTH_OF_THE_RANGE_IS_TOO_LONG_FOR_THE_COMPILER__DOES_NOT_FIT_INTO_4_BYTES__"></span>**<1101,> grave: " <fileName><> de línea \# : la longitud del intervalo es demasiado larga para el compilador (no cabe en 4 bytes)"**
</dt> <dd>

Error semántico del módulo en la especificación de intervalo o tamaño, específico de SNMPv1 o SNMPv2C. El tamaño de un conjunto de intervalos debe ser inferior a 2 ³ ². El tamaño de un conjunto de intervalos se define como la diferencia entre el valor más grande y el valor más pequeño del conjunto.

</dd> </dl>

 

 



