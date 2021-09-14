---
title: Diseño de extensiones de clase auxiliar de NDF
description: Este tema está pensado para proporcionar instrucciones genéricas a través del proceso de desarrollo de extensiones de clase auxiliar.
ms.assetid: f5dbd198-7d22-4e7e-830e-6753e9f4d6c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91ff748d8139aad17fca3710b17e73b5e1eaa14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161215"
---
# <a name="designing-ndf-helper-class-extensions"></a>Diseño de extensiones de clase auxiliar de NDF

Este tema está pensado para proporcionar instrucciones genéricas a través del proceso de desarrollo de extensiones de clase auxiliar. Las instrucciones de este tema se aplican a todas las extensiones de clase auxiliar. Para obtener instrucciones más específicas, [vea Windows asistente extensible](windows-filtering-platform-extensible-helper-class.md) de la plataforma de filtrado y [802.11 Wireless Diagnostics Extensible Helper Classes ( Clases auxiliares extensibles de diagnósticos inalámbricos 802.11).](802-11-wireless-diagnostics-extensible-helper-classes.md)

## <a name="extending-ndf-functionality"></a>Extensión de la funcionalidad de NDF

Windows Vista y versiones posteriores se envían con una variedad de clases auxiliares ya implementadas que pueden diagnosticar y reparar una amplia gama de problemas. Sin embargo, en ocasiones, es posible que los desarrolladores de terceros quieran ampliar estas clases auxiliares para diagnosticar y resolver problemas específicos de sus productos e implementaciones concretos.

Las siguientes clases auxiliares de Microsoft NDF son extensibles.

-   [Plataforma de filtrado de Windows](windows-filtering-platform-extensible-helper-class.md)
-   [Seguridad inalámbrica](802-11-wireless-diagnostics-extensible-helper-classes.md)

## <a name="implementing-a-helper-class-extension"></a>Implementar una extensión de clase auxiliar

Microsoft envía dos interfaces que se pueden usar para desarrollar extensiones de clase auxiliar de NDF.

NDF llama a la interfaz [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) para validar que tiene toda la información necesaria y que ha elegido la clase auxiliar correcta. Esto se logra a través del [**método GetAttributeInfo.**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelperinfo-getattributeinfo)

NDF llama a la interfaz [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) para la mayoría de las actividades que se producen durante el procedimiento de diagnóstico. Algunos de sus métodos son necesarios, pero otros son opcionales para usos específicos.

Los métodos necesarios [**incluyen Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) [**y GetDiagnosticsInfo.**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getdiagnosticsinfo) NDF llama a **Initialize** para enviar parámetros de clave a la extensión de clase auxiliar para inicializar su estado de instancia. **GetDiagnosticsInfo** proporciona una estimación de cuánto tiempo puede tardar el diagnóstico y si requiere la suplantación del contexto de usuario original.

Se llama a [**otro método, LowHealth,**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth)para realizar el diagnóstico en el componente de red correspondiente a la clase auxiliar. [**Se**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cancel) llama a Cancel cuando NDF determina que se debe detener un diagnóstico o reparación en curso. [**La**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cleanup) limpieza permite que NDF libere los recursos de NDF que la extensión de clase auxiliar ha usado desde que se realizó la llamada [**a Initialize.**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize)

Para obtener información sobre métodos adicionales, [**vea INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper).

Las extensiones de clase auxiliar de NDF se usan para diagnosticar y resolver problemas de conectividad asociados a una aplicación o componente específicos. También validan el éxito o el error de un intento de resolución.

Los desarrolladores que consideren la implementación de una extensión de clase auxiliar deben realizar las siguientes tareas.

-   Identificar escenarios de usuario en los que las acciones de diagnóstico y reparación son útiles.
-   Proporcionar soluciones a problemas de conectividad detectados con frecuencia.
-   Si se requiere una extensión de clase auxiliar, defina un modelo de mantenimiento de componentes usado para representar el estado de mantenimiento del componente en NDF.

