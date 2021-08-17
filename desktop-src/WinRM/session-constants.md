---
title: Constantes de sesión
description: Las constantes de sesión de la enumeración WSManSessionFlags especifican la autenticación y otra información para las llamadas CreateSession de \_ \_ WSMan.CreateSession o IWSMan que se conectan a un equipo remoto.
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584eb15c4b235a006b52551de8f9999ddb65459412af68db81f0500a0828888b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743236"
---
# <a name="session-constants"></a>Constantes de sesión

Las constantes de sesión de la enumeración **\_ \_ WSManSessionFlags** especifican la autenticación y otra información para las llamadas [**WSMan.CreateSession**](wsman-createsession.md) o [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) que se conectan a un equipo remoto. Estas constantes también están estrechamente relacionadas con los modificadores de la herramienta de línea de comandos **winrm.**

## <a name="using-session-constants"></a>Uso de constantes de sesión

Puede establecer las marcas de sesión de la llamada en [**WSMan.CreateSession**](wsman-createsession.md) de dos maneras diferentes. Uno es más corto y más sencillo. La forma más larga, como se muestra en el ejemplo siguiente, es buscar el valor de la marca que desea usar y crear una constante en el script con ese valor. A continuación, se usa la constante para establecer el valor del *parámetro iFlags.*

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

La manera recomendada, como se muestra en el ejemplo siguiente, es usar el método de [**objeto WSMan**](wsman.md) asociado a la marca .

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Constantes de autenticación**](authentication-constants.md)
</dt> <dd>

Especifique el método de autenticación y cómo controlar los servidores de certificados.

</dd> <dt>

<span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Otras constantes de sesión**](other-session-constants.md)
</dt> <dd>

Especifique el puerto de codificación, cifrado y nombre de entidad de seguridad de servicio.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes y enumeraciones de WinRM](winrm-constants-and-enumerations.md)
</dt> <dt>

[**WSMan.CreateSession**](wsman-createsession.md)
</dt> <dt>

[Autenticación para conexiones remotas](authentication-for-remote-connections.md)
</dt> </dl>

 

 




