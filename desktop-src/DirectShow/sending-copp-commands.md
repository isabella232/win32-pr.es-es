---
description: Envío de comandos COPP
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Envío de comandos COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66a6ad66abe7e6c4a596446b147fe5943c5460b4ef540dbc5e5a3dfad4bdc7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078885"
---
# <a name="sending-copp-commands"></a>Envío de comandos COPP

Para enviar un comando del Protocolo de protección de salida certificado (COPP), rellene una [**estructura AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) como se muestra a continuación:

-   **guidCommandID**. GUID que identifica el comando. Consulte la referencia de comandos copp.
-   **dwSequence**. Número de secuencia del comando. Incremente este valor después de cada comando. (Este valor se muestra como **uCommandSeq en** [Iniciar una sesión copp).](initiating-a-copp-session.md)
-   **cbSizeData**. Tamaño, en bytes, de los datos necesarios para el comando.
-   **CommandData**. Datos del comando.

Una vez que haya rellenado estos datos, calcule el MAC para el comando:

1.  Calcule la etiqueta OMAC-1 para el bloque de datos que aparece después del **miembro macKDI** de la **estructura AMCOPPCommand.**
2.  Copie este valor en el **miembro macKDI** de la estructura .

Ahora pase la estructura al [**método IAMCertifiedOutputProtection::P rotectionCommand.**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del protocolo de protección de salida certificado (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



