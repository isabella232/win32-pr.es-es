---
title: Desactivar la seguridad de activación
description: Desactivar la seguridad de activación
ms.assetid: 3474f8ad-f041-4886-ad39-ff0603c5c69e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da3ebd7cc03d79fc38fbafe3bc652efc3499437
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369755"
---
# <a name="turning-off-activation-security"></a>Desactivar la seguridad de activación

Normalmente, la activación usa la configuración de seguridad predeterminada. Sin embargo, puede controlar la seguridad de activación especificando una estructura [**COAUTHINFO,**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) que es miembro de la estructura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) que se pasa a las funciones de activación. Si el cliente especifica un nivel de autenticación de RPC \_ C \_ AUTHN LEVEL NONE en la estructura \_ \_ **COAUTHINFO,** no se intenta la autenticación. De lo contrario, se intenta la activación segura y, si se produce un error en la autenticación, se produce un error en la activación.

Si el cliente no especifica una estructura [**COAUTHINFO explícita**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) y, en su lugar, establece el puntero en **NULL,** COM intentará autenticar el cliente. Si no puede autenticar el cliente, COM comprueba el descriptor de seguridad del permiso de inicio para ver si hay una **DACL** NULL o una ACL que permita el acceso a Todos. Si esta comprobación se realiza correctamente, se inicia el servidor. Por lo tanto, incluso si el cliente no especifica una estructura **COAUTHINFO,** la activación no segura puede tener lugar cuando el servidor lo permite.

> [!Note]  
> Para permitir que los usuarios de red no autenticados ejecuten una aplicación COM, los roles de aplicación deben incluir el usuario anónimo. A partir Windows Server 2003, de forma predeterminada, el usuario anónimo no se incluye en el grupo Todos.

 

¿Por qué un cliente desea desactivar la seguridad de activación explícitamente aunque la activación no segura se lleve a cabo si el servidor lo permite? Dado que desactivar explícitamente la seguridad de activación aumenta el rendimiento cuando el cliente no desea o necesita comprobaciones de seguridad.

Se deben realizar las siguientes acciones para desactivar explícitamente la seguridad de activación:

-   El cliente debe especificar un nivel de autenticación de RPC C AUTHN LEVEL NONE en la estructura COAUTHINFO que sea miembro de la estructura \_ \_ \_ \_ [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) [](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) proporcionada a la función de activación.
-   El cliente debe especificar un nivel de suplantación de RPC C IMP LEVEL IMPERSONATE en la estructura COAUTHINFO que sea miembro de la estructura \_ \_ \_ \_ [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) [](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) proporcionada a la función de activación. Si no se pasa este valor, recibirá RPC \_ S \_ SERVER \_ UNAVAILABLE.
-   El servidor debe especificar **Todos para** los permisos de **inicio predeterminados.** La manera recomendada de realizar esta tarea es usar Dcomcnfg.exe como se muestra a continuación:
    1.  Ejecute Dcomcnfg.exe.
    2.  En la **página** Aplicaciones, seleccione la aplicación que representa el servidor. Haga clic en **el botón** Propiedades (o haga doble clic en la aplicación seleccionada).
    3.  En la **página de** propiedades Seguridad, haga clic en el botón Usar permisos de **inicio personalizados.**
    4.  Haga clic **en el** botón Editar del área **Permisos de** inicio.
    5.  En el cuadro **de diálogo Permisos de valor del** Registro , haga clic en el **botón** Agregar.
    6.  Seleccione la entrada Todos **en** el cuadro de lista.
    7.  En el **cuadro de lista Tipo** de acceso, elija Permitir **inicio.**
    8.  Haga clic en el botón **Aceptar** .

> [!Note]  
> En Windows Server 2003, la funcionalidad de autenticación para la aplicación del sistema COM+ incluye el valor EOAC \_ DISABLE \_ AAA. Este valor, que deshabilita las activaciones de activación como activador (AAA), se usa en la llamada [**a CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) al iniciar la aplicación del sistema. Establecer la funcionalidad de autenticación en EOAC DISABLE AAA permite que una aplicación que se ejecuta con una cuenta con privilegios \_ (como LocalSystem) ayude a evitar que su identidad se utilice para iniciar componentes que no son de \_ confianza.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desactivar la seguridad de llamadas](turning-off-call-security.md)
</dt> </dl>

 

 