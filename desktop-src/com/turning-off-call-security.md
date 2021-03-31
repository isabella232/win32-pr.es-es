---
title: Desactivación de la seguridad de llamadas
description: 'La seguridad de llamada determina si un cliente tiene permiso para llamar a los métodos de un servidor. Hay dos formas de deshabilitar la seguridad de la llamada: el uso de Dcomcnfg.exe para modificar el registro y el otro requiere llamadas a CoInitializeSecurity.'
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a838a9c7936c126a1fedeeafc977f55641b63c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418475"
---
# <a name="turning-off-call-security"></a>Desactivación de la seguridad de llamadas

La seguridad de llamada determina si un cliente tiene permiso para llamar a los métodos de un servidor. Hay dos formas de deshabilitar la seguridad de llamada: una implica el uso de Dcomcnfg.exe para modificar el registro y la otra requiere llamadas a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

-   [Desactivar la seguridad de llamadas mediante DCOMCNFG](#turning-off-call-security-using-dcomcnfg)
-   [Desactivar la seguridad de llamadas mediante programación](#turning-off-call-security-programmatically)
-   [Temas relacionados](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a>Desactivar la seguridad de llamadas mediante DCOMCNFG

La seguridad de llamadas se puede desactivar más fácilmente mediante Dcomcnfg.exe para modificar el registro. Sin embargo, el uso de Dcomcnfg.exe para desactivar la seguridad funcionará solo si el cliente y el servidor no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Esto se debe a que cuando se llama a **CoInitializeSecurity** , DCOM omite la configuración del registro y usa en su lugar los valores proporcionados a **CoInitializeSecurity** .

Para desactivar la seguridad con Dcomcnfg.exe, tanto el cliente como el servidor deben establecer sus niveles de autenticación en ninguno. Se deben completar los siguientes pasos:

1.  Ejecute Dcomcnfg.exe.
2.  En la página **aplicaciones** , seleccione la aplicación que representa el servidor. Haga clic en el botón **propiedades** (o haga doble clic en la aplicación seleccionada).
3.  Haga clic en la pestaña **General**.
4.  En el cuadro de lista **nivel de autenticación predeterminado** , seleccione **(ninguno)**.
5.  Haga clic en el botón **aplicar** para aplicar los cambios; sin embargo, los cambios no se aplican a las instancias en ejecución de la aplicación.
6.  Si el cliente aparece en la lista de la página *aplicaciones* , repita los pasos del 2 al 5 y elija el cliente en lugar del servidor para el paso 2. A continuación, haga clic en el botón **Aceptar**. Si el cliente no está en la lista, puede realizar una de estas tres acciones:
    -   Puede establecer el nivel de autenticación del cliente en ninguno en todo el equipo mediante Dcomcnfg.exe. (Vea la advertencia y el procedimiento que se indica a continuación).
    -   Puede establecer el nivel de autenticación del cliente en ninguno mediante programación.
    -   Puede crear una clave [AppID](appid-key.md) para que el cliente indique un nivel de autenticación de ninguno. (Consulte [configuración de Process-Wide seguridad a través del registro](setting-processwide-security-through-the-registry.md)).

Para establecer el nivel de autenticación en ninguno en todo el equipo:

> [!Note]  
> Establecer el nivel de autenticación para todo el equipo en ninguno es extremadamente poco seguro.

 

1.  Ejecute Dcomcnfg.exe.
2.  Elija la pestaña **propiedades predeterminadas** .
3.  En el cuadro de lista **nivel de autenticación predeterminado** , elija **(ninguno)**.
4.  Haga clic en el botón **Aceptar** .

## <a name="turning-off-call-security-programmatically"></a>Desactivar la seguridad de llamadas mediante programación

Para desactivar la seguridad de llamadas mediante programación, tanto el cliente como el servidor deben llamar a **CoInitializeSecurity**, estableciendo el nivel de autenticación en el parámetro *dwAuthnLevel* en el \_ \_ nivel none de autenticación de RPC C \_ \_ .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desactivar la seguridad de activación](turning-off-activation-security.md)
</dt> </dl>

 

 




