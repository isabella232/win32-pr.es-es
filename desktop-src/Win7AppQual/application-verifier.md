---
description: .
ms.assetid: edf719b7-9bd9-4e23-9bba-d0d7c3c5dbf5
title: Comprobador de aplicaciones (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dddbac00c3f16a1072a79aca096c46aaff0d2983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913377"
---
# <a name="application-verifier-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Comprobador de aplicaciones (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes** -Windows XP Windows \| vista Windows \| 7  
**Servidores** : windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2  


## <a name="description"></a>Descripción

Promocione y aplique comprobador de aplicaciones como una puerta de calidad para todo el desarrollo. Incluye varias mejoras:

-   Hemos proporcionado comprobaciones adicionales para solucionar los problemas detectados por el equipo de Informe de errores de Windows durante el uso del grupo de subprocesos.
-   Combinamos versiones de 32 y 64 bits del paquete para tratar los cambios en Windows 7, incluidas las necesidades de pruebas de componentes de 32 bits en una versión de Windows de 64 bits, así como para la simplificación general.
-   Hemos incluido comprobaciones adicionales para las aplicaciones multiproceso, en las que se ejecutan aplicaciones de 32 bits en Windows de 64 bits, así como numerosas correcciones de errores.

Estos cambios no deben tener ningún impacto negativo en los usuarios que no habilitan las comprobaciones de subprocesos; los que deben recibir compatibilidad adicional en la detección y el diagnóstico de los problemas de uso del grupo de subprocesos existentes. Tanto si habilita las comprobaciones de subprocesos como si no, se beneficiará de las demás mejoras y correcciones de errores de este servicio.

Aunque hay una ligera disminución del rendimiento al usar este servicio, los niveles de rendimiento deben ser aceptables porque normalmente no se ejecutan en entornos comerciales.

## <a name="usage"></a>Uso

**Información general**

Para ofrecer aplicaciones Windows confiables:

1.  Pruebe las aplicaciones escritas en código no administrado (nativo) con comprobador de aplicaciones bajo el depurador y con el montón de página completa antes de publicarlo para los clientes.
2.  Siga los pasos proporcionados por comprobador de aplicaciones para resolver las condiciones errantes.
3.  Una vez publicada la aplicación, supervise periódicamente los informes de errores de la aplicación recopilados por Informe de errores de Windows.

Las comprobaciones de grupo de subprocesos están habilitadas de forma predeterminada en el encabezado de comprobación "aspectos básicos". Como se incluye en la configuración predeterminada, los usuarios solo necesitan ejecutar comprobador de aplicaciones en su código con la configuración predeterminada para aprovechar las nuevas comprobaciones.

**Detalles**

Como mínimo, debe ejecutar comprobador de aplicaciones que tenga seleccionada la opción básico. Esto es necesario para WinLogo y WinQual. La configuración de conceptos básicos comprueba lo siguiente:

-   **Detalles** de la detención de excepciones: garantiza que las aplicaciones no ocultan las infracciones de acceso mediante el control de excepciones estructurado.
-   **Controla los detalles** de la detención: comprueba para asegurarse de que la aplicación no intenta usar identificadores no válidos.
-   **Detalles** de la detención de montones: comprueba los problemas de daños en la memoria del montón.
-   **Detalles de detención de entrada/salida** : supervisa la ejecución de e/s asincrónica y realiza varias validaciones.
-   **Detalles de detención de pérdida** : detecta pérdidas mediante el seguimiento de los recursos realizados por una DLL que no se liberan en el momento en que se descargó la dll.
-   **Detalles de detención de bloqueos** : comprueba el uso correcto de las secciones críticas.
-   **Detalles de detención de memoria** : garantiza que las API para las manipulaciones de espacio virtual se usan correctamente (por ejemplo, VirtualAlloc, MapViewOfFile)
-   **Detalles de detención de TLS** : garantiza que las API de almacenamiento local de subprocesos se usen correctamente
-   **Detalles de detención de ThreadPool** : garantiza el uso correcto de las API ThreadPool y aplica las comprobaciones de coherencia en los Estados de subprocesos de trabajo después de una devolución de llamada.

Si la aplicación se está migrando desde una aplicación "anterior a vista", querrá aprovechar el "LuaPriv" (también conocido como comprobaciones de UAC). El predicción de privilegios de cuenta de usuario limitada (LuaPriv) tiene dos objetivos principales:

-   **Predictiva**: mientras se ejecuta una aplicación con privilegios administrativos, prediga si esa aplicación funcionará también si se ejecuta con menos privilegios (por lo general, como un usuario normal). Por ejemplo, si la aplicación escribe en archivos que solo permiten a los administradores tener acceso, la aplicación no podrá escribir en el mismo archivo si se ejecuta como no administrador.
-   **Diagnóstico**: mientras se ejecuta con privilegios que no son de administrador, identifique los posibles problemas que ya existan en la ejecución actual. Continuando con el ejemplo anterior, si la aplicación intenta escribir en un archivo que solo concede acceso a los miembros del grupo de administradores, la aplicación obtendrá un error de acceso \_ denegado. Si la aplicación no funciona correctamente, esta operación puede ser la causa.

LuaPriv identifica los siguientes tipos de problemas:



| **Posible problema**       | **Descripción**                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Espacios de nombres restringidos     | La creación de un objeto de sincronización con nombre (evento, semáforo, exclusión mutua, etc.) sin un espacio de nombres puede complicar la ejecución sin privilegios en algunos sistemas operativos, ya que el sistema operativo puede optar por colocar el objeto en un espacio de nombres restringido. La creación de este tipo de objeto en un espacio de nombres restringido (como el espacio de nombres global) requiere SeCreateGlobalPrivilege, que solo se concede a los administradores.<br/> LuaPriv marca ambos problemas si los detecta.<br/> |
| Comprobaciones del administrador duro | Algunas aplicaciones interrogan el token de seguridad del usuario para averiguar cuántos privilegios tiene. En esos casos, la aplicación puede cambiar su comportamiento en función de la cantidad de energía que considere que tiene el usuario. <br/> LuaPriv marca las llamadas API que devuelven esta información.<br/>                                                                                                                                                                                                |
| Solicitar privilegios     | Una aplicación puede intentar habilitar un privilegio relevante para la seguridad (como SeTcbPrivilege o SeSecurityPrivilege) antes de realizar una operación que lo requiere. <br/> LuaPriv Flags intenta habilitar los privilegios relevantes para la seguridad. <br/>                                                                                                                                                                                                                               |
| Faltan privilegios        | Si una aplicación intenta habilitar un privilegio que el usuario no tiene, es probable que indique que la aplicación espera el privilegio, lo que puede producir diferencias de comportamiento. <br/> LuaPriv marca las solicitudes de privilegios con errores. <br/>                                                                                                                                                                                                                                       |
| Operaciones de INI-File       | Los intentos de escribir en archivos INI asignados (WritePrivateProfileSection y API similares) pueden producir errores como usuarios sin privilegios de administrador. <br/> LuaPriv marca tales operaciones.<br/>                                                                                                                                                                                                                                                                                                            |
| Acceso denegado             | Si la aplicación intenta obtener acceso a un objeto (archivo, clave del registro, etc.) pero se produce un error en el intento debido a un acceso insuficiente, es probable que la aplicación se esté ejecutando con más privilegios de los que tiene. <br/> LuaPriv marca los intentos de apertura de objeto que producen un error con acceso \_ denegado y errores similares.<br/>                                                                                                                                                               |
| ACE de denegación                 | Si un objeto tiene ACE de denegación en su DACL, deniega explícitamente el acceso a entidades específicas. <br/> Esto no es habitual y dificulta la predicción, por lo que las marcas LuaPriv deniegan las ACE cuando las encuentra.<br/>                                                                                                                                                                                                                                                                     |
| Acceso restringido         | Si una aplicación intenta abrir un objeto para los derechos que no se conceden a los usuarios normales (por ejemplo, al intentar escribir en un archivo que solo pueden escribir los administradores), la aplicación probablemente no funcionará igual cuando se ejecute como un usuario normal. <br/> LuaPriv marca tales operaciones.<br/>                                                                                                                                                                      |
| MÁXIMO \_ permitido          | Si una aplicación abre un objeto para \_ el máximo permitido, la comprobación de acceso real en el objeto se producirá en otra parte. La mayoría del código que lo hace no funciona correctamente y casi ciertamente funcionará de manera diferente cuando se ejecute sin privilegios. <br/> De este modo, LuaPriv marca todos los incidentes de máximo \_ permitido. <br/>                                                                                                                                                            |



 

Los problemas que se suelen pasar por alto se capturan en las comprobaciones de Nebulous Misc:

-   Detalles de detención de API peligrosas
-   Detalles de detención de pilas desfasadas
-   Sustitución de hora

Hemos agregado un nuevo comprobador de impresión. Este nivel ayuda a encontrar y solucionar problemas que pueden producirse cuando una aplicación llama al subsistema de impresión. El comprobador de impresión tiene como destino las dos capas del subsistema de impresión, el nivel PrintAPI y el nivel PrintDriver.

*Nivel de API de impresión*

El comprobador de impresión prueba la interfaz entre un programa y winspool. drv y prntvpt.dll y prueba las interfaces de esos archivos dll. Puede revisar las reglas para llamar a funciones en esta interfaz en la sección de ayuda de MSDN sobre las API exportadas por winspool. drv y prntvpt.dll.

*Nivel de controlador de impresión*

El comprobador de impresión también prueba la interfaz entre un controlador de impresión principal, como UNIDRV.DLL, UNIDRUI.DLL, PSCRIPT5.DLL, PS5UI.DLL o MXDWDRV.DLL y los complementos de controlador de impresión. Puede encontrar información sobre esta interfaz en MSDN y WDK.

Tenga en cuenta que algunas de estas comprobaciones son solo para Windows 7 y otras simplemente funcionarán mejor en Windows 7.

Normalmente, solo las versiones de depuración ejecutan el comprobador de aplicaciones, por lo que el rendimiento no suele ser un problema. Si surgen problemas de rendimiento del uso de este, o de cualquier otro comprobador de aplicaciones comprobación, ejecute una comprobación cada vez hasta que haya realizado todas las comprobaciones necesarias.

Casi el 10% de los bloqueos de la aplicación en sistemas Windows se deben a daños en el montón. Estos bloqueos son casi imposibles de depurar después del hecho. La mejor manera de evitar estos problemas es probar con las características del montón de páginas que se encuentran en comprobador de aplicaciones. Hay dos tipos de montones de páginas: "Full" y "Light". Full es el valor predeterminado; forzará que un depurador se detenga al instante después de detectar daños. Esta característica debe ejecutarse en el depurador. Sin embargo, también es el más exigente. Si un usuario tiene problemas de control de tiempo y ya ha ejecutado un escenario en el montón de páginas "completo", es probable que lo establezca en "Light". Además, el montón de páginas claras no se bloquea hasta que finaliza el proceso. Proporciona un seguimiento de la pila para la asignación, pero puede tardar mucho más tiempo en diagnosticarse que aprovechar su homólogo completo.

Supervise el estado de confiabilidad de las aplicaciones a través del portal web de WinQual. Este portal muestra los informes de errores recopilados a través de Informe de errores de Windows, por lo que es fácil identificar los errores más frecuentes. Obtenga información sobre esto en Informe de errores de Windows: Introducción. Microsoft no cobra por este servicio.

Para aprovechar las ventajas de WinQual, debe:

1.  Registre su empresa para WinQual, que requiere un identificador de VeriSign. Puede encontrar información de Windows 7 sobre WinQual en el portal para desarrolladores, agrupado en Windows Vista SP1 \\ Windows Server 2008. Pronto tendrá una ubicación de Windows 7.
2.  Asigne las aplicaciones de ISV a un nombre de producto y el nombre del ISV, que vincula los informes de errores a la empresa. Otros ISV no pueden ver los informes de errores.
3.  Use el portal para identificar los principales problemas. Los ISV también pueden crear respuestas que informen a los clientes de los pasos que deben realizarse después de un error. El sistema de respuesta admite más de 10 idiomas en todo el mundo.

Tenga en cuenta lo siguiente: comprobador de aplicaciones solo es tan bueno como las rutas de acceso de código en las que se ejecuta. El valor de la combinación de esta herramienta con una herramienta de cobertura de código no puede ser sobreutilizado.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

**Herramientas de depuración para Windows:**

-   [Información general y sitio de descarga](https://msdn.microsoft.com/windows/hardware/bg127145)
-   [Documentación en línea de MSDN](/windows-hardware/drivers/debugger/)

**comprobador de aplicaciones:**

-   [Información general](/previous-versions/ms220948(v=vs.80))
-   [Descargar](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&amp;DisplayLang=en)
-   [Comprobador de aplicaciones para Microsoft Visual Studio 2008/.NET Framework 3,5](/previous-versions/ms220948(v=vs.80))

    **Nota:** la versión de Comprobador de aplicaciones que se incluye en Visual Studio es bastante antigua. Si es posible, utilice en su lugar el paquete independiente. Por esta razón, las versiones futuras de Visual Studio ya no tendrán comprobador de aplicaciones incrustadas.

**WinQual**

-   [Servicios en línea de calidad de Windows (WinQual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)
-   [Informe de errores de Windows: Introducción](../wer/using-wer.md)

 

 
