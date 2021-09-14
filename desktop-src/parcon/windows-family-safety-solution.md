---
description: Windows Solución de seguridad para familias
ms.assetid: b89cf0c7-bf9f-4bcb-b008-8b7c792f3300
title: Windows Solución de seguridad para familias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2d8776893468df4f4877c7220436f505ab1e6f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268439"
---
# <a name="windows-family-safety-solution"></a>Windows Solución de seguridad para familias

Los requisitos clave definidos por Microsoft para una solución más completa son los siguientes. Tenga en cuenta que la definición de en línea es una tecnología orientada principalmente a Internet, a diferencia de un cliente sin conexión que normalmente está limitado en el equipo.

-   Proporcione un área única y fácil de encontrar en la interfaz de usuario del sistema operativo donde se puedan detectar fácilmente todas las directivas de controles parentales, el control de la supervisión de la actividad y los datos de actividad de una identidad.

-   Permite supervisar la actividad suficiente del usuario controlado para que un elemento primario o guardián tenga una confianza razonable de que se puedan detectar actividades de riesgo. Además, se puede detectar la reconfiguración de registros de las directivas del usuario controlado para que se puedan detectar cambios no deseados o no autorizados.

-   Exponga las funcionalidades de supervisión de la actividad Windows las interfaces de registro de eventos de Vista y proporcione una solución de visor integrada. Defina eventos de actividad estándar y proporcione extensibilidad a la generación de eventos personalizados por isv.

-   Promueva que todas las restricciones y la supervisión de un usuario estén activadas solo de forma opt-in por parte de los padres o guardianes. Siempre que sea posible, la funcionalidad de restricciones debe estar completamente inactiva para que los usuarios no controlados minimicen los riesgos de compatibilidad de aplicaciones y seguridad.

-   Microsoft se esfuerza, siempre que sea posible, por no tomar decisiones de valor por edad u otros parámetros para el usuario controlado (es posible que terceros decidan hacerlo). Estas decisiones las deja el primario o el guardián, a menudo influenciados por comunidades u organizaciones.

-   Proporcione implementaciones en el producto para la supervisión de la actividad sin conexión y restricciones en las que actualmente hay pocas ofertas disponibles, donde la funcionalidad de riesgo de seguridad asociada está disponible en el producto o donde una solución de Microsoft proporciona funcionalidad capaz y sólida totalmente integrada con el diseño del sistema operativo.

-   Por lo general, promueva que las aplicaciones realicen su propio registro y restricciones para obtener el mejor contexto y experiencia de interfaz de usuario.

    Excepción: proporcione restricciones y supervisión completa de la actividad en línea en áreas seleccionadas en las que las ventajas para los consumidores y el sector superan los costos.

-   Exponga la configuración de la interfaz de usuario de los controles parentales y las definiciones de eventos de actividad mediante las API públicas para que terceros puedan consultar el estado, modificar la configuración y leer los registros de actividad si se ejecutan con suficientes privilegios de Windows cuenta.

Un objetivo general es promover la coexistencia de las soluciones de controles parentales de terceros con la funcionalidad integrada y admitir la adición de valor mediante la integración, la ampliación o el suministro de funcionalidades alternativas cuando sea adecuado.

 

 



