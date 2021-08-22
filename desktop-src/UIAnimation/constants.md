---
title: Constantes (referencia Windows animación)
description: Documentación de referencia de las constantes y enumeraciones definidas por el administrador Windows Animation Manager.
ms.assetid: c590cf68-28ce-4d7d-949d-2683ece3c12d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23964a2936b3879d551bcde9c2c25c2d63465e1cb4afb07cee25a3ce74a2a57f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419143"
---
# <a name="constants-windows-animation-reference"></a>Constantes (referencia Windows animación)

Documentación de referencia de las constantes y enumeraciones definidas por el administrador Windows Animation Manager.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                             | Descripción                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DIMENSIÓN DE \_ ANIMACIÓN DE INTERFAZ DE USUARIO \_ \_ DESCONOCIDA**](ui-animation-dimension-unknown.md)<br/>                                            | Indica que no se puede recuperar la dimensión solicitada.<br/>                                                                                                                                                                                                     |
| [**\_ITERACIÓN DE ANIMACIÓN DE INTERFAZ DE USUARIO \_ \_ NONE**](-ui-animation-iteration-none.md)<br/>                                                 | Indica que se trata de la entrada inicial en un bucle determinado.<br/>                                                                                                                                                                                                     |
| [**INICIO DEL \_ GUIÓN \_ GRÁFICO DE \_ FOTOGRAMAS CLAVE DE ANIMACIÓN DE LA \_ INTERFAZ DE USUARIO**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85))<br/>                           | Representa el fotograma clave implícito al principio de cada guión gráfico.<br/>                                                                                                                                                                                              |
| [**LA \_ ANIMACIÓN DE LA INTERFAZ DE USUARIO SE REPITE \_ \_ INDEFINIDAMENTE**](ui-animation-repeat-indefinitely.md)<br/>                                        | Indica que el intervalo entre dos fotogramas clave de un guión gráfico debe repetirse indefinidamente hasta que se llame al método [**IUIAnimationStoryboard::Conclude.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude)<br/>                                                            |
| [**LA \_ ANIMACIÓN DE LA INTERFAZ DE USUARIO SE REPITE \_ \_ INDEFINIDAMENTE Y CONCLUYE AL \_ \_ \_ FINAL**](ui-animation-repeat-indefinitely-conclude-at-end.md)<br/>     | Indica que el intervalo entre dos fotogramas clave de un guión gráfico debe repetirse indefinidamente hasta que el bucle de fotogramas clave finalice en el fotograma clave final cuando se llame al método [**IUIAnimationStoryboard::Conclude.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude)<br/>   |
| [**LA \_ ANIMACIÓN DE LA INTERFAZ DE USUARIO SE REPITE \_ \_ INDEFINIDAMENTE Y CONCLUYE AL \_ \_ \_ PRINCIPIO**](ui-animation-repeat-indefinitely-conclude-at-start.md)<br/> | Indica que el intervalo entre dos fotogramas clave de un guión gráfico debe repetirse indefinidamente hasta que el bucle de fotogramas clave finalice en el fotograma clave inicial cuando se llame al método [**IUIAnimationStoryboard::Conclude.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude)<br/> |
| [**FINALMENTE, \_ LOS SEGUNDOS DE ANIMACIÓN DE LA INTERFAZ DE \_ \_ USUARIO**](ui-animation-seconds-eventually.md)<br/>                                          | Indica que Windows animación puede retrasar el inicio programado de un guión gráfico durante el tiempo necesario para evitar conflictos de programación.<br/>                                                                                                                     |
| [**SEGUNDOS \_ INFINITOS DE \_ ANIMACIÓN DE INTERFAZ \_ DE USUARIO**](ui-animation-seconds-infinite.md)<br/>                                              | Indica que no hay ningún evento programado.<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Referencia de animación](windows-animation-reference.md)
</dt> </dl>

 

