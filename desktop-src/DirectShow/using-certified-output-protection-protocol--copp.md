---
description: Uso del protocolo de protección de salida certificado (COPP)
ms.assetid: 23eebe93-416b-48c8-a05f-019e38b9a660
title: Uso del protocolo de protección de salida certificado (COPP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c97ee1daf62f2d1fb42cdb63e02ae31991c168cfeaaf4437c2e77643fc6cbd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086775"
---
# <a name="using-certified-output-protection-protocol-copp"></a>Uso del protocolo de protección de salida certificado (COPP)

El Protocolo de protección de salida certificado (COPP) permite a una aplicación proteger una secuencia de vídeo mientras viaja desde el adaptador de gráficos al dispositivo de pantalla. Una aplicación puede usar COPP para detectar qué tipo de conector físico está conectado al dispositivo de visualización y qué tipos de protección de salida están disponibles. Entre los mecanismos de protección se incluyen los siguientes:

-   High-Bandwidth Digital Content Protection (HDCP)
-   Sistema de administración de generación de copias: análogo (CGMS-A)
-   Protección de copia análoga (ACP)

Si el adaptador de gráficos admite uno de estos mecanismos, la aplicación puede usar COPP para establecer el nivel de protección.

COPP define un protocolo que se usa para establecer un canal de comunicaciones seguro con el controlador de gráficos. Usa códigos de autenticación de mensajes (MAC) para comprobar la integridad de los comandos COPP que se pasan entre la aplicación y el controlador de pantalla. La aplicación usa COPP llamando a métodos en la interfaz [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) del filtro de representador de mezcla de vídeo de DirectShow (VMR-7 o VMR-9).

COPP no define nada sobre las directivas de derechos digitales que podrían aplicarse al contenido multimedia digital. Además, copp no implementa ningún sistema de protección de salida. El protocolo COPP simplemente proporciona una manera de establecer y consultar los niveles de protección en el adaptador de gráficos, mediante los sistemas de protección proporcionados por el adaptador.

En esta sección se da por supuesto que está familiarizado con las siguientes tecnologías:

-   DirectShow
-   Windows SDK de formato multimedia
-   XML
-   Criptografía de clave pública y criptografía simétrica

Los ejemplos de código de esta sección usan CryptoAPI de Microsoft para realizar operaciones criptográficas. Esta sección contiene los siguientes temas:

-   [Información general de COPP](overview-of-copp.md)
-   [Obtener la cadena de certificados del controlador](obtaining-the-drivers-certificate-chain.md)
-   [Validación de la cadena de certificados](validating-the-certificate-chain.md)
-   [Listas de revocación de certificados](certificate-revocation-lists.md)
-   [Importar la clave pública del controlador](importing-the-drivers-public-key.md)
-   [Inicio de una sesión copp](initiating-a-copp-session.md)
-   [Envío de solicitudes de estado de COPP](sending-copp-status-requests.md)
-   [Envío de comandos COPP](sending-copp-commands.md)
-   [Prueba de si un controlador de gráficos admite COPP](testing-whether-a-graphics-driver-supports-copp.md)
-   [Referencia de consulta COPP](copp-query-reference.md)
-   [Referencia de comandos copp](copp-command-reference.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del representador de mezcla de vídeo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



