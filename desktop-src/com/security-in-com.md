---
title: Seguridad en COM
description: La seguridad en COM se basa en firme en la seguridad proporcionada por los Windows y los mecanismos de seguridad rpc subyacentes.
ms.assetid: c9f6d06c-da24-48ea-908a-2462c33f7ee3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b197a632494545e5a151110ca17f1cf1ae1df7577a897284d1e5d437b74093f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918126"
---
# <a name="security-in-com"></a>Seguridad en COM

La seguridad en COM se basa en firme en la seguridad proporcionada por los Windows y los mecanismos de seguridad rpc subyacentes. La seguridad COM se basa en la autenticación *(el* proceso de comprobar la identidad de un autor de la llamada) y la autorización *(el* proceso de determinar si un autor de la llamada está autorizado para hacer lo que está solicitando). Hay dos tipos principales de seguridad en COM: seguridad *de activación* y seguridad *de llamada.* La seguridad de activación determina si un cliente puede iniciar un servidor. Una vez iniciado un servidor, puede usar la seguridad de llamada para controlar el acceso a los objetos de un servidor.

En este modelo de seguridad, los servidores administran y ayudan a proteger objetos, los clientes obtienen acceso a los objetos a través de servidores y los servidores pueden intentar acceder al mismo tiempo que suplantan al cliente.

El sistema implementa el protocolo de autenticación Kerberos v5 y el paquete de seguridad de Schannel. También incluye características como la suplantación de nivel de delegado, la autenticación mutua, la capacidad de establecer niveles de autenticación para un AppID en el registro y la protección. Con la seguridad COM, puede implementar objetos que pueden realizar operaciones con privilegios sin poner en peligro la seguridad.

Dado que hay una amplia gama de características de seguridad COM disponibles, resulta útil determinar inicialmente qué tipo de seguridad necesita la aplicación. Para la mayoría de las aplicaciones, establecer un nivel de seguridad aceptable puede ser un proceso sin problemas, pero también puede usar la seguridad COM para admitir escenarios de seguridad muy complejos.

Puede establecer el proceso de seguridad en todo el proceso, ya sea mediante Dcomcnfg.exe para establecer el registro o llamando a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Dos interfaces principales, [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) (y las funciones auxiliares asociadas), permiten establecer la seguridad de nivel de llamada en el programa.

Para más información sobre la seguridad COM, consulte los temas siguientes:

-   [Determinar las necesidades de seguridad](determining-your-security-needs.md)
-   [Valores predeterminados de seguridad COM](com-security-defaults.md)
-   [Seguridad de activación](activation-security.md)
-   [Valores de seguridad](security-values.md)
-   [Configuración de la seguridad para aplicaciones COM](setting-security-for-com-applications.md)
-   [Habilitación de la seguridad COM mediante DCOMCNFG](enabling-com-security-using-dcomcnfg.md)
-   [Desactivar la seguridad](turning-off-security.md)
-   [Seguridad del lado servidor](server-side-security.md)
-   [Negociación de negociación de negociación de seguridad](security-blanket-negotiation.md)
-   [COM y paquetes de seguridad](com-and-security-packages.md)
-   [Mejoras de seguridad de DCOM en Windows XP Service Pack 2 y Windows Server 2003 Service Pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
-   [Access Control para COM](access-control-lists-for-com.md)
-   [Moniker de elevación COM](the-com-elevation-moniker.md)

 

 