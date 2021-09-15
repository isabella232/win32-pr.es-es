---
description: Los protocolos Schannel requieren credenciales para autenticar servidores y, opcionalmente, clientes.
ms.assetid: 8295b1bd-6ae1-4f7e-926d-a9da7ec6a524
title: Credenciales de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91556a7e3bfca67aa386f0264e78ae67052f02c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476548"
---
# <a name="schannel-credentials"></a>Credenciales de Schannel

Los protocolos Schannel requieren credenciales para autenticar servidores y, opcionalmente, clientes. La autenticación de servidor, donde el servidor proporciona una prueba de su identidad al cliente, es necesaria por los [*protocolos*](../secgloss/s-gly.md)de seguridad de Schannel . El servidor puede solicitar la autenticación de cliente en cualquier momento.

Las credenciales de Schannel [*son certificados X.509.*](../secgloss/x-gly.md) [*La*](../secgloss/p-gly.md) información [*de clave pública y*](../secgloss/p-gly.md) privada de los certificados se usa para autenticar el servidor y, opcionalmente, el cliente. Estas claves también se usan para proporcionar integridad [*de*](../secgloss/i-gly.md) mensajes mientras el cliente y el servidor intercambian la información necesaria para generar e intercambiar claves [*de sesión*](../secgloss/s-gly.md).

Para obtener información de programación, [vea Obtención de credenciales de Schannel.](obtaining-schannel-credentials.md)

 

 
