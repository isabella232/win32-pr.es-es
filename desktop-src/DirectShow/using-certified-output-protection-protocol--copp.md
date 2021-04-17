---
description: Uso del Protocolo de protección de la salida certificada (COPP)
ms.assetid: 23eebe93-416b-48c8-a05f-019e38b9a660
title: Uso del Protocolo de protección de la salida certificada (COPP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76460e335985c2aab7f9047b55d2df05aace0269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678085"
---
# <a name="using-certified-output-protection-protocol-copp"></a>Uso del Protocolo de protección de la salida certificada (COPP)

El protocolo de protección de la salida certificada (COPP) permite a una aplicación proteger una secuencia de vídeo mientras se desplaza desde el adaptador de gráficos al dispositivo de pantalla. Una aplicación puede usar COPP para detectar qué tipo de conector físico está conectado al dispositivo de pantalla y qué tipos de protección de salida están disponibles. Entre los mecanismos de protección se incluyen los siguientes:

-   High-Bandwidth Digital Content Protection (HDCP)
-   Sistema de administración de generación de copias: analógico (CGMS-A)
-   Protección de copia analógica (ACP)

Si el adaptador de gráficos admite uno de estos mecanismos, la aplicación puede usar COPP para establecer el nivel de protección.

COPP define un protocolo que se usa para establecer un canal de comunicaciones seguro con el controlador de gráficos. Usa códigos de autenticación de mensajes (Mac) para comprobar la integridad de los comandos COPP que se pasan entre la aplicación y el controlador de pantalla. La aplicación usa COPP llamando a los métodos de la interfaz [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) del filtro de representador de combinación de vídeo de DIRECTSHOW (VMR-7 o VMR-9).

COPP no define nada sobre las directivas de derechos digitales que se pueden aplicar a contenido multimedia digital. Además, el propio COPP no implementa ningún sistema de protección de salida. El protocolo COPP simplemente proporciona una manera de establecer y consultar los niveles de protección en el adaptador de gráficos mediante los sistemas de protección que proporciona el adaptador.

En esta sección se da por supuesto que está familiarizado con las siguientes tecnologías:

-   DirectShow
-   SDK de Windows Media Format
-   XML
-   Criptografía de clave pública y criptografía simétrica

Los ejemplos de código de esta sección usan CryptoAPI de Microsoft para realizar operaciones criptográficas. Esta sección contiene los siguientes temas:

-   [Información general de COPP](overview-of-copp.md)
-   [Obtención de la cadena de certificados del controlador](obtaining-the-drivers-certificate-chain.md)
-   [Validar la cadena de certificados](validating-the-certificate-chain.md)
-   [Listas de revocación de certificados](certificate-revocation-lists.md)
-   [Importar la clave pública del controlador](importing-the-drivers-public-key.md)
-   [Iniciar una sesión de COPP](initiating-a-copp-session.md)
-   [Envío de solicitudes de estado de COPP](sending-copp-status-requests.md)
-   [Envío de comandos COPP](sending-copp-commands.md)
-   [Prueba de si un controlador de gráficos es compatible con COPP](testing-whether-a-graphics-driver-supports-copp.md)
-   [Referencia de consulta de COPP](copp-query-reference.md)
-   [Referencia de comandos de COPP](copp-command-reference.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el representador de mezcla de vídeo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



