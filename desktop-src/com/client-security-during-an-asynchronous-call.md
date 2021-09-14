---
title: Seguridad de cliente durante una llamada asincrónica
description: Seguridad de cliente durante una llamada asincrónica
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bea2f83bf6341704dd0265a37ec2f64b79e9b2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973677"
---
# <a name="client-security-during-an-asynchronous-call"></a>Seguridad de cliente durante una llamada asincrónica

El administrador de proxy creado por MIDL para los objetos que usan la serialización estándar implementa la [**interfaz IClientSecurity.**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) Los clientes pueden administrar la seguridad de las llamadas serializadas consultando **IClientSecurity** en el objeto de llamada y obteniendo o cambiando la configuración de seguridad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Realizar una llamada asincrónica](making-an-asynchronous-call.md)
</dt> </dl>

 

 




