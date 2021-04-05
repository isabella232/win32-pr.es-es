---
description: La autenticación es el proceso de determinar que los llamadores son realmente quienes dicen que están&\# 8212; comprobar la autenticidad de una demanda de identidad.
ms.assetid: c1b11f58-5bab-45d9-a686-86c95415990e
title: Autenticación de clientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd24edf341fc2033807587b01fd37420d781d5f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000680"
---
# <a name="client-authentication"></a>Autenticación de clientes

La autenticación es el proceso de determinar que los llamadores son realmente quienes dicen que son: comprobar la autenticidad de una demanda de identidad. En general, esto se puede hacer tanto en el servidor como en el cliente, y cada uno de ellos autentica el otro. Pero es especialmente importante para una aplicación de servidor que está autorizando a los clientes, como con la seguridad basada en roles, realizar también la autenticación. La autenticación de clientes es un requisito previo para una directiva de autorización significativa. Puede realizar todas las comprobaciones de roles que desee, pero si no sabe con certeza que la identidad del cliente que está comprobando es auténtica, la aplicación se basa básicamente en el sistema de honor.

En el caso de las aplicaciones COM+, la autenticación es algo que se puede activar y configurar administrativamente, después de que funciona de forma transparente en la aplicación. Especifique un nivel de autenticación administrativamente mediante la herramienta administrativa Servicios de componentes o las funciones administrativas. Para obtener más información sobre la configuración de la autenticación, consulte [configuración de un nivel de autenticación para una aplicación de servidor](setting-an-authentication-level-for-a-server-application.md) y [habilitación de la autenticación para una aplicación de biblioteca](enabling-authentication-for-a-library-application.md).

La configuración de la autenticación implica distintas cosas dependiendo de si el tipo de aplicación es una aplicación de biblioteca o servidor.

## <a name="setting-authentication-for-com-server-applications"></a>Establecer la autenticación para las aplicaciones de servidor COM+

En el caso de una aplicación de servidor COM+, se establece un nivel de autenticación que determina cómo se realizará la autenticación cuando los clientes llamen a los componentes de la aplicación. Puede elegir entre varios niveles de autenticación que proporcionan distintos grados de seguridad, que van desde sin autenticación hasta el cifrado de todos los paquetes y todos los parámetros de la llamada al método. Para obtener más información, consulte [configuración de un nivel de autenticación para una aplicación de servidor](setting-an-authentication-level-for-a-server-application.md).

Sin embargo, una mayor seguridad incluye algún costo de rendimiento, que debe tener en cuenta al configurar la aplicación. COM+ negociará entre el nivel de autenticación especificado por el cliente y el servidor. La manera en que se lleva a cabo esta negociación tiene la ventaja de que permite controlar de forma administrativa la autenticación desde el servidor solo. Para obtener más información, consulte [negociación del nivel de autenticación](negotiation-of-authentication-level.md).

> [!Note]  
> Nunca debe especificar un nivel de autenticación mediante programación con [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) en una aplicación com+. COM+ llama a **CoInitializeSecurity** automáticamente y solo se puede llamar una vez por cada proceso.

 

Los servicios de autenticación subyacentes se proporcionan mediante COM y Microsoft Windows. En un servicio de autenticación, un tercero proporciona un certificado para un usuario, que da fe de la autenticidad de la identidad del usuario. Esta certificación es tan creíble como la autoridad de certificación y, de forma muy similar a la licencia de un controlador o a una cuenta de Passport sirve como documento de certificación, depende de la autoridad del emisor. Para obtener información más detallada sobre los servicios de autenticación, vea [com and Security Packages](/windows/desktop/com/com-and-security-packages) en la documentación de com.

## <a name="setting-authentication-for-com-library-applications"></a>Establecer la autenticación para las aplicaciones de biblioteca COM+

En el caso de una aplicación de biblioteca COM+, habilite o deshabilite la autenticación de para determinar si la aplicación estará sujeta a la autenticación realizada por el proceso de hospedaje. Aunque el proceso de hospedaje controla en gran medida la autenticación de una aplicación de biblioteca COM+, puede configurar la aplicación de biblioteca para que no participe en la autenticación. Es decir, las llamadas a la aplicación se pueden autenticar o no autenticar y, en el segundo caso, la "autenticación" de los clientes siempre se realiza correctamente. Para obtener más información, consulte [habilitación de la autenticación para una aplicación de biblioteca](enabling-authentication-for-a-library-application.md).

Además, es posible que desee o que tenga que autenticar al cliente en la base de datos o en alguna aplicación de nivel inferior; la autenticación de clientes en la aplicación COM+ no es suficiente. Si es así, debe suplantar al cliente para que la identidad del cliente se propague hacia abajo. Para obtener información detallada acerca de la suplantación, consulte [suplantación y delegación del cliente](client-impersonation-and-delegation.md). Para obtener una explicación de los problemas implicados en la decisión de decidir si la autenticación se realiza en la capa de datos, vea [seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Seguridad de aplicaciones de biblioteca](library-application-security.md)
</dt> <dt>

[Seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> <dt>

[Administración de la seguridad basada en roles](role-based-security-administration.md)
</dt> <dt>

[Usar la Directiva de restricción de software en COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
