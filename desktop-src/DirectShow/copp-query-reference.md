---
description: Referencia de consulta de COPP
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: Referencia de consulta de COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41de36f3cdcc37a38e2ebc53caa7b6b37c204d9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080069"
---
# <a name="copp-query-reference"></a>Referencia de consulta de COPP

En esta sección se describen las consultas de estado admitidas por el protocolo de protección de la salida certificada (COPP). Para cada consulta, se muestra el GUID que define la consulta, junto con los datos de entrada y los datos devueltos.



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

Devuelve el tipo de bus de e/s utilizado por el adaptador de gráficos.

-   **GUID**: DXVA \_ COPPQueryBusData
-   **Datos de entrada**: ninguno.
-   **Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . El tipo de bus se devuelve en el miembro **dwData** como una marca de la enumeración [**COPP \_ BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) .

Consulta de tipo de conector

Devuelve el tipo de conector físico.

-   **GUID**: DXVA \_ COPPQueryConnectorType
-   **Datos de entrada**: ninguno.
-   **Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . El tipo de conector se devuelve en el miembro **dwData** como una marca de la enumeración [**COPP \_ ConnectorType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) .

Consulta de visualización de datos

Devuelve una descripción de la señal de vídeo que se transmite a través del conector.

La señal de vídeo que se transmite a través del conector no tiene necesariamente el mismo formato que el modo de presentación del escritorio. Por ejemplo, el modo de presentación del escritorio puede tener 1024x768 píxeles a 85 Hz, mientras que el conector puede ser un conector de S-vídeo que transmite una señal de vídeo a 720 x 480 píxeles, 60/1.01 Hz entrelazada. En ese caso, el controlador devolvería la resolución de la señal S-video, no la resolución del escritorio.

-   **GUID**: DXVA \_ COPPQueryDisplayData
-   **Datos de entrada**: ninguno.
-   **Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusDisplayData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) .

Consulta de datos de clave de HDCP

Devuelve el vector de selección de clave de HDCP del dispositivo (B-KSV).

KSV es un identificador proporcionado al fabricante del dispositivo y se usa en el proceso de autenticación y configuración de HDCP. La aplicación debe comprobar este valor con la lista de KSVs revocados. El mecanismo para obtener la lista de revocación de KSV está fuera del ámbito del protocolo COPP. Para obtener más información, consulte la especificación de HDCP.

Esta consulta también determina si el dispositivo HDCP conectado es un monitor o un repetidor de HDCP. La aplicación no debe reproducir contenido protegido si el dispositivo HDCP es un repetidor de HDCP, ya que estos no son compatibles con COPP.

-   **GUID**: DXVA \_ COPPQueryHDCPKeyData
-   **Datos de entrada**: ninguno.
-   **Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusHDCPKeyData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) .

Consulta de nivel de protección global

Devuelve el nivel de protección global para un mecanismo de protección especificado.

El nivel de protección global es el nivel de protección que se está aplicando actualmente en el conector, independientemente de cómo se haya indicado al controlador de gráficos que aplique la protección. Por ejemplo, una aplicación puede establecer el nivel de protección ACP llamando a la función **ChangeDisplaySettingsEx** . En ese caso, el nivel de protección global reflejaría esta configuración, aunque no se solicitó a través de COPP.

-   **GUID**: DXVA \_ COPPQueryGlobalProtectionLevel
-   **Datos de entrada**: mecanismo de protección que se va a consultar, especificado como un entero de 32 bits. Consulte [marcas de tipo de protección COPP](copp-protection-type-flags.md).
-   **Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . El nivel de protección actual se devuelve en el miembro **dwData** . El significado de este valor depende del mecanismo de protección que se consulta. Para cada mecanismo de protección, el valor del miembro **dwData** es una marca de una enumeración diferente, como se muestra en la tabla siguiente.

    | Mecanismo de protección | Enumeración                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**Nivel de protección de los ACP de COPP \_ \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**Nivel de protección de COPP \_ CGMSA \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | HDCP                 | [**\_Nivel de \_ protección de HDCP de COPP \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Consulta de nivel de protección local

Devuelve el nivel de protección local para un mecanismo de protección especificado.

El nivel de protección local es el nivel de protección que se solicitó a través de la sesión de COPP actual. Es posible que el controlador establezca un nivel de protección superior.

-   **GUID**: DXVA \_ COPPQueryLocalProtectionLevel
-   **Datos de entrada**: mecanismo de protección que se va a consultar, como un entero de 32 bits. Consulte [marcas de tipo de protección COPP](copp-protection-type-flags.md).
-   **Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . El nivel de protección actual se devuelve en el miembro **dwData** . El significado de este valor depende del mecanismo de protección que se consulta. Para cada mecanismo de protección, el valor del miembro **dwData** es una marca de una enumeración diferente, como se muestra en la tabla siguiente.

    | Mecanismo de protección | Enumeración                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**Nivel de protección de los ACP de COPP \_ \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**Nivel de protección de COPP \_ CGMSA \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | HDCP                 | [**\_Nivel de \_ protección de HDCP de COPP \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Consulta de tipo de protección

Devuelve los mecanismos de protección que están disponibles para el conector.

-   **GUID**: DXVA \_ COPPQueryProtectionType
-   **Datos de entrada**: ninguno.
-   **Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . Los mecanismos de protección se devuelven en el miembro **dwData** como una combinación de cero o más marcadores. Consulte [marcas de tipo de protección COPP](copp-protection-type-flags.md). Si hay más de un mecanismo de protección disponible, las marcas se combinan con una **operación OR** bit a bit.

Consulta de señalización

Devuelve una lista de todos los estándares de protección admitidos por el controlador, el estándar que está activo actualmente y la relación de aspecto actual u otros datos de señalización.

-   **GUID**: DXVA \_ COPPQuerySignaling
-   **Datos de entrada**: ninguno.
-   **Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Protocolo de protección de la salida certificada (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



