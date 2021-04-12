---
description: Proveedores de credenciales en Windows 10
ms.assetid: BCF69196-D4E4-41D0-B372-5000FD50164B
title: Proveedores de credenciales en Windows 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a7947000e5d5a989f71dcdddd808a8e1d5ab3f
ms.sourcegitcommit: cd9672511263d04c0e4bc41758dd1d9e89ea92b4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2021
ms.locfileid: "104361764"
---
# <a name="credential-providers-in-windows-10"></a>Proveedores de credenciales en Windows 10

Los proveedores de credenciales son el mecanismo principal para la autenticación de usuarios: actualmente son el único método para que los usuarios demuestren su identidad, lo cual es necesario para los escenarios de inicio de sesión y otros tipos de autenticación del sistema. Con Windows 10 y la introducción de Microsoft Passport, los proveedores de credenciales son más importantes que nunca. se usarán para la autenticación en aplicaciones, sitios web, etc.

Microsoft proporciona una variedad de proveedores de credenciales como parte de Windows, como la contraseña, el PIN, la tarjeta inteligente y el reconocimiento de huellas digitales, caras y iris. Estos se conocen como "proveedores de credenciales del sistema" en este artículo. Los OEM, las empresas y otras entidades pueden escribir sus propios proveedores de credenciales e integrarlos fácilmente en Windows. Estos se conocen como "proveedores de credenciales de terceros" en este artículo. Tenga en cuenta que los proveedores de credenciales V1 y V2 se admiten en Windows 10. Es importante que los creadores y administradores de proveedores de credenciales de terceros conozcan estas recomendaciones.

## <a name="system-credential-providers"></a>Proveedores de credenciales del sistema

Se recomienda encarecidamente que siempre haya al menos un proveedor de credenciales del sistema disponible para todos los usuarios del dispositivo, además de los proveedores de credenciales de terceros. Además, durante la configuración del proveedor de credenciales de terceros, se debe solicitar a cada usuario del dispositivo que configure al menos un proveedor de credenciales del sistema (si no hay otras opciones de recuperación disponibles; consulte el escenario A a continuación).

### <a name="scenario-a"></a>Escenario A

Un usuario de la cuenta local ha configurado un proveedor de credenciales de terceros y lo usa con regularidad para iniciar sesión en el dispositivo. Un día, el usuario instala algunas actualizaciones en el dispositivo que interrumpen el proveedor de credenciales de terceros y el usuario no es consciente de este cambio antes de reiniciar el equipo.

En el siguiente reinicio, el usuario se encuentra en la pantalla de inicio de sesión y no puede usar el proveedor de credenciales de terceros esperado. Si el usuario ha configurado un proveedor de credenciales del sistema, el usuario podrá iniciar sesión en el equipo con él. Si no es así, el usuario no tiene ninguna manera de recuperar la cuenta en el equipo.

### <a name="scenario-b"></a>Escenario B

Un usuario de la cuenta de MSA/AD/AAD ha configurado un proveedor de credenciales de terceros y lo usa con regularidad para iniciar sesión en el dispositivo. Un día, el usuario instala algunas actualizaciones en el dispositivo que interrumpen el proveedor de credenciales de terceros y el usuario no es consciente de este cambio antes de reiniciar el equipo.

En el siguiente reinicio, el usuario se encuentra en la pantalla de inicio de sesión y no puede usar el proveedor de credenciales de terceros esperado. Si el usuario ha configurado un proveedor de credenciales del sistema, el usuario podrá iniciar sesión en el equipo con él. Como alternativa, si el proveedor de credenciales de contraseña del sistema está disponible, el usuario puede solicitar o restablecer la contraseña de forma remota y usarla para iniciar sesión en la máquina. Si ninguna de las opciones está disponible, el usuario no tiene ninguna manera de recuperar la cuenta en el equipo.

### <a name="conclusion"></a>Conclusión

En Resumen, queremos deshabilitar la deshabilitación de todos los proveedores de credenciales del sistema en un dispositivo. Aunque los proveedores de credenciales de terceros pueden cumplir requisitos de autenticación adicionales para grupos concretos de usuarios, es muy importante asegurarse de que el usuario siempre puede recuperar el acceso a su equipo cuando se produce un cambio importante. Los proveedores de credenciales del sistema proporcionan esta garantía.

