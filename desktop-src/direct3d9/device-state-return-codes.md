---
description: Lista de algunos de los códigos de retorno posibles para métodos y funciones.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6cd860fcc8268bf2b63a9498b9960da359ca210
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999342"
---
# <a name="s_present"></a>S \_ PRESENT

Lista de algunos de los códigos de retorno posibles para métodos y funciones.



| \#Definir                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ OK                     | El dispositivo se ejecuta con normalidad y se puede usar para la representación.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| S \_ PRESENT \_ OCCLUDED      | El área de presentación está ocluida. La oclusión significa que la ventana de presentación se minimiza o que otro dispositivo entra en el modo de pantalla completa en el mismo monitor que la ventana de presentación y la ventana de presentación está completamente en ese monitor. La oclusión no se producirá si el área de cliente está cubierta por otra ventana.<br/> Las aplicaciones con ocluida pueden continuar con la representación y todas las llamadas se realizarán correctamente, pero la ventana de presentación concluida no se actualizará. Preferiblemente, la aplicación debe dejar de representarse en la ventana de presentación mediante el dispositivo y seguir llamando a [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) hasta que se devuelva \_ S OK o S PRESENT MODE \_ \_ \_ CHANGED.<br/> |
| SE HA \_ CAMBIADO \_ EL MODO \_ ACTUAL | Se ha cambiado el modo de presentación del escritorio. La aplicación puede continuar con la representación, pero puede haber conversión o extensión de color. Elija un formato de búfer de reserva similar al modo de presentación actual y llame a Reset para volver a crear las cadenas de intercambio. El dispositivo dejará este estado después de llamar a Un restablecimiento.                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Otros códigos de error están contenidos en [D3DERR.](d3derr.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




