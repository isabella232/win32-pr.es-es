---
title: Desactivar la seguridad de llamadas
description: 'La seguridad de llamadas determina si un cliente tiene permiso para llamar a los métodos de un servidor. Hay dos maneras de deshabilitar la seguridad de llamadas: una implica el uso de Dcomcnfg.exe para modificar el registro y la otra requiere llamadas a CoInitializeSecurity.'
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a838a9c7936c126a1fedeeafc977f55641b63c5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160528"
---
# <a name="turning-off-call-security"></a>Desactivar la seguridad de llamadas

La seguridad de llamadas determina si un cliente tiene permiso para llamar a los métodos de un servidor. Hay dos maneras de deshabilitar la seguridad de las llamadas: una implica el uso de Dcomcnfg.exe para modificar el registro y la otra requiere llamadas a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

-   [Desactivar la seguridad de llamadas mediante DCOMCNFG](#turning-off-call-security-using-dcomcnfg)
-   [Desactivar la seguridad de llamadas mediante programación](#turning-off-call-security-programmatically)
-   [Temas relacionados](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a>Desactivar la seguridad de llamadas mediante DCOMCNFG

La seguridad de las llamadas se puede desactivar más fácilmente mediante Dcomcnfg.exe para modificar el Registro. Sin embargo, Dcomcnfg.exe para desactivar la seguridad solo funcionará si el cliente y el servidor no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Esto se debe a que cuando se llama a **CoInitializeSecurity,** DCOM omite la configuración del Registro y usa los valores proporcionados a **CoInitializeSecurity en su** lugar.

Para desactivar la seguridad con Dcomcnfg.exe, tanto el cliente como el servidor deben establecer sus niveles de autenticación en Ninguno. Deben completarse los pasos siguientes:

1.  Ejecute Dcomcnfg.exe.
2.  En la **página** Aplicaciones, seleccione la aplicación que representa el servidor. Haga clic en **el botón** Propiedades (o haga doble clic en la aplicación seleccionada).
3.  Haga clic en la pestaña **General**.
4.  En el **cuadro de lista Nivel** de autenticación predeterminado, seleccione **(Ninguno).**
5.  Haga clic en **el botón** Aplicar para aplicar los cambios; sin embargo, los cambios no se aplican a ninguna instancia en ejecución de la aplicación.
6.  Si el cliente aparece en  la lista de la página Aplicaciones, repita los pasos del 2 al 5, eligiendo el cliente en lugar del servidor para el paso 2. A continuación, haga clic en el botón **Aceptar**. Si el cliente no está en la lista, puede realizar una de las tres acciones siguientes:
    -   Puede establecer el nivel de autenticación del cliente en Ninguno en todo el equipo mediante Dcomcnfg.exe. (Vea la advertencia y el procedimiento siguiente).
    -   Puede establecer el nivel de autenticación del cliente en Ninguno mediante programación.
    -   Puede crear una clave [AppID](appid-key.md) para que el cliente indique un nivel de autenticación Ninguno. (Consulte [Configuración de Process-Wide seguridad mediante el Registro).](setting-processwide-security-through-the-registry.md)

Para establecer el nivel de autenticación en Ninguno en todo el equipo:

> [!Note]  
> Establecer el nivel de autenticación de todo el equipo en Ninguno no es muy seguro.

 

1.  Ejecute Dcomcnfg.exe.
2.  Elija la **pestaña Propiedades predeterminadas.**
3.  En el **cuadro de lista Nivel** de autenticación predeterminado, elija **(Ninguno).**
4.  Haga clic en el botón **Aceptar** .

## <a name="turning-off-call-security-programmatically"></a>Desactivar la seguridad de llamadas mediante programación

Para desactivar la seguridad de llamadas mediante programación, tanto el cliente como el servidor deben llamar a **CoInitializeSecurity** y establecer el nivel de autenticación del parámetro *dwAuthnLevel* en RPC \_ C \_ AUTHN \_ LEVEL \_ NONE.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desactivar la seguridad de activación](turning-off-activation-security.md)
</dt> </dl>

 

 




