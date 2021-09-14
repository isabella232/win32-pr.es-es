---
description: La autenticación es el proceso de determinar que los autores de la llamada son realmente&8212; comprobar la autenticidad de una notificación \# de identidad.
ms.assetid: c1b11f58-5bab-45d9-a686-86c95415990e
title: Autenticación de clientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd24edf341fc2033807587b01fd37420d781d5f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073009"
---
# <a name="client-authentication"></a>Autenticación de clientes

La autenticación es el proceso de determinar que los llamadores son realmente quienes dicen ser, comprobando la autenticidad de una notificación de identidad. En general, esto lo pueden hacer el servidor y el cliente, cada uno autenticando el otro. Pero es especialmente importante para una aplicación de servidor que autoriza a los clientes, como con la seguridad basada en roles, a realizar también la autenticación. La autenticación de clientes es un requisito previo para una directiva de autorización significativa. Puede realizar todas las comprobación de roles que quiera, pero si no sabe con certeza que la identidad de cliente que está comprobando es auténtica, la aplicación se basa básicamente en el sistema de honor.

En el caso de las aplicaciones COM+, la autenticación es algo que se puede activar y configurar administrativamente, después de lo cual funciona de forma transparente para la aplicación. Especifique un nivel de autenticación administrativamente mediante la herramienta administrativa Servicios de componentes o las funciones administrativas. Para obtener más información sobre cómo establecer la autenticación, vea Establecer un nivel [de autenticación para](setting-an-authentication-level-for-a-server-application.md) una aplicación de servidor y [Habilitar la autenticación para una aplicación de biblioteca.](enabling-authentication-for-a-library-application.md)

Establecer la autenticación significa cosas diferentes en función de si el tipo de aplicación es una aplicación de servidor o de biblioteca.

## <a name="setting-authentication-for-com-server-applications"></a>Configuración de la autenticación para aplicaciones de servidor COM+

Para una aplicación de servidor COM+, establezca un nivel de autenticación que determine cómo se realizará la autenticación cuando los clientes llamen a componentes dentro de la aplicación. Puede elegir entre varios niveles de autenticación que proporcionan distintos grados de seguridad, desde sin autenticación hasta el cifrado de todos los paquetes y todos los parámetros de llamada de método. Para obtener más información, vea [Establecer un nivel de autenticación para una aplicación de servidor.](setting-an-authentication-level-for-a-server-application.md)

Sin embargo, una mayor seguridad incluye cierto costo de rendimiento, que debe tener en cuenta al configurar la aplicación. COM+ negociará entre el nivel de autenticación especificado por el cliente y el servidor. La forma en que se lleva a cabo esta negociación tiene la ventaja de permitirle controlar la autenticación administrativamente solo desde el lado servidor. Para obtener más información, vea [Negociación del nivel de autenticación.](negotiation-of-authentication-level.md)

> [!Note]  
> Nunca debe especificar un nivel de autenticación mediante programación mediante [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) dentro de una aplicación COM+. COM+ llama **a CoInitializeSecurity** por usted y solo se puede llamar a esta opción una vez por proceso.

 

Los servicios de autenticación subyacentes los proporcionan COM y Microsoft Windows. En un servicio de autenticación, un tercero proporciona un certificado para un usuario, que atestigua la autenticidad de la identidad del usuario. Esta certificación es tan confiable como la autoridad de certificación y, en gran medida del mismo modo que una licencia de conducir o un pasaporte actúa como documento de certificación, depende de la autoridad del emisor. Para obtener información más detallada sobre los servicios de autenticación, [vea Paquetes de seguridad y COM](/windows/desktop/com/com-and-security-packages) en la documentación de COM.

## <a name="setting-authentication-for-com-library-applications"></a>Configuración de la autenticación para aplicaciones de biblioteca COM+

Para una aplicación de biblioteca COM+, habilite o deshabilite la autenticación para determinar si la aplicación estará sujeta a la autenticación realizada por el proceso de hospedaje. Aunque la autenticación de una aplicación de biblioteca COM+ se controla en gran medida mediante el proceso de hospedaje, puede configurar la aplicación de biblioteca para que no participe en la autenticación. Es decir, las llamadas a la aplicación se pueden autenticar o no autenticar y, en el último caso, la "autenticación" de los clientes siempre se realiza correctamente. Para obtener más información, vea [Habilitar la autenticación para una aplicación de biblioteca.](enabling-authentication-for-a-library-application.md)

Además, es posible que desee o se le requiera que autentique el cliente en la base de datos o en alguna aplicación de nivel inferior, ya que es posible que la autenticación de clientes en la aplicación COM+ por sí sola no sea suficiente. Si este es el caso, debe suplantar al cliente para que la identidad del cliente se propague de nivel inferior. Para obtener información detallada sobre la suplantación, vea [Suplantación y delegación de cliente.](client-impersonation-and-delegation.md) Para obtener una explicación de los problemas implicados en la decisión de si se debe realizar la autenticación en el nivel de datos, consulte [Seguridad de aplicaciones de niveles múltiples.](multi-tier-application-security.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Seguridad de la aplicación de biblioteca](library-application-security.md)
</dt> <dt>

[Seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> <dt>

[Administración de seguridad basada en roles](role-based-security-administration.md)
</dt> <dt>

[Uso de la directiva de restricción de software en COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
