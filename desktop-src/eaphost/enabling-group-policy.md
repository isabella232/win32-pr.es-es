---
title: Habilitar directiva de grupo
description: Obtenga información acerca de cómo configurar el suplicante habilitando la Directiva de grupo. Vea Consideraciones para suplicantes y ver recursos adicionales disponibles.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b57e736bf078068156f6aff10d294621749a2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421432"
---
# <a name="enabling-group-policy"></a>Habilitar directiva de grupo

En este tema se explica cómo configurar el suplicante habilitando la Directiva de grupo. Los suplicantes de EAPHost pueden participar en la Directiva de grupo para permitir que un administrador de red configure de forma centralizada sus equipos de red.

El método y el mecanismo precisos que elige el solicitante para participar en la Directiva de grupo es el solicitante. Entre los ejemplos de mecanismos para la participación de directivas de grupo se incluyen extensiones de cliente/servidor, plantilla administrativa, etc.

## <a name="considerations-when-enabling-group-policy"></a>Consideraciones al habilitar directiva de grupo

Estas son las consideraciones para los suplicantes con respecto a la Directiva de grupo y EAP.

1.  La configuración de EAP siempre se debe almacenar como XML siempre que sea posible y no en formato binario. La Directiva de grupo se puede aplicar a cualquier equipo del dominio, y no se garantiza que los datos de usuario y la configuración del método EAP sean portátiles entre las arquitecturas de procesador de 32 bits y 64 bits. XML resuelve los problemas de los límites de la arquitectura del procesador, ya que el suplicante convierte localmente el XML independiente de la arquitectura del procesador en la representación binaria de la configuración en el momento de la autenticación.

    Para obtener más información, vea los siguientes temas.

    -   [Preguntas frecuentes generales](general-frequently-asked-questions.md)
    -   [Preguntas más frecuentes sobre el método EAP](eap-method-frequently-asked-questions.md).
    -   [**EapHostPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [**EapHostPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  Si se usa una extensión de servidor de directiva de grupo, la extensión llamará a [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) normalmente para determinar los métodos disponibles y para generar la configuración de EAP adecuada para esa Directiva. A continuación, la Directiva se envía a los clientes de red adecuados donde se aplica la Directiva.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la interfaz de usuario del método EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Implementación de la compatibilidad de In-Band NAP con métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementación de la compatibilidad de NAP con métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Transferencia de datos entre el suplicante y los métodos EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Suplicantes de EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




