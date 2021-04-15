---
title: Constantes (referencia de animación de Windows)
description: Documentación de referencia para las constantes y enumeraciones definidas por el administrador de animaciones de Windows.
ms.assetid: c590cf68-28ce-4d7d-949d-2683ece3c12d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2cceae981ea7cc0e2b78d9dadbea88075eb3ad
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105676535"
---
# <a name="constants-windows-animation-reference"></a>Constantes (referencia de animación de Windows)

Documentación de referencia para las constantes y enumeraciones definidas por el administrador de animaciones de Windows.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                             | Descripción                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**dimensión de animación de IU \_ \_ \_ desconocida**](ui-animation-dimension-unknown.md)<br/>                                            | Indica que no se puede recuperar la dimensión solicitada.<br/>                                                                                                                                                                                                     |
| [**\_iteración de animación de IU \_ \_ ninguno**](-ui-animation-iteration-none.md)<br/>                                                 | Indica que esta es la entrada inicial en un bucle determinado.<br/>                                                                                                                                                                                                     |
| [**\_Inicio de \_ \_ guion gráfico \_ de animación de IU**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85))<br/>                           | Representa el fotograma clave implícito al principio de cada guion gráfico.<br/>                                                                                                                                                                                              |
| [**animación de IU \_ \_ repetir \_ indefinidamente**](ui-animation-repeat-indefinitely.md)<br/>                                        | Indica que el intervalo entre dos fotogramas clave de un guión gráfico debe repetirse indefinidamente hasta que se llame al método [**IUIAnimationStoryboard:: concluir**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) .<br/>                                                            |
| [**la \_ animación de la interfaz de usuario se \_ repite \_ indefinidamente \_ \_ al \_ final**](ui-animation-repeat-indefinitely-conclude-at-end.md)<br/>     | Indica que el intervalo entre dos fotogramas clave de un guión gráfico debe repetirse indefinidamente hasta que el bucle de fotogramas clave finaliza en el fotograma clave final cuando se llama al método [**IUIAnimationStoryboard:: concluir**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) .<br/>   |
| [**la \_ animación de la interfaz de usuario se \_ repite \_ indefinidamente \_ \_ al \_ principio**](ui-animation-repeat-indefinitely-conclude-at-start.md)<br/> | Indica que el intervalo entre dos fotogramas clave de un guión gráfico debe repetirse indefinidamente hasta que el bucle de fotogramas clave finaliza en el fotograma clave inicial cuando se llama al método [**IUIAnimationStoryboard:: concluir**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) .<br/> |
| [**\_segundos de animación de la interfaz de usuario \_ \_**](ui-animation-seconds-eventually.md)<br/>                                          | Indica que la animación de Windows puede retrasar el inicio programado de un guión gráfico en tanto tiempo como sea necesario para evitar conflictos de programación.<br/>                                                                                                                     |
| [**segundos de animación de interfaz de usuario \_ \_ \_ infinitos**](ui-animation-seconds-infinite.md)<br/>                                              | Indica que no hay ningún evento programado.<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de animación de Windows](windows-animation-reference.md)
</dt> </dl>

 

