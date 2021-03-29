---
title: Seguridad en COM
description: La seguridad en COM se basa firmemente en la seguridad proporcionada por Windows y los mecanismos de seguridad RPC subyacentes.
ms.assetid: c9f6d06c-da24-48ea-908a-2462c33f7ee3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5e462317d85f7c445d4d8a5ae0aa4d9d3ee724
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421474"
---
# <a name="security-in-com"></a>Seguridad en COM

La seguridad en COM se basa firmemente en la seguridad proporcionada por Windows y los mecanismos de seguridad RPC subyacentes. La seguridad COM se basa en la *autenticación* (el proceso de comprobación de la identidad de un llamador) y en la *autorización* (el proceso de determinar si un llamador está autorizado para hacer lo que se pide). Hay dos tipos principales de seguridad en COM: *seguridad de activación* y *seguridad de llamadas*. La seguridad de activación determina si un cliente puede iniciar un servidor. Una vez iniciado un servidor, puede usar la seguridad de llamada para controlar el acceso a los objetos de un servidor.

En este modelo de seguridad, los servidores administran y ayudan a proteger los objetos, los clientes obtienen acceso a los objetos a través de servidores y los servidores pueden intentar el acceso durante la suplantación del cliente.

El sistema implementa el protocolo de autenticación de Kerberos V5 y el paquete de seguridad de Schannel. También incluye características como la suplantación de nivel de delegado, la autenticación mutua, la capacidad de establecer los niveles de autenticación para un AppID en el registro y la ocultación. Con la seguridad COM, puede implementar objetos que pueden realizar operaciones con privilegios sin poner en peligro la seguridad.

Dado que hay una amplia gama de características de seguridad COM disponibles, es útil determinar inicialmente qué tipo de seguridad necesita la aplicación. Para la mayoría de las aplicaciones, establecer un nivel aceptable de seguridad puede ser un proceso sin problemas, pero también puede usar la seguridad COM para admitir escenarios de seguridad muy complejos.

Puede establecer processwide de seguridad, ya sea mediante Dcomcnfg.exe para establecer el registro o mediante una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Dos interfaces principales, [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) y [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) (y las funciones auxiliares asociadas), permiten establecer la seguridad de nivel de llamada en el programa.

Para obtener más información acerca de la seguridad COM, vea los temas siguientes:

-   [Determinación de las necesidades de seguridad](determining-your-security-needs.md)
-   [Valores predeterminados de seguridad COM](com-security-defaults.md)
-   [Seguridad de activación](activation-security.md)
-   [Valores de seguridad](security-values.md)
-   [Establecer la seguridad de las aplicaciones COM](setting-security-for-com-applications.md)
-   [Habilitar la seguridad COM mediante DCOMCNFG](enabling-com-security-using-dcomcnfg.md)
-   [Desactivar la seguridad](turning-off-security.md)
-   [Seguridad del lado servidor](server-side-security.md)
-   [Negociación de la capa de seguridad](security-blanket-negotiation.md)
-   [COM y paquetes de seguridad](com-and-security-packages.md)
-   [Mejoras de seguridad de DCOM en Windows XP Service Pack 2 y Windows Server 2003 Service Pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
-   [Access Control listas para COM](access-control-lists-for-com.md)
-   [Moniker de elevación COM](the-com-elevation-moniker.md)

 

 