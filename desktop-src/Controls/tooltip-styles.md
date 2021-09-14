---
title: Estilos de información sobre herramientas (CommCtrl.h)
description: En esta sección se enumeran los estilos de control usados con controles de información sobre herramientas.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165994"
---
# <a name="tooltip-styles"></a>Estilos de información sobre herramientas

En esta sección se enumeran los estilos de control usados con controles de información sobre herramientas.



| Constante                                                                                                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <dt>**TTS \_ ALWAYSTIP**</dt> </dl>                | Indica que el control de información sobre herramientas aparece cuando el cursor está en una herramienta, incluso si la ventana de propietario del control de información sobre herramientas está inactiva. Sin este estilo, la información sobre herramientas solo aparece cuando la ventana de propietario de la herramienta está activa.<br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <dt>**GLOBO \_ DE TTS**</dt> </dl>                      | [Versión 5.80.](common-control-versions.md) Indica que el control de información sobre herramientas tiene la apariencia de un "globo" con esquinas redondeadas y una lemat que apunta al elemento. <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <dt>**TTS \_ CLOSE**</dt> </dl>                            | Muestra un **botón Cerrar** en la información sobre herramientas. Solo es válida cuando la información sobre herramientas tiene el estilo \_ TTS BALLOON y un título; vea [**\_ SETTITLE de TTM.**](ttm-settitle.md)<br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <dt>**TTS \_ NOANIMATE**</dt> </dl>                | [Versión 5.80.](common-control-versions.md) Deshabilita la animación de información sobre herramientas deslizante Windows 98 y Windows 2000. Este estilo se omite en sistemas anteriores.<br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <dt>**TTS \_ NOFADE**</dt> </dl>                         | [Versión 5.80.](common-control-versions.md) Deshabilita la animación de información sobre herramientas de desvanecha. <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <dt>**TTS \_ NOPREFIX**</dt> </dl>                   | Impide que el sistema quita caracteres de yerras de una cadena o termina una cadena en un carácter de tabulación. Sin este estilo, el sistema quita automáticamente los caracteres de y comercial y finaliza una cadena en el primer carácter de tabulación. Esto permite que una aplicación use la misma cadena que un elemento de menú y como texto en un control de información sobre herramientas.<br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <dt>**TTS \_ USEVISUALSTYLE**</dt> </dl> | Usa hipervínculos con formato. El tema definirá los estilos de los vínculos de la información sobre herramientas. Este estilo siempre requiere que se \_ establezca TTF PARSELINKS. <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a>Observaciones

Un control de información sobre herramientas siempre tiene los estilos de ventana WS POPUP y \_ WS EX TOOLWINDOW, independientemente de si se especifican \_ \_ al crear el control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





