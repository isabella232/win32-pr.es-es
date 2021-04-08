---
title: Integridad y privacidad
description: Las comunicaciones entre el cliente y el servicio que requieren autenticación mutua deben proteger el tráfico que intercambian después de la autenticación correcta.
ms.assetid: 5ae3ede3-6eed-4532-9b02-448d2f4ca674
ms.tgt_platform: multiple
keywords:
- AD de integridad y privacidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ed167c3796aec2b0717b1207ff56565ec94afa
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995075"
---
# <a name="integrity-and-privacy"></a>Integridad y privacidad

Las comunicaciones entre el cliente y el servicio que requieren autenticación mutua deben proteger el tráfico que intercambian después de la autenticación correcta. No es aconsejable realizar la autenticación mutua en el momento de la conexión inicial con el servicio si el tráfico está sujeto posteriormente a la modificación por parte de un usuario no autorizado. SSPI, RPC y COM proporcionan utilidades para firmar y cifrar mensajes digitalmente. La aplicación de firmas digitales evita que el tráfico modificado salga de la detección y desaconseja la interceptación. Se puede interceptar el tráfico, pero el descifrado del tráfico es suficientemente difícil para impedir la mayoría de los usuarios no autorizados.

A menos que los requisitos de rendimiento sean graves, se recomienda el uso de la firma y el cifrado, especialmente para las funciones administrativas. Incluso cuando el rendimiento es un problema, algunos clientes eligen una seguridad más estricta sobre el mejor rendimiento. En tales casos, las opciones de integridad y privacidad configurables con mayor seguridad son las opciones predeterminadas y de mayor rendimiento que la opción.

Los clientes RPC pueden especificar el nivel de integridad y privacidad cuando llaman a la función [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) para establecer los datos de autenticación para el enlace RPC. Use la integridad de la **PKT de nivel de autenticación de RPC \_ c \_ \_ \_ \_** para la firma y la **\_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC c** para el cifrado. Para obtener más información, vea [autenticación mutua en aplicaciones RPC](mutual-authentication-in-rpc-applications.md).

Los servicios que usan un paquete SSPI para la autenticación mutua pueden consultar el paquete para determinar si admite las funciones [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature), [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)y [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) para firmar y cifrar mensajes. Para obtener más información y un ejemplo de código, consulte asegurar la integridad de la [comunicación durante el intercambio de mensajes](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

 

 