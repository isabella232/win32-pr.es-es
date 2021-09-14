---
description: Proveedores de credenciales en Windows 10
ms.assetid: BCF69196-D4E4-41D0-B372-5000FD50164B
title: Proveedores de credenciales en Windows 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a7947000e5d5a989f71dcdddd808a8e1d5ab3f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160997"
---
# <a name="credential-providers-in-windows-10"></a>Proveedores de credenciales en Windows 10

Los proveedores de credenciales son el mecanismo principal para la autenticación de usuarios: actualmente son el único método para que los usuarios prueben su identidad, que es necesaria para el inicio de sesión y otros escenarios de autenticación del sistema. Con Windows 10 y la introducción de Microsoft Passport, los proveedores de credenciales son más importantes que nunca. se usarán para la autenticación en aplicaciones, sitios web y mucho más.

Microsoft proporciona una variedad de proveedores de credenciales como parte de Windows, como contraseña, PIN, tarjeta inteligente y Windows Hello (reconocimiento de huella digital, cara e iris). Estos se conocen como "proveedores de credenciales del sistema" en este artículo. Los OEM, las empresas y otras entidades pueden escribir sus propios proveedores de credenciales e integrarlos fácilmente en Windows. Estos se conocen como "proveedores de credenciales de terceros" en este artículo. Tenga en cuenta que los proveedores de credenciales V1 y V2 se admiten en Windows 10. Es importante que los creadores y administradores de proveedores de credenciales de terceros comprendan estas recomendaciones.

## <a name="system-credential-providers"></a>Proveedores de credenciales del sistema

Se recomienda encarecidamente que siempre haya al menos un proveedor de credenciales del sistema disponible para todos los usuarios del dispositivo, además de cualquier proveedor de credenciales de terceros. Además, durante la configuración del proveedor de credenciales de terceros, se debe solicitar a cada usuario del dispositivo que configure al menos un proveedor de credenciales del sistema (si no hay otras opciones de recuperación disponibles; consulte el escenario A a continuación).

### <a name="scenario-a"></a>Escenario A

Un usuario de cuenta local ha configurado un proveedor de credenciales de terceros y lo usa regularmente para iniciar sesión en el dispositivo. Un día, el usuario instala alguna actualización en el dispositivo que interrumpe el proveedor de credenciales de terceros y el usuario no es consciente de este cambio antes de reiniciar la máquina.

En el siguiente reinicio, el usuario está en la pantalla de inicio de sesión y no puede usar el proveedor de credenciales de terceros esperado. Si el usuario ha configurado un proveedor de credenciales del sistema, el usuario podrá iniciar sesión en la máquina con él. Si no es así, el usuario no tiene ninguna manera de recuperar la cuenta en la máquina.

### <a name="scenario-b"></a>Escenario B

Un usuario de cuenta de MSA/AD/AAD ha configurado un proveedor de credenciales de terceros y lo usa regularmente para iniciar sesión en el dispositivo. Un día, el usuario instala alguna actualización en el dispositivo que interrumpe el proveedor de credenciales de terceros y el usuario no es consciente de este cambio antes de reiniciar la máquina.

En el siguiente reinicio, el usuario está en la pantalla de inicio de sesión y no puede usar el proveedor de credenciales de terceros esperado. Si el usuario ha configurado un proveedor de credenciales del sistema, el usuario podrá iniciar sesión en la máquina con él. Como alternativa, si el proveedor de credenciales de contraseña del sistema está disponible, el usuario puede solicitar o restablecer la contraseña de forma remota y usarla para iniciar sesión en la máquina. Si ninguna opción está disponible, el usuario no tiene ninguna manera de recuperar la cuenta en la máquina.

### <a name="conclusion"></a>Conclusión

En resumen, queremos desaconsejan la deshabilitación de todos los proveedores de credenciales del sistema en un dispositivo. Aunque los proveedores de credenciales de terceros pueden cumplir requisitos de autenticación adicionales para determinados grupos de usuarios, es muy importante asegurarse de que el usuario siempre puede recuperar el acceso a su máquina cuando se produce un cambio importante. Los proveedores de credenciales del sistema proporcionan esta garantía.

## <a name="custom-credential-providers"></a>Proveedores de credenciales personalizadas

