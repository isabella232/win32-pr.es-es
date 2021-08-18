---
title: Integridad y privacidad
description: Las comunicaciones de cliente y servicio que requieren autenticación mutua deben proteger el tráfico que intercambian después de una autenticación correcta.
ms.assetid: 5ae3ede3-6eed-4532-9b02-448d2f4ca674
ms.tgt_platform: multiple
keywords:
- Integridad y privacidad de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7c287956fcebc250d5324a15f88fb6a47e087fca40f68f793dd695b47e6719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187109"
---
# <a name="integrity-and-privacy"></a>Integridad y privacidad

Las comunicaciones de cliente y servicio que requieren autenticación mutua deben proteger el tráfico que intercambian después de una autenticación correcta. No es imprudente autenticarse mutuamente en el momento de la conexión inicial con el servicio si el tráfico está sujeto posteriormente a modificaciones por parte de un usuario no autorizado. SSPI, RPC y COM proporcionan utilidades para firmar y cifrar digitalmente los mensajes. La aplicación de firmas digitales impide que el tráfico modificado no se detecte y desaconseja la interceptación. Por supuesto, el tráfico se puede interceptar, pero descifrar el tráfico es lo suficientemente difícil como para disuadir a la mayoría de los usuarios no autorizados.

A menos que los requisitos de rendimiento sean graves, se recomienda usar tanto la firma como el cifrado, especialmente para las funciones administrativas. Incluso cuando el rendimiento es un problema, algunos clientes eligen una seguridad más estricta en lugar de un mejor rendimiento. En tales casos, haga que las opciones de integridad y privacidad configurables con mayor seguridad sea la opción predeterminada y de mayor rendimiento.

Los clientes RPC pueden especificar el nivel de integridad y privacidad cuando llaman a la [**función RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) para establecer los datos de autenticación para el enlace RPC. Use **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY** para firmar y **RPC C \_ \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** para el cifrado. Para obtener más información, vea [Autenticación mutua en aplicaciones RPC.](mutual-authentication-in-rpc-applications.md)

Los servicios que usan un paquete SSPI para la autenticación mutua pueden consultar el paquete para determinar si admite las funciones [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature,**](/windows/desktop/api/sspi/nf-sspi-verifysignature) [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)y [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) para firmar y cifrar mensajes. Para obtener más información y un ejemplo de código, vea [Ensuring Communication Integrity During Message Exchange](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

 

 