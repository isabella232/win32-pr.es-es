---
title: Constantes de derechos
description: Constantes de derechos
ms.assetid: fb20dc57-25da-4613-a324-e081ba87df73
keywords:
- Windows SDK de formato multimedia, constantes
- administración de derechos digitales (DRM),constantes
- DRM (administración de derechos digitales), constantes
- API extendidas de cliente DRM, constantes
- API extendidas de cliente, constantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 088c3130551a6798900ea77cc3628cb784ff7c70b418795157b203ab2f71b64e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110145"
---
# <a name="rights-constants"></a>Constantes de derechos

Las constantes enumeradas en la tabla siguiente se usan para identificar acciones DRM y para compilar listas de acciones.



| Constante                                        | Descripción                                                                                                                                                                                                                                                    |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ ACTIONLIST \_ TAG                    | Define el nombre del elemento XML para una lista de acciones.                                                                                                                                                                                                               |
| g \_ wszWMDRM \_ ACTION \_ TAG                        | Define el nombre del elemento XML para una entrada de una lista de acciones.                                                                                                                                                                                                   |
| g \_ wszWMDRM \_ RIGHT \_ PLAYBACK                    | Define la cadena del derecho para reproducir contenido.                                                                                                                                                                                                              |
| g \_ wszWMDRM \_ RIGHT \_ COPY                        | Define la cadena del derecho para copiar contenido.                                                                                                                                                                                                              |
| g \_ wszWMDRM \_ RIGHT PLAYLIST \_ \_ BURN              | Define la cadena del derecho para grabar contenido en CD como parte de una lista de reproducción.                                                                                                                                                                                  |
| g \_ wszWMDRM \_ RIGHT CREATE THUMBNAIL \_ \_ \_ IMAGE    | Define la cadena de la derecha para crear una imagen en miniatura a partir del contenido del vídeo.                                                                                                                                                                               |
| g \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ CD                | Define la cadena del derecho para copiar contenido en un CD. Las nuevas licencias no deben usar este derecho. En su lugar, todos los derechos que conceden permiso para copiar contenido deben estar cubiertos por el derecho de copia y el derecho de grabación de la lista de reproducción.                                     |
| g \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ SDMI \_ DEVICE      | Define la cadena del derecho para copiar contenido en un dispositivo que se ajuste a la iniciativa de Música digital seguro (SDMI). Las nuevas licencias no deben usar este derecho. En su lugar, todos los derechos que conceden permiso para copiar contenido deben estar cubiertos por el derecho de copia. |
| g \_ wszWMDRM \_ RIGHT COPY TO NON \_ \_ \_ \_ SDMI \_ DEVICE | Define la cadena del derecho para copiar en un dispositivo que no se ajusta a secure digital Música Initiative (SDMI). Las nuevas licencias no deben usar este derecho. En su lugar, todos los derechos que conceden permiso para copiar contenido deben estar cubiertos por el derecho de copia. |
| g \_ wszWMDRM \_ RIGHT \_ BACKUP                      | Define la cadena del derecho para realizar una copia de seguridad de la licencia.                                                                                                                                                                                                        |
| g \_ wszWMDRM \_ RIGHT COLLABORATIVE \_ \_ PLAY         | Define la cadena del derecho para reproducir contenido a través de una red como parte de una lista de reproducción compartida.                                                                                                                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Constantes**](constants.md)
</dt> </dl>

 

 