## <a name="custom-credential-providers"></a>Proveedores de credenciales personalizadas

El marco de trabajo del proveedor de credenciales de Windows permite a los desarrolladores crear proveedores de credenciales personalizados. Cuando [Winlogon](winlogon.md) desea recopilar credenciales, la interfaz de usuario de inicio de sesión consulta cada proveedor de credenciales para conocer el número de credenciales que desea enumerar. Una vez que todos los proveedores han enumerado sus iconos, la interfaz de usuario de inicio de sesión los muestra al usuario. Después, el usuario interactúa con un icono para proporcionar las credenciales necesarias. La interfaz de usuario de inicio de sesión envía estas credenciales para la autenticación. La interfaz de usuario de credenciales también puede usar los proveedores de credenciales cuando se necesitan credenciales. Consulte [**\_ escenario de \_ uso \_ del proveedor de credenciales**](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario) para obtener una lista de escenarios en los que se puede admitir un proveedor de credenciales.

Gracias a este sistema, es mucho más fácil crear un proveedor de credenciales de lo que históricamente. Gran parte del trabajo se controla mediante la combinación de [Winlogon](winlogon.md), la interfaz de usuario de inicio de sesión y la interfaz de usuario de credenciales. Para ello, tendrá que crear su propia implementación de [**ICredentialProvider**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider) y [**ICredentialProviderCredential**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential). Si está implementando un proveedor de credenciales V2, lo que se recomienda, también tendrá que implementar [**ICredentialProviderCredential2**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential2).

Es importante tener en cuenta que los proveedores de credenciales no son mecanismos de cumplimiento. Simplemente se usan para recopilar y serializar las credenciales, y enviarlas para la autorización. La autoridad local y los paquetes de autenticación controlarán y cualquier aplicación de seguridad necesaria.

Al combinar proveedores de credenciales con hardware compatible, puede extender Windows para admitir el inicio de sesión con información biométrica, contraseñas, PIN, certificados de tarjeta inteligente o cualquier paquete de autenticación personalizado que decida crear. También puede personalizar la experiencia de inicio de sesión del usuario de diversas maneras. Por ejemplo, cuando la interfaz de usuario de inicio de sesión consulta el proveedor de credenciales para los iconos de credenciales, puede especificar un icono predeterminado para proporcionar una experiencia personalizada a un usuario. Los proveedores de credenciales pueden incluso diseñarse para admitir el inicio de sesión único (SSO), autenticar a los usuarios en un punto de acceso seguro, así como iniciar sesión en el equipo.

Los proveedores de credenciales se registran en un equipo Windows y son responsables de lo siguiente.

-   Que describe la información de credenciales necesaria para la autenticación.
-   Control de la comunicación y la lógica con cualquier entidad de autenticación externa.
-   Empaquetar las credenciales para el inicio de sesión interactivo y de red.

> [!TIP]
>
> Tenga en cuenta que se pueden instalar varios proveedores de credenciales en un único equipo.

## <a name="wrapping-credential-providers"></a>Encapsular proveedores de credenciales

Se puede ajustar un proveedor de credenciales del sistema para agregar funcionalidad a ese proveedor de credenciales que no se admite de forma nativa. Esto no es recomendable porque puede dar lugar a un comportamiento problemático. Se pueden realizar cambios en el proveedor de credenciales, lo que puede entrar en conflicto con el contenedor, lo que produce una mala experiencia del usuario o incluso impedir que el usuario entre en su dispositivo. Esto es especialmente cierto con la cadencia de actualización frecuente de Windows 10.

Si se necesita funcionalidad en un proveedor de credenciales que no se incluye de forma nativa, la ruta de acceso recomendada es crear un proveedor de credenciales personalizado. Se trata de un enfoque más estable que no tiene dependencias en los proveedores del sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Experiencia de inicio de sesión Windows controlada por el proveedor de credenciales](https://go.microsoft.com/fwlink/?LinkId=717287)
</dt> <dt>

[ICredentialProvider](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider)
</dt> <dt>

[\_ \_ serialización de credenciales del proveedor de credenciales \_](/windows/desktop/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization)
</dt> <dt>

[\_escenario de \_ uso del proveedor de credenciales \_](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario)
</dt> </dl>

 

 
