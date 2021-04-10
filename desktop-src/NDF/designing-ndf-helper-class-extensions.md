---
title: Diseñar extensiones de clase auxiliar NDF
description: El objetivo de este tema es proporcionar instrucciones genéricas mediante el proceso de desarrollo de la extensión de clase auxiliar.
ms.assetid: f5dbd198-7d22-4e7e-830e-6753e9f4d6c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91ff748d8139aad17fca3710b17e73b5e1eaa14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994105"
---
# <a name="designing-ndf-helper-class-extensions"></a>Diseñar extensiones de clase auxiliar NDF

El objetivo de este tema es proporcionar instrucciones genéricas mediante el proceso de desarrollo de la extensión de clase auxiliar. Las instrucciones de este tema se aplican a todas las extensiones de clase auxiliares. Para obtener instrucciones más específicas, consulte la [clase auxiliar extensible](windows-filtering-platform-extensible-helper-class.md) de la plataforma de filtrado de Windows y [las clases auxiliares extensibles de diagnóstico inalámbrico de 802,11](802-11-wireless-diagnostics-extensible-helper-classes.md).

## <a name="extending-ndf-functionality"></a>Extender la funcionalidad NDF

Windows Vista y versiones posteriores se incluyen con una variedad de clases auxiliares ya implementadas que pueden diagnosticar y reparar una amplia gama de problemas. Sin embargo, en ocasiones, es posible que los desarrolladores de terceros quieran ampliar estas clases auxiliares para diagnosticar y resolver problemas específicos de sus productos e implementaciones particulares.

Las siguientes clases auxiliares de Microsoft NDF son extensibles.

-   [Plataforma de filtrado de Windows](windows-filtering-platform-extensible-helper-class.md)
-   [Seguridad inalámbrica](802-11-wireless-diagnostics-extensible-helper-classes.md)

## <a name="implementing-a-helper-class-extension"></a>Implementar una extensión de clase auxiliar

Microsoft envía dos interfaces que se pueden usar para desarrollar extensiones de clase auxiliares de NDF.

NDF llama a la interfaz [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) para validar que tiene toda la información necesaria y que ha elegido la clase auxiliar correcta. Esto lo lleva a cabo a través del método [**GetAttributeInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelperinfo-getattributeinfo) .

NDF llama a la interfaz [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) para la mayoría de las actividades que se producen durante el procedimiento de diagnóstico. Algunos de sus métodos son obligatorios, pero otros son opcionales para usos específicos.

Los métodos necesarios incluyen [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) y [**GetDiagnosticsInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getdiagnosticsinfo). NDF llama a **Initialize** para enviar parámetros de clave a la extensión de clase auxiliar para inicializar el estado de la instancia. **GetDiagnosticsInfo** proporciona una estimación del tiempo que puede tardar el diagnóstico y de si requiere la suplantación del contexto de usuario original.

Otro método, [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth), se llama para realizar el diagnóstico en el componente de red correspondiente a la clase auxiliar. Se llama a [**Cancel**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cancel) cuando NDF determina que se debe detener el diagnóstico o la reparación en curso. La [**limpieza**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cleanup) permite a NDF liberar los recursos NDF que la extensión de clase auxiliar ha usado desde que se realizó la llamada a [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) .

Para obtener información sobre métodos adicionales, vea [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper).

Las extensiones de clase auxiliar NDF se usan para diagnosticar y resolver problemas de conectividad asociados a una aplicación o componente específico. También validan el éxito o el fracaso de un intento de resolución.

Los desarrolladores que consideren la implementación de una extensión de clase auxiliar deben realizar las siguientes tareas.

-   Identificar los escenarios de usuario en los que resultan útiles las acciones de diagnóstico y reparación.
-   Proporcionar soluciones a los problemas de conectividad que se producen con frecuencia.
-   Si se requiere una extensión de clase auxiliar, defina un modelo de estado de componente que se usa para representar el estado de mantenimiento del componente en NDF.

