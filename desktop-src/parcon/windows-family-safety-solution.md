---
description: Solución de seguridad para la familia Windows
ms.assetid: b89cf0c7-bf9f-4bcb-b008-8b7c792f3300
title: Solución de seguridad para la familia Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2d8776893468df4f4877c7220436f505ab1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649256"
---
# <a name="windows-family-safety-solution"></a>Solución de seguridad para la familia Windows

Los requisitos clave definidos por Microsoft para una solución más completa son los siguientes. Tenga en cuenta que la definición de en línea es una tecnología principalmente orientada a Internet, a diferencia de un cliente sin conexión que normalmente está limitado en el equipo.

-   Proporcionan un área única y fácil de encontrar en la interfaz de usuario del sistema operativo donde se pueden detectar fácilmente todas las directivas de controles parentales, el control de la supervisión de la actividad y los datos de actividad de una identidad.

-   Admitir la supervisión de la actividad suficiente del usuario controlado para que un padre o tutor tenga una confianza razonable de que se puedan detectar actividades de riesgo. Además, registre la reconfiguración de las directivas del usuario controlado para que los cambios no deseados o no autorizados sean reconocibles.

-   Exponga las capacidades de supervisión de actividades a través de las interfaces estándar de registro de eventos de Windows Vista y proporcione una solución de visor integrada. Defina los eventos de actividad estándar y proporcione extensibilidad a la generación de eventos personalizados por parte de los ISV.

-   Promueva que toda la supervisión y las restricciones de un usuario se activen solo en función de los padres o tutores. Siempre que sea posible, la funcionalidad de restricciones debe estar completamente inactiva para los usuarios no controlados con el fin de minimizar los riesgos de seguridad y compatibilidad de aplicaciones.

-   Microsoft procurará, siempre que sea posible, no realizar resoluciones de valor por edad u otros parámetros para el usuario controlado (es posible que otros fabricantes decidan hacerlo). Dichas decisiones se dejan al padre o a la protección, que a menudo se ven afectadas por comunidades u organizaciones.

-   Proporcionar implementaciones en el producto para la supervisión de actividades sin conexión y las restricciones en las que las ofertas o no están disponibles hoy en día, donde la funcionalidad de riesgo de seguridad asociada está disponible en el producto, o en los casos en los que una solución de Microsoft proporciona una funcionalidad compatible y sólida totalmente integrada con el diseño del sistema operativo.

-   Por lo general, promueva que las aplicaciones realicen sus propios registros y restricciones para obtener una mejor experiencia de contexto y de interfaz de usuario.

    Excepción: proporcione una supervisión y restricciones completas de la actividad en línea en áreas seleccionadas en las que la ventaja de los consumidores y del sector supere los costos.

-   Exponga la configuración de la interfaz de usuario de controles parentales y las definiciones de eventos de actividad mediante el uso de API públicas para que otros usuarios puedan consultar el estado, modificar la configuración y leer los registros de actividad si se ejecutan con suficientes privilegios de cuenta de Windows.

Un objetivo general es promover la coexistencia de soluciones de controles parentales de terceros con la funcionalidad integrada y permitir agregar valor mediante la integración con, la extensión o el suministro de funcionalidades alternativas cuando sea adecuado.

 

 



