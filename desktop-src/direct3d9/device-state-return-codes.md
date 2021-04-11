---
description: Una lista de algunos de los códigos de retorno posibles para métodos y funciones.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4146a65e9092dcd3fed261c127e84fe8552128a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274688"
---
# <a name="s_present"></a>S \_ presentes

Una lista de algunos de los códigos de retorno posibles para métodos y funciones.



|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#define                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| S \_ correcto                     | El dispositivo se está ejecutando con normalidad y se puede usar para la representación.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| S \_ presente \_ ocluidos      | El área de presentación es ocluidos. La oclusión significa que la ventana de presentación está minimizada u otro dispositivo entró en el modo de pantalla completa en el mismo monitor que la ventana de presentación y la ventana de presentación está completamente en ese monitor. La oclusión no se producirá si el área de cliente está incluida en otra ventana.<br/> Las aplicaciones ocluidos pueden continuar la representación y todas las llamadas se realizarán correctamente, pero la ventana de presentación ocluidos no se actualizará. Preferiblemente, la aplicación debe dejar de representar la representación en la ventana de presentación mediante el dispositivo y mantener la llamada a [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) hasta que se cambie el modo de presentación de s \_ o el \_ \_ modo present \_ .<br/> |
| \_modo present \_ \_ cambiado | Se ha cambiado el modo de presentación del escritorio. La aplicación puede continuar con la representación, pero puede haber conversión o ajuste de color. Elija un formato de búfer de reserva similar al modo de presentación actual y llame a restablecer para volver a crear las cadenas de intercambio. El dispositivo dejará este estado después de que se llame a RESET.                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Otros códigos de error se encuentran en [D3DERR](d3derr.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




