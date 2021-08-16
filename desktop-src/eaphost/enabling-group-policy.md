---
title: Habilitar directiva de grupo
description: Aprenda a configurar el suplicante habilitando la directiva de grupo. Consulte consideraciones sobre los suplicantes y vea los recursos disponibles adicionales.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2a388bf8dba155e42d5542c1379f7b0cc34d44579b92809387541d7e20cf65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785004"
---
# <a name="enabling-group-policy"></a>Habilitar directiva de grupo

En este tema se explica cómo configurar el suplicante habilitando la directiva de grupo. Los suplicadores de EAPHost pueden participar en la directiva de grupo para permitir que un administrador de red configure centralmente sus máquinas de red.

El método y el mecanismo precisos por los que el suplicante decide participar en la directiva de grupo está a discreción del suplicante. Algunos ejemplos de mecanismos para la participación de directivas de grupo son las extensiones del lado cliente/servidor, la plantilla administrativa, etc.

## <a name="considerations-when-enabling-group-policy"></a>Consideraciones al habilitar directiva de grupo

Estas son las consideraciones para los suplicadores con respecto a la directiva de grupo y EAP.

1.  La configuración de EAP siempre debe almacenarse como XML siempre que sea posible y no en formato binario. La directiva de grupo se puede aplicar a cualquier máquina del dominio, y no se garantiza que la configuración del método EAP y los datos de usuario sean portátiles entre arquitecturas de procesador de 32 y 64 bits. XML resuelve los problemas de límites de la arquitectura del procesador, ya que el suplicante convierte localmente el XML independiente de la arquitectura del procesador en la representación binaria de la configuración en el momento de la autenticación.

    Para obtener más información, vea los temas siguientes:

    -   [Preguntas generales más frecuentes](general-frequently-asked-questions.md)
    -   [Preguntas más frecuentes sobre el método EAP](eap-method-frequently-asked-questions.md).
    -   [**EapHostPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [**EapHostPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  Si se usa una extensión del lado servidor de directiva de grupo, la extensión llamará a [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) normalmente para determinar los métodos disponibles y generar la configuración de EAP adecuada para esa directiva. A continuación, la directiva se inserta en los clientes de red adecuados donde se aplica la directiva.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del método EAP Interfaz de usuario](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Implementar la compatibilidad In-Band NAP para los métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementación de la compatibilidad de NAP con métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Transferencia de datos entre los métodos supplicant y EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Suplicantes de EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