El marco Windows proveedor de credenciales permite a los desarrolladores crear proveedores de credenciales personalizados. Cuando [Winlogon quiere](winlogon.md) recopilar credenciales, la interfaz de usuario de inicio de sesión consulta a cada proveedor de credenciales el número de credenciales que desea enumerar. Una vez que todos los proveedores han enumerado sus iconos, la interfaz de usuario de inicio de sesión los muestra al usuario. A continuación, el usuario interactúa con un icono para proporcionar las credenciales necesarias. La interfaz de usuario de inicio de sesión envía estas credenciales para la autenticación. La interfaz de usuario de credenciales también puede usar proveedores de credenciales cuando son necesarias credenciales. Consulte [**ESCENARIO DE USO DEL PROVEEDOR DE \_ \_ \_ CREDENCIALES**](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario) para obtener una lista de escenarios en los que se puede admite un proveedor de credenciales.

Gracias a este sistema, es mucho más fácil crear un proveedor de credenciales que históricamente. Gran parte del trabajo se controla mediante la combinación de [Winlogon](winlogon.md), la interfaz de usuario de inicio de sesión y la interfaz de usuario de credenciales. Para ello, deberá crear su propia implementación de [**ICredentialProvider**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider) e [**ICredentialProviderCredential**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential). Si va a implementar un proveedor de credenciales V2, que se recomienda, también deberá implementar [**ICredentialProviderCredential2**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential2).

Es importante tener en cuenta que los proveedores de credenciales no son mecanismos de cumplimiento. Simplemente se usan para recopilar y serializar credenciales y enviarlas para su autorización. La autoridad local y los paquetes de autenticación controlarán y cualquier aplicación de seguridad necesaria.

Al combinar proveedores de credenciales con hardware compatible, puede ampliar Windows para admitir el inicio de sesión con información biométrica, contraseñas, PIN, certificados de tarjeta inteligente o cualquier paquete de autenticación personalizado que decida crear. También puede personalizar la experiencia de inicio de sesión para el usuario de varias maneras. Por ejemplo, cuando la interfaz de usuario de inicio de sesión consulta los iconos de credenciales al proveedor de credenciales, puede especificar un icono predeterminado para proporcionar una experiencia personalizada para un usuario. Los proveedores de credenciales incluso se pueden diseñar para admitir el inicio de sesión único (SSO), la autenticación de los usuarios en un punto de acceso seguro, así como el inicio de sesión automático.

Los proveedores de credenciales se registran en Windows máquina virtual y son responsables de lo siguiente.

-   Descripción de la información de credenciales necesaria para la autenticación.
-   Control de la comunicación y la lógica con cualquier autoridad de autenticación externa.
-   Empaquetar las credenciales para el inicio de sesión interactivo y de red.

> [!TIP]
>
> Tenga en cuenta que se pueden instalar varios proveedores de credenciales en una sola máquina.

## <a name="wrapping-credential-providers"></a>Ajuste de proveedores de credenciales

El ajuste de un proveedor de credenciales del sistema se puede realizar para agregar funcionalidad a ese proveedor de credenciales que no se admite de forma nativa. Esto no se recomienda porque puede provocar un comportamiento problemático. Se pueden realizar cambios en el proveedor de credenciales que pueden entrar en conflicto con el contenedor, lo que provoca una mala experiencia del usuario o incluso impide que el usuario entre en su dispositivo. Esto es especialmente cierto con la cadencia de actualización frecuente de Windows 10.

Si se necesita una funcionalidad en un proveedor de credenciales que no se incluye de forma nativa, la ruta de acceso recomendada es crear un proveedor de credenciales personalizado. Se trata de un enfoque más estable que no toma dependencias de los proveedores del sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedor de credenciales experiencia Windows inicio de sesión controlado](https://go.microsoft.com/fwlink/?LinkId=717287)
</dt> <dt>

[ICredentialProvider](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider)
</dt> <dt>

[SERIALIZACIÓN DE \_ CREDENCIALES DEL PROVEEDOR DE \_ \_ CREDENCIALES](/windows/desktop/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization)
</dt> <dt>

[ESCENARIO DE USO \_ DEL \_ PROVEEDOR DE \_ CREDENCIALES](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario)
</dt> </dl>

 

 
