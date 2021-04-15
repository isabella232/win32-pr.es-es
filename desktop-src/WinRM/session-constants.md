---
title: Constantes de sesión
description: Las constantes de sesión en la \_ \_ enumeración WSManSessionFlags especifican la autenticación y otra información para las llamadas a WSMan. createSession o IWSMan createSession que se conectan a un equipo remoto.
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8417289a218203dbdaee288ff03096d894f4bd4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714127"
---
# <a name="session-constants"></a>Constantes de sesión

Las constantes de sesión en la enumeración **\_ \_ WSManSessionFlags** especifican la autenticación y otra información para las llamadas [**WSMan. createSession**](wsman-createsession.md) o [**IWSMan:: createSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) que se conectan a un equipo remoto. Estas constantes también están estrechamente relacionadas con los modificadores de la herramienta de línea de comandos de **WinRM** .

## <a name="using-session-constants"></a>Usar constantes de sesión

Puede establecer las marcas de sesión para la llamada a [**WSMan. createSession**](wsman-createsession.md) de dos maneras diferentes. Una es más corta y más sencilla. La forma más larga, como se muestra en el ejemplo siguiente, es ubicar el valor de la marca que desea usar y crear una constante en el script con ese valor. A continuación, la constante se usa para establecer el valor del parámetro *iFlags* .

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

La manera recomendada, como se muestra en el ejemplo siguiente, es usar el método de objeto [**WSMan**](wsman.md) asociado a la marca.

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Constantes de autenticación**](authentication-constants.md)
</dt> <dd>

Especifique el método de autenticación y cómo administrar los servidores de certificados.

</dd> <dt>

<span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Otras constantes de sesión**](other-session-constants.md)
</dt> <dd>

Especifique la codificación, el cifrado y el puerto de nombre de entidad de seguridad de servicio.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes y enumeraciones de WinRM](winrm-constants-and-enumerations.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[Autenticación para conexiones remotas](authentication-for-remote-connections.md)
</dt> </dl>

 

 




