---
title: Operaciones de red DRM
description: Operaciones de red DRM
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- Windows SDK de formato multimedia, operaciones de red DRM
- Formato de sistemas avanzados (ASF), operaciones de red DRM
- ASF (formato de sistemas avanzados), operaciones de red DRM
- administración de derechos digitales (DRM), operaciones de red
- DRM (administración de derechos digitales), operaciones de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f026ed972b88a1e6290bdd513012c2fab758da2c5b4b91a6a1162df5d258207
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771755"
---
# <a name="drm-network-operations"></a>Operaciones de red DRM

Varias operaciones relacionadas con DRM requieren que la aplicación se conecte a un servicio que se ejecuta en una red. Estas operaciones incluyen la individualización, la adquisición de licencias, la revocación de licencias y la copia de seguridad y restauración de licencias.

Al igual que con cualquier transacción de red, la aplicación debe tener en cuenta diversas dificultades al incluir características que requieren operaciones de red. La aplicación debe realizar un seguimiento del estado de la operación en la medida en que sea posible para la característica específica, normalmente controlando los mensajes de estado. Debe proporcionar comentarios al usuario sobre el estado. Si se produce un error en una operación en el primer intento, debe dar al usuario la oportunidad de volver a intentarlo. En muchos casos, el primer intento encuentra dificultades, pero un intento posterior se completa sin errores.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




