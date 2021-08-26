---
description: Puede supervisar las estadísticas de objetos a medida que se ejecuta una aplicación. Al hacerlo, puede ajustar las características del grupo de objetos para lograr el equilibrio entre rendimiento y recursos que le gustaría tener.
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: Supervisión de estadísticas de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e58946953ef1688dcb44223522cc58ccd1195f07ec0173a0b75413fe441195f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070474"
---
# <a name="monitoring-object-statistics"></a>Supervisión de estadísticas de objetos

Puede supervisar las estadísticas de objetos a medida que se ejecuta una aplicación. Al hacerlo, puede ajustar las características del grupo de objetos para lograr el equilibrio entre rendimiento y recursos que le gustaría tener.

Puede supervisar el estado de los objetos configurados para admitir estadísticas de objetos e informes de eventos. La habilitación de las estadísticas de objetos tiene una sobrecarga de rendimiento muy ligera.

**Para habilitar las estadísticas de objetos**

1.  En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón derecho en el componente que desea configurar y, a continuación, haga clic en **Propiedades**.

2.  En el cuadro de diálogo propiedades del componente, haga clic en **la pestaña** Activación .

3.  Para habilitar las estadísticas de objetos para el componente, en **Contexto de activación**, active la casilla Componente admite eventos y **estadísticas.**

**Para supervisar el estado del objeto**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, abra la carpeta de la aplicación que incluye los componentes que desea supervisar.

2.  Haga clic con el botón derecho en **la carpeta Componentes,** seleccione **Ver** y, a continuación, haga clic en Vista **de estado**. El panel de detalles muestra ahora la vista de estado de todos los componentes de la aplicación. En la tabla siguiente se describen las seis columnas de la vista de estado.

    

    | Columna                        | Descripción                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **ProgID**<br/>         | Identifica un componente específico.<br/>                                                                                                                                                                                |
    | **Objects**<br/>        | Muestra el número de objetos que están retenidos actualmente por las referencias de cliente.<br/>                                                                                                                                       |
    | **Activado**<br/>      | Muestra el número de objetos que están activados actualmente. <br/>                                                                                                                                                      |
    | **Combinado**<br/>         | Muestra el número total de objetos creados por el grupo, incluidos los objetos que están en uso y los objetos que están desactivados.<br/>                                                                                      |
    | **In Call**<br/>        | Identifica los objetos de la llamada.<br/>                                                                                                                                                                                     |
    | **Tiempo de llamada (ms)**<br/> | Muestra la duración media de la llamada (en milisegundos) de las llamadas de método realizadas en los últimos 20 segundos (hasta 20 llamadas). El tiempo de llamada se mide en el objeto y no incluye el tiempo usado para atravesar la red.<br/> |

    

     

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de un componente que se va a agrupar](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




