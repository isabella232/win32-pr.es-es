---
title: Propiedades (IInertiaProcessor)
description: Esta sección contiene las propiedades de la interfaz IInertiaProcessor.
ms.assetid: 47fd1a49-8e14-4076-8ce6-f0c4917e8cf1
keywords:
- Windows Touch, interfaz IInertiaProcessor
- Windows Touch, propiedades de la interfaz
- inercia, interfaz IInertiaProcessor
- Interfaz IInertiaProcessor, propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab3e1754c7b723b4be446e82fd0ba39fc67af5d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421741"
---
# <a name="properties-iinertiaprocessor"></a>Propiedades (IInertiaProcessor)

Esta sección contiene las propiedades de la interfaz [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .



| Propiedad                                                                               | Descripción                                                                                               |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**InitialOriginX**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginx)                             | Especifica la ubicación horizontal inicial de un destino con Intercia.                                   |
| [**InitialOriginY**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginy)                             | Especifica la ubicación vertical inicial de un destino con Intercia.                                     |
| [**InitialVelocityX**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityx)                         | Especifica el movimiento inicial del objeto de destino en el eje horizontal.                              |
| [**InitialVelocityY**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityy)                         | Especifica el movimiento inicial del objeto de destino en el eje vertical.                                |
| [**InitialAngularVelocity**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialangularvelocity)             | Especifica la velocidad de rotación del destino cuando comienza el movimiento.                                    |
| [**InitialExpansionVelocity**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialexpansionvelocity)         | Especifica la velocidad de expansión RADIUS del destino cuando comienza el movimiento.                               |
| [**InitialRadius**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialradius)                               | Especifica la distancia desde el borde del destino hasta su centro antes de que se cambiara el objeto.          |
| [**BoundaryLeft**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryleft)                                 | Limita el desplazamiento hacia la izquierda de la pantalla que el objeto de destino puede desplazar.                                 |
| [**BoundaryTop**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarytop)                                   | Limita hasta qué punto de la pantalla se puede desplazar el objeto de destino.                                  |
| [**BoundaryRight**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryright)                               | Limita el grado de distancia hacia el lado derecho de la pantalla que puede moverse el objeto de destino.                           |
| [**BoundaryBottom**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarybottom)                             | Limita hasta qué parte de la parte inferior de la pantalla se puede desplazar el objeto de destino.                               |
| [**ElasticMarginLeft**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginleft)                       | Especifica la región más a la izquierda para rebotar el objeto de destino.                                            |
| [**ElasticMarginTop**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmargintop)                         | Especifica la región de nivel superior para rebotar el objeto de destino.                                             |
| [**ElasticMarginRight**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginright)                     | Especifica la región más a la derecha para rebotar el objeto de destino.                                           |
| [**ElasticMarginBottom**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginbottom)                   | Especifica la región inferior para rebotar el objeto de destino.                                              |
| [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration)     | Especifica la tasa deseada en la que el objeto de destino detendrá el giro en radianes por milisegundos.                |
| [**DesiredRotation**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredrotation)                           | Especifica la distancia deseada (en radianes) que el procesador de inercia manipulará un objeto. |
| [**DesiredExpansion**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansion)                         | Especifica el cambio deseado en el radio medio del objeto.                                        |
| [**DesiredExpansionDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansiondeceleration) | Especifica la velocidad a la que el objeto dejará de expandirse.                                              |
| [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)                   | Especifica la velocidad deseada a la que se ralentizarán las operaciones de traducción.                              |
| [**DesiredDisplacement**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddisplacement)                   | Especifica la distancia deseada a la que se desplazará el objeto.                                              |
| [**InitialTimestamp**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialtimestamp)                         | Especifica la marca de tiempo de inicio para un objeto de destino que tiene inercia.                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




