---
description: Envío de comandos COPP
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Envío de comandos COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044756f8bdfe59e44309c158cb0be1dc983143d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677089"
---
# <a name="sending-copp-commands"></a>Envío de comandos COPP

Para enviar un comando de protocolo de protección de la salida (COPP) certificado, rellene una estructura [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) como se indica a continuación:

-   **guidCommandID**. GUID que identifica el comando. Consulte la referencia de comandos de COPP.
-   **dwSequence**. Número de secuencia del comando. Incremente este valor después de cada comando. (Este valor se muestra como **uCommandSeq** en [el inicio de una sesión de COPP](initiating-a-copp-session.md)).
-   **cbSizeData**. Tamaño, en bytes, de los datos necesarios para el comando.
-   **CommandData**. Datos para el comando.

Una vez que haya rellenado los datos, calcule el equipo MAC para el comando:

1.  Calcule la etiqueta OMAC-1 para el bloque de datos que aparece después del miembro **macKDI** de la estructura **AMCOPPCommand** .
2.  Copie este valor en el miembro **macKDI** de la estructura.

Pase ahora la estructura al método [**IAMCertifiedOutputProtection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Protocolo de protección de la salida certificada (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



