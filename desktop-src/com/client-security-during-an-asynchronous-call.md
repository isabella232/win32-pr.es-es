---
title: Seguridad de cliente durante una llamada asincrónica
description: Seguridad de cliente durante una llamada asincrónica
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4c25e17712d0164938f3de9895d1e6b02582f2d86cba9957297e23aa4e7f1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071045"
---
# <a name="client-security-during-an-asynchronous-call"></a>Seguridad de cliente durante una llamada asincrónica

El administrador de proxy creado por MIDL para los objetos que usan la serialización estándar implementa la [**interfaz IClientSecurity.**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) Los clientes pueden administrar la seguridad de las llamadas serializadas consultando **IClientSecurity** en el objeto de llamada y obteniendo o cambiando la configuración de seguridad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Realizar una llamada asincrónica](making-an-asynchronous-call.md)
</dt> </dl>

 

 