## <a name="identify-user-scenarios"></a>Identificar escenarios de usuario

Es posible que las pruebas y el uso de una aplicación ya hayan proporcionado patrones perceptibles que una extensión de clase auxiliar pueda diagnosticar y, posiblemente, reparar. Los desarrolladores de aplicaciones pueden usar estos datos para determinar los problemas de conectividad más importantes que se deben solucionar e identificar los escenarios de usuario en los que es probable que se produzcan problemas de conectividad.

Determinar la causa principal de cada problema es fundamental en esta parte del proceso. Esto puede requerir una amplia investigación, pero ayudará a crear software que sea mucho más fácil de usar para los usuarios y administradores. Si no se identifica una causa principal, resulta difícil o imposible ofrecer resolución de problemas mediante la extensión de clase auxiliar.

## <a name="provide-resolutions"></a>Proporcionar resoluciones

Después de que un equipo de desarrollo haya identificado las causas principales de los problemas asociados a su software, el siguiente paso es identificar las acciones de resolución adecuadas para ayudar al usuario a resolver el problema de la manera más eficaz posible.

No todas las resoluciones requieren que se cree una extensión de clase auxiliar o una acción automatizada. En algunos casos, el equipo puede determinar que el mejor enfoque para resolver una causa principal es corregir o actualizar el componente, proporcionar contenido de ayuda adicional para el componente o desarrollar otras estrategias que proporcionen mejores soluciones a largo plazo.

Para los problemas en los que una acción automatizada es ideal, la creación de una extensión de clase auxiliar de NDF suele ser una solución excelente.

Las extensiones de clase auxiliar devuelven información sobre las causas principales y la información de reparación a los usuarios a través de NDF. Las cadenas usadas para describir las causas principales y la información de reparación deben ser sencillas y fáciles de entender para un usuario no técnico. Para obtener más información sobre estas cadenas, vea Interfaz de usuario instrucciones para las extensiones de clase [auxiliar de NDF](user-interface-guidelines-for-ndf-helper-class-extensions.md).

## <a name="define-a-component-health-model"></a>Definir un modelo de mantenimiento de componentes

Los desarrolladores de software deben definir los niveles de "estado" asociados a la capacidad de administración de los problemas de red. Un modelo de mantenimiento que se usa para desarrollar clases auxiliares define solo dos niveles de mantenimiento: correcto e incorrecto. Estos niveles también se pueden aplicar a las extensiones de clase auxiliar de NDF.

Un componente correcto indica una ausencia de problemas. Un componente se puede considerar incorrecto debido a sus propios problemas o a problemas que se producen en otros componentes de los que depende.



| Término                                                                                                                             | Descripción                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="LowHealth"></span><span id="lowhealth"></span><span id="LOWHEALTH"></span>LowHealth<br/>                         | Este estado indica un nivel inaceptable de errores de este componente y que el componente es el problema.<br/>    |
| <span id="LowHealth_Below"></span><span id="lowhealth_below"></span><span id="LOWHEALTH_BELOW"></span>LowHealth a continuación<br/> | Este estado indica un nivel inaceptable de errores de un componente de máquina local del que depende este componente.<br/> |



 

Cuando el diagnóstico tiene lugar mediante NDF, se realiza una serie de preguntas a la extensión de clase auxiliar para determinar su estado de mantenimiento. Si la extensión responde que está en mal estado, NDF hace preguntas aclarantes, intentando diagnosticar el problema, su ubicación y dónde buscar a continuación. Cada clase auxiliar debe ser capaz de responder a la pregunta de bajo estado con el fin de dirigir mejor las actividades de diagnóstico adecuadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Clase auxiliar extensible de la plataforma de filtrado](windows-filtering-platform-extensible-helper-class.md)
</dt> <dt>

[802.11 Clases auxiliares extensibles de diagnóstico inalámbrico](802-11-wireless-diagnostics-extensible-helper-classes.md)
</dt> </dl>

 

 





