---
description: Los protocolos de Schannel requieren credenciales para autenticar servidores y, opcionalmente, clientes.
ms.assetid: 8295b1bd-6ae1-4f7e-926d-a9da7ec6a524
title: Credenciales de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91556a7e3bfca67aa386f0264e78ae67052f02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001850"
---
# <a name="schannel-credentials"></a>Credenciales de Schannel

Los protocolos de Schannel requieren credenciales para autenticar servidores y, opcionalmente, clientes. La autenticación de servidor, donde el servidor proporciona la prueba de su identidad al cliente, es necesaria para los [*protocolos de seguridad*](../secgloss/s-gly.md)de Schannel. El servidor puede solicitar la autenticación de cliente en cualquier momento.

Las credenciales de Schannel son certificados [*X. 509*](../secgloss/x-gly.md) . La información de clave [*pública*](../secgloss/p-gly.md) y [*privada*](../secgloss/p-gly.md) de los certificados se usa para autenticar el servidor y, opcionalmente, el cliente. Estas claves también se usan para proporcionar [*integridad*](../secgloss/i-gly.md) del mensaje, mientras que el cliente y el servidor intercambian la información necesaria para generar e intercambiar [*claves de sesión*](../secgloss/s-gly.md).

Para obtener información de programación, consulte [obtención de credenciales de Schannel](obtaining-schannel-credentials.md).

 

 
