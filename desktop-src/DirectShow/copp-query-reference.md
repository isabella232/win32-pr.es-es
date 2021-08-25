---
description: Referencia de consulta COPP
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: Referencia de consulta COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59d36cde152600faaa1dd567faac916bfa8281e2b2edb9464074fe34a58d5011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909665"
---
# <a name="copp-query-reference"></a>Referencia de consulta COPP

En esta sección se describen las consultas de estado compatibles con el Protocolo de protección de salida certificado (COPP). Para cada consulta, se muestra el GUID que define la consulta, junto con los datos de entrada y los datos devueltos.



| Consultar                   | GUID                                     |
|-------------------------|------------------------------------------|
| Datos de bus                | **DXVA \_ COPPQueryBusData**               |
| Tipo de conector          | **DXVA \_ COPPQueryConnectorType**         |
| Mostrar datos            | **DXVA \_ COPPQueryDisplayData**           |
| Datos de clave de HDCP           | **DXVA \_ COPPQueryHDCPKeyData**           |
| Nivel de protección global | **DXVA \_ COPPQueryGlobalProtectionLevel** |
| Nivel de protección local  | **DXVA \_ COPPQueryLocalProtectionLevel**  |
| Tipo de protección         | **DXVA \_ COPPQueryProtectionType**        |
| Signaling               | **DXVA \_ COPPQuerySignaling**             |



 

Consulta de datos de bus

Devuelve el tipo de bus de E/S utilizado por el adaptador de gráficos.

-   **GUID:** DXVA \_ COPPQueryBusData
-   **Datos de entrada:** Ninguno.
-   **Devolver datos:** devuelve una [**estructura \_ COPPStatusData de DXVA.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) El tipo de bus se devuelve en el **miembro dwData** como una marca de la [**enumeración COPP \_ BusType.**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype)

Consulta de tipo de conector

Devuelve el tipo de conector físico.

-   **GUID:** DXVA \_ COPPQueryConnectorType
-   **Datos de entrada:** Ninguno.
-   **Devolver datos:** devuelve una [**estructura \_ COPPStatusData de DXVA.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) El tipo de conector se devuelve en el **miembro dwData** como una marca de la [**enumeración COPP \_ ConnectorType.**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype)

Mostrar consulta de datos

Devuelve una descripción de la señal de vídeo que se transmite a través del conector.

La señal de vídeo que se transmite a través del conector no tiene necesariamente el mismo formato que el modo de visualización de escritorio. Por ejemplo, el modo de visualización de escritorio podría ser de 1024 x 768 píxeles a 85 Hz, mientras que el conector podría ser un conector S-Video que transmite una señal de vídeo a 720 x 480 píxeles, 60/1,01 Hz entrelazada. En ese caso, el controlador devolvería la resolución de la señal S-Video, no la resolución de escritorio.

-   **GUID:** DXVA \_ COPPQueryDisplayData
-   **Datos de entrada:** Ninguno.
-   **Devolver datos:** devuelve una [**estructura \_ DXVA COPPStatusDisplayData.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata)

Consulta de datos de claves de HDCP

Devuelve el vector de selección de claves HDCP (B-KSV) del dispositivo.

KSV es un identificador proporcionado al fabricante del dispositivo y se usa en el proceso de autenticación y configuración de HDCP. La aplicación debe comprobar este valor en la lista de CSV revocados. El mecanismo para obtener la lista de revocación de KSV está fuera del ámbito del protocolo COPP. Para más información, consulte la especificación de HDCP.

Esta consulta también determina si el dispositivo HDCP conectado es un monitor o un repetidor HDCP. La aplicación no debe reproducir contenido protegido si el dispositivo HDCP es un repetidor HDCP, ya que no son compatibles con COPP.

-   **GUID:** DXVA \_ COPPQueryHDCPKeyData
-   **Datos de entrada:** Ninguno.
-   **Devolver datos:** devuelve una [**estructura \_ DXVA COPPStatusHDCPKeyData.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata)

Consulta de nivel de protección global

Devuelve el nivel de protección global para un mecanismo de protección especificado.

El nivel de protección global es el nivel de protección que se aplica actualmente en el conector, independientemente de cómo se indique al controlador de gráficos que aplique la protección. Por ejemplo, una aplicación puede establecer el nivel de protección ACP llamando a la **función ChangeDisplaySettingsEx.** En ese caso, el nivel de protección global reflejaría esta configuración, aunque no se solicitó a través de COPP.

-   **GUID:** DXVA \_ COPPQueryGlobalProtectionLevel
-   **Datos de** entrada: mecanismo de protección que se consulta, especificado como un entero de 32 bits. Vea [Marcas de tipo de protección COPP](copp-protection-type-flags.md).
-   **Devolver datos:** devuelve una [**estructura \_ COPPStatusData de DXVA.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) El nivel de protección actual se devuelve en el **miembro dwData.** El significado de este valor depende del mecanismo de protección que se consulta. Para cada mecanismo de protección, el valor del **miembro dwData** es una marca de una enumeración diferente, como se muestra en la tabla siguiente.

    | Mecanismo de protección | Enumeración                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**Nivel de protección de COPP \_ ACP \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**Nivel de protección \_ de COPP CGMSA \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | Hdcp                 | [**Nivel de protección \_ de HDCP \_ de \_ COPP**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Consulta de nivel de protección local

Devuelve el nivel de protección local para un mecanismo de protección especificado.

El nivel de protección local es el nivel de protección que se solicitó a través de la sesión actual de COPP. El controlador podría establecer un nivel de protección superior.

-   **GUID:** DXVA \_ COPPQueryLocalProtectionLevel
-   **Datos de** entrada: mecanismo de protección que se consulta, como un entero de 32 bits. Vea [Marcas de tipo de protección COPP](copp-protection-type-flags.md).
-   **Devolver datos:** devuelve una [**estructura \_ COPPStatusData de DXVA.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) El nivel de protección actual se devuelve en el **miembro dwData.** El significado de este valor depende del mecanismo de protección que se consulta. Para cada mecanismo de protección, el valor del **miembro dwData** es una marca de una enumeración diferente, como se muestra en la tabla siguiente.

    | Mecanismo de protección | Enumeración                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**Nivel de protección de COPP \_ ACP \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**Nivel de protección \_ de COPP CGMSA \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | Hdcp                 | [**Nivel de protección \_ de HDCP \_ de \_ COPP**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Consulta de tipo de protección

Devuelve los mecanismos de protección que están disponibles para el conector.

-   **GUID:** DXVA \_ COPPQueryProtectionType
-   **Datos de entrada:** Ninguno.
-   **Devolver datos:** devuelve una [**estructura \_ COPPStatusData de DXVA.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) Los mecanismos de protección se devuelven en el **miembro dwData** como una combinación de cero o más marcas. Vea [Marcas de tipo de protección COPP](copp-protection-type-flags.md). Si hay más de un mecanismo de protección disponible, las marcas se combinan con un OR bit a **bit.**

Consulta de señalización

Devuelve una lista de todos los estándares de protección admitidos por el controlador, el estándar que está activo actualmente y la relación de aspecto actual u otros datos de señalización.

-   **GUID:** DXVA \_ COPPQuerySignaling
-   **Datos de entrada:** Ninguno.
-   **Devolver datos:** devuelve una [**estructura \_ COPPStatusSignalingCmdData de DXVA.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del protocolo de protección de salida certificado (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



