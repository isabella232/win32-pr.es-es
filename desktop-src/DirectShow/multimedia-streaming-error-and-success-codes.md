---
description: Códigos de error y éxito de streaming multimedia
ms.assetid: 3b7a11d2-55b9-4505-8eb2-46be423c662b
title: Códigos de error y éxito de streaming multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54a185b46134f4603c7adea0f1b4467da3a2cf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361938"
---
# <a name="multimedia-streaming-error-and-success-codes"></a>Códigos de error y éxito de streaming multimedia

> [!Note]  
> Esta API está en desuso. Las nuevas aplicaciones no deben utilizarla.

 

La lista siguiente contiene los mensajes de error y las notificaciones correctas para las aplicaciones que usan las interfaces de transmisión por secuencias de multimedia. Esta lista no contiene todos los errores posibles; los errores mostrados se aplican específicamente a la implementación de Microsoft® DirectShow® de las interfaces de streaming multimedia.



| Value                       | Código hexadecimal | Descripción                                                                                                                                                                                |
|-----------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MS \_ S \_ pendientes              | 0x00040001       | Todavía no se ha completado la actualización de ejemplo.                                                                                                                                                         |
| noactualizar MS \_ S \_             | 0x00040002       | El ejemplo no se actualizó después de la finalización forzada.                                                                                                                                            |
| \_ENDOFSTREAM MS S \_          | 0x00040003       | Final de la secuencia. Muestra no actualizada.                                                                                                                                                         |
| MS \_ E \_ SAMPLEALLOC          | 0x80040401       | No se pudo quitar un objeto [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) de un objeto [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) porque todavía contiene al menos un ejemplo asignado. |
| MS \_ E \_ PURPOSEID            | 0x80040402       | No se puede usar el ID. de propósito especificado para la llamada.                                                                                                                                       |
| MS \_ E \_ nostream             | 0x80040403       | No se puede encontrar ningún flujo con los atributos especificados.                                                                                                                                      |
| MS \_ E \_ nobúsqueda            | 0x80040404       | No se admite la búsqueda en este objeto [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) .                                                                                                      |
| MS \_ E \_ incompatible         | 0x80040405       | Los formatos de secuencia no son compatibles.                                                                                                                                                     |
| MS \_ E \_ ocupado                 | 0x80040406       | El ejemplo está ocupado.                                                                                                                                                                        |
| MS \_ E \_ NOTINIT              | 0x80040407       | El objeto no puede aceptar la llamada porque no se ha llamado a su función Initialize o equivalente.                                                                                        |
| MS \_ E \_ SOURCEALREADYDEFINED | 0x80040408       | El origen ya está definido.                                                                                                                                                                    |
| MS \_ E \_ INVALIDSTREAMTYPE    | 0x80040409       | El tipo de flujo no es válido para esta operación.                                                                                                                                           |
| MS \_ E \_ NOTRUNNING           | 0x8004040A       | El objeto [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) no está en estado de ejecución.                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transmisión por secuencias multimedia](multimedia-streaming.md)
</dt> </dl>

 

 



