---
description: Puede supervisar las estadísticas de objetos a medida que se ejecuta una aplicación. Al hacerlo, puede ajustar las características del grupo de objetos para lograr el equilibrio en el rendimiento y los recursos que desea tener.
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: Supervisión de estadísticas de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f438bc7081546083f1930fe31f16a2198b09b48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360039"
---
# <a name="monitoring-object-statistics"></a>Supervisión de estadísticas de objetos

Puede supervisar las estadísticas de objetos a medida que se ejecuta una aplicación. Al hacerlo, puede ajustar las características del grupo de objetos para lograr el equilibrio en el rendimiento y los recursos que desea tener.

Puede supervisar el estado de los objetos configurados para admitir las estadísticas de objetos y los informes de eventos. Habilitar las estadísticas de objetos tiene una pequeña sobrecarga de rendimiento.

**Para habilitar las estadísticas de objetos**

1.  En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en el componente que desee configurar y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **activación** .

3.  Para habilitar las estadísticas de objetos para el componente, en **contexto de activación**, active la casilla el **componente admite eventos y estadísticas** .

**Para supervisar el estado de los objetos**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, abra la carpeta de la aplicación que incluye los componentes que desea supervisar.

2.  Haga clic con el botón secundario en la carpeta **componentes** , elija **Ver** y, a continuación, haga clic en **vista estado**. En el panel de detalles se muestra ahora la vista de estado de todos los componentes de la aplicación. En la tabla siguiente se describen las seis columnas de la vista de estado.

    

    | Columna                        | Descripción                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **ProgID**<br/>         | Identifica un componente específico.<br/>                                                                                                                                                                                |
    | **Objects**<br/>        | Muestra el número de objetos que se encuentran actualmente en referencias de cliente.<br/>                                                                                                                                       |
    | **Desactiva**<br/>      | Muestra el número de objetos que están activados actualmente. <br/>                                                                                                                                                      |
    | **Agrupados**<br/>         | Muestra el número total de objetos creados por el grupo, incluidos los objetos que están en uso y los objetos que están desactivados.<br/>                                                                                      |
    | **En la llamada**<br/>        | Identifica los objetos de la llamada.<br/>                                                                                                                                                                                     |
    | **Tiempo de llamada (MS)**<br/> | Muestra la duración media de la llamada (en milisegundos) de las llamadas a métodos realizadas en los últimos 20 segundos (hasta 20 llamadas). El tiempo de llamada se mide en el objeto y no incluye el tiempo usado para atravesar la red.<br/> |

    

     

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de un componente que se va a agrupar](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




