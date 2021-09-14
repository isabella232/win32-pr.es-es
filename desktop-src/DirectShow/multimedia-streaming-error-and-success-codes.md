---
description: Errores de streaming multimedia y códigos de éxito
ms.assetid: 3b7a11d2-55b9-4505-8eb2-46be423c662b
title: Errores de streaming multimedia y códigos de éxito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54a185b46134f4603c7adea0f1b4467da3a2cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254324"
---
# <a name="multimedia-streaming-error-and-success-codes"></a>Errores de streaming multimedia y códigos de éxito

> [!Note]  
> Esta API está en desuso. Las nuevas aplicaciones no deben usarla.

 

La lista siguiente contiene mensajes de error y notificaciones de éxito para las aplicaciones que usan las interfaces de streaming multimedia. Esta lista no contiene todos los errores posibles; los errores mostrados se aplican específicamente a la implementación ® DirectShow® microsoft de las interfaces de streaming multimedia.



| Value                       | Código hexadecimal | Descripción                                                                                                                                                                                |
|-----------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MS \_ PENDIENTE \_              | 0x00040001       | La actualización de ejemplo aún no se ha completado.                                                                                                                                                         |
| MS \_ S \_ NOUPDATE             | 0x00040002       | El ejemplo no se actualizó después de la finalización forzada.                                                                                                                                            |
| MS \_ S \_ ENDOFSTREAM          | 0x00040003       | Final de la secuencia. Ejemplo no actualizado.                                                                                                                                                         |
| MS \_ E \_ SAMPLEALLOC          | 0x80040401       | No se pudo quitar un objeto [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) de un objeto [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) porque todavía contiene al menos una muestra asignada. |
| MS \_ E \_ PURPOSEID            | 0x80040402       | El identificador de propósito especificado no se puede usar para la llamada.                                                                                                                                       |
| MS \_ E \_ NOSTREAM             | 0x80040403       | No se puede encontrar ninguna secuencia con los atributos especificados.                                                                                                                                      |
| MS \_ E \_ NOSEEKING            | 0x80040404       | Búsqueda no admitida para este [**objeto IMultiMediaStream.**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)                                                                                                      |
| MS \_ E \_ INCOMPATIBLE         | 0x80040405       | Los formatos de secuencia no son compatibles.                                                                                                                                                     |
| MS \_ E \_ BUSY                 | 0x80040406       | El ejemplo está ocupado.                                                                                                                                                                        |
| MS \_ E \_ NOTINIT              | 0x80040407       | El objeto no puede aceptar la llamada porque no se ha llamado a su función initialize o equivalente.                                                                                        |
| MS \_ E \_ SOURCEALREADYDEFINED | 0x80040408       | Origen ya definido.                                                                                                                                                                    |
| MS \_ E \_ INVALIDSTREAMTYPE    | 0x80040409       | El tipo de secuencia no es válido para esta operación.                                                                                                                                           |
| MS \_ E \_ NOTRUNNING           | 0x8004040A       | El [**objeto IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) no está en estado de ejecución.                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Multimedia Streaming](multimedia-streaming.md)
</dt> </dl>

 

 