## <a name="identify-user-scenarios"></a>Identificar escenarios de usuario

Es posible que las pruebas y el uso de una aplicación ya hayan proporcionado patrones que puedan ser capaces de diagnosticar y reparar. Los desarrolladores de aplicaciones pueden usar estos datos para determinar los problemas de conectividad más importantes que se deben abordar e identificar los escenarios de usuario en los que es probable que se produzcan problemas de conectividad.

La determinación de la causa principal de cada problema es fundamental en esta parte del proceso. Esto puede requerir una investigación extensa, pero le ayudará a crear software que sea mucho más fácil de usar para los usuarios y los administradores. Si no se identifica una causa raíz, resulta difícil o imposible ofrecer resolución de problemas con la extensión de clase auxiliar.

## <a name="provide-resolutions"></a>Proporcionar soluciones

Después de que un equipo de desarrollo identifique las causas raíz de los problemas asociados a su software, el paso siguiente consiste en identificar las acciones de resolución adecuadas para ayudar al usuario a resolver el problema de la manera más eficaz posible.

No todas las resoluciones requieren que se cree una extensión de clase auxiliar o una acción automatizada. En algunos casos, el equipo puede determinar que el mejor enfoque para resolver una causa raíz es corregir o actualizar el componente, proporcionar contenido de ayuda adicional para el componente o desarrollar otras estrategias que proporcionan mejores soluciones a largo plazo.

En el caso de los problemas en los que una acción automatizada es ideal, la creación de una extensión de clase auxiliar NDF suele ser una solución excelente.

Las extensiones de clase auxiliar devuelven información sobre las causas raíz y la información de reparación a los usuarios a través de NDF. Las cadenas que se usan para describir las causas raíz y la información de reparación deben ser sencillas y fáciles de entender para un usuario no técnico. Para obtener más información sobre estas cadenas, vea [directrices de la interfaz de usuario para las extensiones de clase auxiliares de NDF](user-interface-guidelines-for-ndf-helper-class-extensions.md).

## <a name="define-a-component-health-model"></a>Definir un modelo de estado de componentes

Los desarrolladores de software deben definir niveles de "mantenimiento" asociados a la capacidad de administración de los problemas de red. Un modelo de estado usado para desarrollar clases auxiliares define solo dos niveles de mantenimiento: correcto y incorrecto. Estos niveles también se pueden aplicar a las extensiones de clase auxiliar NDF.

Un componente correcto indica una ausencia de problemas. Un componente se puede considerar incorrecto debido a sus propios problemas o debido a problemas que se producen en otros componentes de los que depende.



| Término                                                                                                                             | Descripción                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="LowHealth"></span><span id="lowhealth"></span><span id="LOWHEALTH"></span>LowHealth<br/>                         | Este estado indica un nivel inaceptable de errores de este componente y que el componente es el problema.<br/>    |
| <span id="LowHealth_Below"></span><span id="lowhealth_below"></span><span id="LOWHEALTH_BELOW"></span>LowHealth a continuación<br/> | Este estado indica un nivel inaceptable de errores de un componente del equipo local del que depende este componente.<br/> |



 

Cuando se realiza el diagnóstico con NDF, se formula una serie de preguntas en la extensión de clase auxiliar para determinar su estado de mantenimiento. Si la extensión responde que está en mal estado, NDF le pedirá dudas, intentando diagnosticar el problema, su ubicación y dónde buscar a continuación. Cada clase auxiliar debe ser capaz de responder a la pregunta de un estado bajo para mejorar las actividades de diagnóstico adecuadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clase auxiliar extensible de la plataforma de filtrado de Windows](windows-filtering-platform-extensible-helper-class.md)
</dt> <dt>

[802,11 clases auxiliares extensibles de diagnóstico inalámbrico](802-11-wireless-diagnostics-extensible-helper-classes.md)
</dt> </dl>

 

 





