---
title: Prueba de un Interfaz de usuario
description: En esta sección se describen en detalle algunas de las tareas asociadas a la prueba de una interfaz de usuario para Windows aplicación.
ms.assetid: d628e530-7a0b-4a8d-9a9f-253aec275fa9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f3d6686cdcd892aa5608944cf8c1a20df0d44106a0fdac01b2bbbd855fe523
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507444"
---
# <a name="testing-a-user-interface"></a>Prueba de un Interfaz de usuario

En esta sección se describen en detalle algunas de las tareas asociadas a la prueba de una interfaz de usuario para Windows aplicación.

-   [Introducción](#introduction)
-   [Pruebas de facilidad de uso](#usability-testing)
-   [Pruebas de accesibilidad](#accessibility-testing)

## <a name="introduction"></a>Introducción

Para determinar completamente la eficacia y facilidad de uso general de una interfaz de usuario de aplicación, se debe probar. Las pruebas exponen lo fácil o difícil que es usar la interfaz de usuario para el público más amplio posible. El tiempo que se tarda en probar una aplicación merece la pena.

Este tema se centra en tres escenarios de prueba principales: facilidad de uso general, accesibilidad y automatización.

## <a name="usability-testing"></a>Pruebas de facilidad de uso

Las pruebas de facilidad de uso ofrecen la oportunidad de evaluar un producto mediante el estudio de cómo usan realmente los usuarios reales el producto. Este análisis garantiza que las suposiciones clave sobre los usuarios previstos y los diseños de interfaz se admiten (o se prueban) con datos reales. Solo mediante la recopilación de estos datos empíricos puede averiguar qué tan bien se ajusta la interfaz de usuario de un producto a las necesidades y expectativas de los usuarios.

Al observar la interacción del usuario con el producto y escuchar los comentarios de los usuarios, se identifican características importantes que pueden ser difíciles de encontrar y usar. En función de estos resultados, se pueden realizar ajustes en la interfaz de usuario según sea necesario. Es casi imposible crear un producto útil sin algún nivel de prueba de facilidad de uso, ya que los resultados proporcionan la base para tomar mejores decisiones sobre el producto y mejorar la experiencia general del usuario.

Las pruebas de facilidad de uso proporcionan una reversión significativa solo cuando está bien integrada en todo el ciclo de vida del proyecto. Un único estudio de facilidad de uso puede identificar problemas, pero sin pruebas de seguimiento es difícil determinar si las soluciones han resuelto esos problemas o han introducido otros nuevos.

Los escenarios principales para las pruebas de facilidad de uso son:

-   Si es un proveedor de productos de software, probar usuarios reales del producto significa que está evaluando el diseño. En función de cómo haya diseñado la aplicación, ¿pueden los usuarios completar las tareas que necesitan hacer? Las pruebas de usuarios reales que realicen tareas reales también pueden señalar si las directrices de interfaz de usuario que sigue funcionan en el contexto del producto y cuando la coherencia ayuda o dificulta la capacidad de un usuario para realizar su trabajo.
-   Si es comprador de un producto de software, puede realizar pruebas de facilidad de uso para evaluar un producto para su compra. Por ejemplo, su empresa podría considerar la posibilidad de comprar un producto para sus veinte mil empleados. Antes de que la empresa gaste su dinero, quiere asegurarse de que el producto en cuestión realmente ayudará a los empleados a mejorar su trabajo. Las pruebas de facilidad de uso también pueden ser útiles para ver si la aplicación propuesta sigue las directrices de estilo de interfaz de usuario publicadas (internas o externas). Es mejor usar las directrices de la interfaz de usuario como una fuente auxiliar, en lugar de principal, de información para tomar decisiones de compra.

Para obtener más información, vea [Facilidad de uso en la práctica: Pruebas de facilidad de uso.](/archive/msdn-magazine/2009/brownfield/usability-in-practice-usability-testing)

## <a name="accessibility-testing"></a>Pruebas de accesibilidad

Las pruebas de accesibilidad abarcan dos áreas de un diseño de interfaz de usuario: compatibilidad con usuarios con discapacidades y acceso mediante programación mediante marcos de prueba automatizados.

Asegurarse de que una aplicación es accesible para los usuarios con discapacidades implica realizar pruebas para:

-   Cumplimiento: ¿la aplicación cumple varios requisitos legales relacionados con la accesibilidad?
-   Eficacia: ¿los usuarios con discapacidades pueden usar la aplicación?
-   Utilidad: ¿expone la aplicación la funcionalidad adecuada para los usuarios con discapacidades?
-   Satisfacción: ¿cómo la aplicación la perciben los usuarios con discapacidades?

Las pruebas de estos aspectos de una aplicación se pueden realizar mediante una auditoría de accesibilidad, que implica una revisión manual de la aplicación por parte de un experto en accesibilidad y un estudio de facilidad de uso centrado de usuarios deshabilitados y dispositivos de tecnología de asistencia.

Aunque aparentemente no está relacionado, hay una estrecha correlación entre los requisitos de acceso mediante programación de los marcos de prueba automatizados y los de los dispositivos de tecnología de asistencia. La compatibilidad con una tiene la ventaja adicional de habilitar la otra. Para obtener más información sobre la accesibilidad y la automatización [](/windows/desktop/WinAuto/testing-tools)de pruebas en Windows, vea [Accesibilidad,](/windows/desktop/accessibility)Herramientas de pruebas y la [API Windows Automation.](/windows/desktop/WinAuto/windows-automation-api-portal)

 

 