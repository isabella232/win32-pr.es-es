---
title: Estilos de información sobre herramientas (CommCtrl. h)
description: En esta sección se enumeran los estilos de control utilizados con controles ToolTip.
ms.assetid: a6aeac71-6a69-4903-af78-0bfe1f83e632
topic_type:
- apiref
api_name:
- TTS_ALWAYSTIP
- TTS_BALLOON
- TTS_CLOSE
- TTS_NOANIMATE
- TTS_NOFADE
- TTS_NOPREFIX
- TTS_USEVISUALSTYLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8b89aed88caddceae815414b9f2b4d93a550c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649684"
---
# <a name="tooltip-styles"></a>Estilos de información sobre herramientas

En esta sección se enumeran los estilos de control utilizados con controles ToolTip.



| Constante                                                                                                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <dt>**ALWAYSTIP de TTS \_**</dt> </dl>                | Indica que el control de información sobre herramientas aparece cuando el cursor está en una herramienta, incluso si la ventana propietaria del control de información sobre herramientas está inactiva. Sin este estilo, la información sobre herramientas solo aparece cuando la ventana propietaria de la herramienta está activa.<br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <dt>**globo de TTS \_**</dt> </dl>                      | [Versión 5,80](common-control-versions.md). Indica que el control ToolTip tiene la apariencia de un "globo" animado, con esquinas redondeadas y un tallo que apunta al elemento. <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <dt>**\_cerrar TTS**</dt> </dl>                            | Muestra un botón **cerrar** en la información sobre herramientas. Solo es válido cuando la información sobre herramientas tiene el \_ estilo de globo TTS y un título; vea [**TTM \_ SETTITLE**](ttm-settitle.md).<br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <dt>**TTS \_ NOanimate**</dt> </dl>                | [Versión 5,80](common-control-versions.md). Deshabilita la animación deslizante de la información sobre herramientas en los sistemas Windows 98 y Windows 2000. Este estilo se omite en sistemas anteriores.<br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <dt>**TTS \_ NOdesvanecese**</dt> </dl>                         | [Versión 5,80](common-control-versions.md). Deshabilita la animación de la información sobre herramientas de atenuación. <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <dt>**TTS \_ NOprefix**</dt> </dl>                   | Impide que el sistema elimine los caracteres de y comercial de una cadena o que termine una cadena en un carácter de tabulación. Sin este estilo, el sistema quita los caracteres de y comercial automáticamente y termina una cadena en el primer carácter de tabulación. Esto permite que una aplicación use la misma cadena como un elemento de menú y como texto en un control de información sobre herramientas.<br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <dt>**USEVISUALSTYLE de TTS \_**</dt> </dl> | Utiliza hipervínculos con los mismos. El tema definirá los estilos para los vínculos de la información sobre herramientas. Este estilo siempre requiere \_ que se establezca ttf PARSELINKS. <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a>Observaciones

Un control de información sobre herramientas siempre tiene los \_ estilos del elemento emergente WS y \_ de la \_ ventana de la ventana de herramientas de WS ex, independientemente de si se especifican al crear el control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





