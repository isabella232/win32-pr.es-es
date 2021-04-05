---
title: WM/MediaClassSecondaryID
description: El atributo WM/MediaClassSecondaryID contiene el GUID de la clase multimedia secundaria.
ms.assetid: 3d1429bc-f168-4b25-9d26-c1c28b852160
keywords:
- Formato de Windows Media WM/MediaClassSecondaryID
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5923ff0ff0545f1feb769973f2528bd82e351e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419663"
---
# <a name="wmmediaclasssecondaryid"></a>WM/MediaClassSecondaryID

El atributo **WM/MediaClassSecondaryID** contiene el GUID de la clase multimedia secundaria.

## <a name="global-constant"></a>Constante global

g \_ wszWMMediaClassSecondaryID

## <a name="data-type"></a>Tipo de datos

**\_GUID de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Este atributo debe establecerse en uno de los valores de la tabla siguiente.



| GUID de clase secundaria                   | Descripción                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "E0236BEB-C281-4EDE-A36D-7AF76A3D45B5" | Se usa para los archivos de libro de audio.                                                                                                                                                               |
| "3A172A13-2BD9-4831-835B-114F6A95943F" | Se usa para los archivos de audio que contienen la palabra oral, pero no los libros de audio. Por ejemplo, las rutinas de comedia de los servidores.                                                                           |
| "6677DB9B-E5A0-4063-A1AD-ACEB52840CF1" | Se usa para los archivos de audio relacionados con las noticias.                                                                                                                                                    |
| "1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B" | Se usa para los archivos de audio con la conversación Mostrar contenido.                                                                                                                                             |
| "1FE2E091-4E1E-40CE-B22D-348C732E0B10" | Se usa para archivos de vídeo relacionados con las noticias.                                                                                                                                                    |
| "D6DE1D88-C77C-4593-BFBC-9C61E8C373E3" | Se usa para archivos de vídeo que contienen presentaciones basadas en Web, películas cortas, finalizadores de películas, etc. Este es el identificador general para el entretenimiento de vídeo que no encaja en otra categoría. |
| "00033368-5009-4AC3-A820-5D2D09A4E7C1" | Se usa para archivos de audio que contienen clips de sonido de juegos.                                                                                                                                  |
| "F24FF731-96FC-4D0F-A2F5-5A3483682B1A" | Se usa para archivos de audio que contienen canciones completas de pistas de sonido de juegos. Si solo parte de una canción está codificada en el archivo, use en su lugar el identificador de los clips de sonido del juego.                   |
| "E3E689E2-BA8C-4330-96DF-A0EEEFFA6876" | Se usa para archivos de vídeo que contienen vídeos musicales.                                                                                                                                            |
| "B76628F4-300D-443D-9CB5-01C285109DAF" | Se usa para archivos de vídeo que contienen vídeos de inicio generales.                                                                                                                                      |
| "A9B87FC9-BD47-4BF0-AC4F-655B89F7D868" | Se usa para archivos de vídeo que contienen películas de características.                                                                                                                                           |
| "BA7F258A-62F7-47A9-B21F-4651C42A000E" | Se usa para archivos de vídeo que contienen programas de televisión. En el caso de las presentaciones basadas en Web, use el identificador más genérico.                                                                                  |
| "44051B5B-B103-4B5C-92AB-93060A9463F0" | Se usa para los archivos de vídeo que contienen vídeos corporativos. Por ejemplo, reuniones grabadas o vídeos de aprendizaje.                                                                                      |
| "0B710218-8C0C-475E-AF73-4C41C0C8F8CE" | Use para archivos de vídeo que contengan vídeo en casa procedente de fotografías.                                                                                                                        |



 

Al especificar un identificador de clase secundaria, el archivo también debe contener un atributo de identificador de clase principal.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassPrimaryID**](wm-mediaprimaryid.md)
</dt> </dl>

 

 




