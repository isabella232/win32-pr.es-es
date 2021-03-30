---
title: Probar una interfaz de usuario
description: En esta sección se describen detalladamente algunas de las tareas asociadas a la prueba de una interfaz de usuario para una aplicación Windows.
ms.assetid: d628e530-7a0b-4a8d-9a9f-253aec275fa9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e86282c03502642541c0ea1318b8ccaf6d16b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995545"
---
# <a name="testing-a-user-interface"></a>Probar una interfaz de usuario

En esta sección se describen detalladamente algunas de las tareas asociadas a la prueba de una interfaz de usuario para una aplicación Windows.

-   [Introducción](#introduction)
-   [Pruebas de facilidad de uso](#usability-testing)
-   [Pruebas de accesibilidad](#accessibility-testing)

## <a name="introduction"></a>Introducción

Para determinar por completo la eficacia y la facilidad de uso general de una interfaz de usuario de la aplicación, se debe probar. La prueba expone lo fácil o difícil que la interfaz de usuario puede usar para el público más amplio posible. El tiempo que se tarda en probar una aplicación es una buena pena.

Este tema se centra en tres escenarios de prueba principales: facilidad de uso general, accesibilidad y automatización.

## <a name="usability-testing"></a>Pruebas de facilidad de uso

Las pruebas de facilidad de uso proporcionan la oportunidad de evaluar un producto estudiando el modo en que los usuarios reales usan el producto. Este análisis garantiza que las suposiciones clave sobre los usuarios previstos y los diseños de interfaz se admiten (o se desafian) con datos reales. Solo mediante la recopilación de estos datos empíricos puede averiguar el grado en que la interfaz de usuario de un producto se adapta a las necesidades y expectativas de los usuarios.

Al observar la interacción del usuario con el producto y escuchar los comentarios de los usuarios, se identifican las características importantes que pueden ser difíciles de encontrar y usar. En función de estos resultados, se pueden realizar ajustes en la interfaz de usuario según sea necesario. Es casi imposible crear un producto útil sin cierto nivel de pruebas de facilidad de uso, ya que los resultados proporcionan la base para tomar mejores decisiones sobre el producto y mejorar la experiencia de usuario global.

Las pruebas de facilidad de uso proporcionan una amortización significativa solo cuando está bien integrada en todo el ciclo de vida del proyecto. Un estudio de facilidad de uso único puede identificar problemas, pero sin pruebas de seguimiento, es difícil determinar si las soluciones han resuelto esos problemas o se han introducido nuevos.

Los escenarios principales para las pruebas de facilidad de uso son:

-   Si es un proveedor de productos de software, la prueba de usuarios reales de su producto significa que está evaluando el diseño. En función de cómo haya diseñado la aplicación, ¿pueden completar los usuarios las tareas que necesitan? La prueba de los usuarios reales que realizan tareas reales también puede señalar si las instrucciones de la interfaz de usuario que está siguiendo están trabajando en el contexto de su producto y cuando la coherencia ayuda o entorpece la capacidad de un usuario para realizar su trabajo.
-   Si es un comprador de productos de software, puede realizar pruebas de facilidad de uso para evaluar un producto para su compra. Por ejemplo, su empresa puede considerar la posibilidad de comprar un producto para sus empleados de 20000. Antes de que la empresa dedique su dinero, desea asegurarse de que el producto en cuestión ayudará realmente a los empleados a mejorar su trabajo. Las pruebas de facilidad de uso también pueden ser útiles para ver si la aplicación propuesta sigue las directrices de estilo de la interfaz de usuario publicadas (interno o externo). Es mejor usar las directrices de la interfaz de usuario como origen de información auxiliar, en lugar de principal, para tomar decisiones de compra.

Para obtener más información, consulte [facilidad de uso en la práctica: pruebas de facilidad de uso](/archive/msdn-magazine/2009/brownfield/usability-in-practice-usability-testing).

## <a name="accessibility-testing"></a>Pruebas de accesibilidad

Las pruebas de accesibilidad abarcan dos áreas de un diseño de la interfaz de usuario: compatibilidad con usuarios con discapacidades y acceso mediante programación mediante marcos de pruebas automatizadas.

Asegurarse de que una aplicación sea accesible para los usuarios con discapacidades implica probar lo siguiente:

-   Cumplimiento: ¿cumple la aplicación los distintos requisitos legales relacionados con la accesibilidad?
-   Eficacia: ¿pueden los usuarios con discapacidades usar la aplicación?
-   Utilidad: ¿la aplicación expone la funcionalidad adecuada para los usuarios con discapacidades?
-   Satisfacción: ¿cómo percibe la aplicación los usuarios con discapacidades?

La comprobación de estos aspectos de una aplicación se puede realizar a través de una auditoría de accesibilidad, que implica una revisión manual de la aplicación por parte de un experto en accesibilidad y un estudio de facilidad de uso centrado en los usuarios deshabilitados y los dispositivos de tecnología de asistencia.

Aunque aparentemente no está relacionado, existe una estrecha correlación entre los requisitos de acceso mediante programación de marcos de pruebas automatizadas y los dispositivos de tecnología de asistencia. La compatibilidad con uno tiene la ventaja adicional de habilitar el otro. Para obtener más información sobre la automatización de la accesibilidad y la prueba en aplicaciones Windows, vea [accesibilidad](/windows/desktop/accessibility), [herramientas de prueba](/windows/desktop/WinAuto/testing-tools)y la API de [automatización de Windows](/windows/desktop/WinAuto/windows-automation-api-portal).

 

 