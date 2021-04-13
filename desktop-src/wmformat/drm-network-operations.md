---
title: Operaciones de red DRM
description: Operaciones de red DRM
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- SDK de Windows Media Format, operaciones de red DRM
- Advanced Systems Format (ASF), operaciones de red DRM
- ASF (formato de sistemas avanzados), operaciones de red DRM
- Administración de derechos digitales (DRM), operaciones de red
- DRM (administración de derechos digitales), operaciones de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875186e43e066d71847da014468e9b1764b60cf2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356776"
---
# <a name="drm-network-operations"></a>Operaciones de red DRM

Varias operaciones relacionadas con DRM requieren que la aplicación se conecte a un servicio que se ejecuta en una red. Estas operaciones incluyen la individualización, adquisición de licencias, revocación de licencias y copia de seguridad y restauración de licencias.

Como con cualquier transacción de red, la aplicación debe tener en cuenta una serie de dificultades al incluir características que requieren operaciones de red. La aplicación debe realizar un seguimiento del estado de la operación en cualquier medida que sea posible para la característica específica, normalmente mediante el control de los mensajes de estado. Debe proporcionar comentarios al usuario sobre el estado. Si se produce un error en una operación en el primer intento, debe proporcionar al usuario la oportunidad de volver a intentarlo. En muchos casos, el primer intento tiene problemas, pero un intento posterior se completa sin errores.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




