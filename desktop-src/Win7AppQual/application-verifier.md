---
description: Application Verifier (Windows guía de calidad de aplicaciones de Windows Server 2008 R2)
ms.assetid: edf719b7-9bd9-4e23-9bba-d0d7c3c5dbf5
title: Application Verifier (Windows guía de calidad de aplicaciones de Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac2a8bc900ea9d1f35ae228371226355657b930
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249404"
---
# <a name="application-verifier-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Application Verifier (Windows guía de calidad de aplicaciones de Windows Server 2008 R2)

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows XP, Windows Vista, Windows 7  
**Servidores:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  


## <a name="description"></a>Descripción

Promover y aplicar Application Verifier como puerta de calidad para todo el desarrollo. Incluye varias mejoras:

-   Hemos proporcionado comprobaciones adicionales para solucionar los problemas detectados por el Informe de errores de Windows durante el uso del grupo de subprocesos.
-   Combinamos versiones de 32 y 64 bits del paquete para abordar los cambios de Windows 7, incluidas las necesidades de probar componentes de 32 bits en una versión de 64 bits de Windows, así como para simplificar de forma general.
-   Hemos incluido comprobaciones adicionales para aplicaciones multiproceso, que ejecutan aplicaciones de 32 bits en aplicaciones de 64 Windows, así como muchas correcciones de errores.

Estos cambios no deben tener ningún impacto negativo en los usuarios que no habilitan las comprobaciones de subprocesos. aquellos que lo hacen deben recibir soporte adicional en la detección y el diagnóstico de problemas de uso existentes del grupo de subprocesos. Independientemente de si habilita o no las comprobaciones de subprocesos, se beneficiará de las otras mejoras y correcciones de errores de este servicio.

Aunque hay una pequeña reducción del rendimiento al usar este servicio, los niveles de rendimiento deben seguir siendo aceptables porque normalmente no se ejecutan en entornos comerciales.

## <a name="usage"></a>Uso

**Información general**

Para proporcionar aplicaciones de Windows confiables:

1.  Pruebe las aplicaciones escritas en código no administrado (nativo) con Application Verifier en el depurador y con el montón de página completa antes de publicarlo a los clientes.
2.  Siga los pasos proporcionados por Application Verifier resolver condiciones errantes.
3.  Una vez publicada la aplicación, supervise periódicamente los informes de errores de la aplicación recopilados por Informe de errores de Windows.

Las comprobaciones del grupo de subprocesos están habilitadas de forma predeterminada en el encabezado de comprobación "Aspectos básicos". Como esto se incluye en la configuración predeterminada, los usuarios solo necesitan ejecutar Application Verifier en su código con la configuración predeterminada para aprovechar las nuevas comprobaciones.

**Detalles**

Como mínimo, debe ejecutar el Application Verifier con la opción Aspectos básicos seleccionada. Esto es necesario para WinLogo y WinQual. La configuración Aspectos básicos comprueba lo siguiente:

-   **Detalles de detenciones de excepciones:** garantiza que las aplicaciones no ocultan las infracciones de acceso mediante el control de excepciones estructurado
-   **Identificadores de detalles de detenerse:** pruebas para asegurarse de que la aplicación no intenta usar identificadores no válidos
-   **Detalles de detenciones de montones:** comprueba si hay problemas de daños en la memoria en el montón
-   **Detalles de detenerse de entrada/salida:** supervisa la ejecución de E/S asincrónica y realiza varias validaciones.
-   **Detalles de la** detección de pérdidas: detecta pérdidas mediante el seguimiento de los recursos realizados por un archivo DLL que no se liberan en el momento en que se descargó el archivo DLL.
-   **Detalles de detenciones de bloqueos:** comprueba el uso correcto de las secciones críticas
-   **Detalles de detenciones** de memoria: garantiza que las API para manipulaciones de espacio virtual se usan correctamente (por ejemplo, VirtualAlloc, MapViewOfFile)
-   **Detalles de detenerse de TLS:** garantiza que las API de Storage de subprocesos se usan correctamente
-   **Detalles de detenciones de threadpool:** garantiza el uso correcto de las API de threadpool y aplica comprobaciones de coherencia en los estados de subproceso de trabajo después de una devolución de llamada

Si la aplicación va a migrar desde una aplicación "Pre-Vista", querrá aprovechar "LuaPriv" (también conocida como comprobaciones de UAC). El predictor de privilegios de cuenta de usuario limitado (LuaPriv) tiene dos objetivos principales:

-   **Predictivo:** al ejecutar una aplicación con privilegios administrativos, predijo si esa aplicación funcionaría bien si se ejecuta con menos privilegios (por lo general, como usuario normal). Por ejemplo, si la aplicación escribe en archivos que solo permiten el acceso de administradores, esa aplicación no podrá escribir en el mismo archivo si se ejecuta como no administrador.
-   **Diagnóstico:** mientras se ejecuta con privilegios de no administrador, identifique posibles problemas que ya puedan existir con la ejecución actual. Siguiendo con el ejemplo anterior, si la aplicación intenta escribir en un archivo que concede acceso solo a los miembros del grupo administrador, la aplicación recibirá un error DE ACCESO \_ DENEGADO. Si la aplicación no funciona correctamente, esta operación puede ser la causa.

LuaPriv identifica los siguientes tipos de problemas:



| **Posible problema**       | **Descripción**                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Espacios de nombres restringidos     | La creación de un objeto de sincronización con nombre (evento, semáforo, exclusión mutua, etc.) sin un espacio de nombres puede complicar la ejecución sin privilegios en algunos sistemas operativos porque el sistema operativo puede optar por colocar el objeto en un espacio de nombres restringido. La creación de este tipo de objeto en un espacio de nombres restringido (como el espacio de nombres global) requiere SeCreateGlobalPrivilege, que solo se concede a los administradores.<br/> LuaPriv marca ambos problemas si los detecta.<br/> |
| Comprobaciones de administrador de forma dura | Algunas aplicaciones interrogan el token de seguridad del usuario para averiguar cuántos privilegios tiene. En esos casos, la aplicación puede cambiar su comportamiento en función de la potencia que piense que tiene el usuario. <br/> LuaPriv marca las llamadas API que devuelven esta información.<br/>                                                                                                                                                                                                |
| Solicitar privilegios     | Una aplicación puede intentar habilitar un privilegio relevante para la seguridad (como SeTcbPrivilege o SeSecurityPrivilege) antes de realizar una operación que lo requiera. <br/> Las marcas de LuaPriv intentan habilitar privilegios pertinentes para la seguridad. <br/>                                                                                                                                                                                                                               |
| Privilegios que faltan        | Si una aplicación intenta habilitar un privilegio que el usuario no tiene, probablemente señale que la aplicación espera el privilegio, lo que puede provocar diferencias de comportamiento. <br/> LuaPriv marca las solicitudes de privilegios con error. <br/>                                                                                                                                                                                                                                       |
| INI-File operations       | Los intentos de escribir en archivos INI asignados (WritePrivateProfileSection y API similares) pueden producir un error como usuario que no es administrador. <br/> LuaPriv marca estas operaciones.<br/>                                                                                                                                                                                                                                                                                                            |
| Acceso denegado             | Si la aplicación intenta acceder a un objeto (archivo, clave del Registro, etc.) pero se produce un error en el intento debido a un acceso insuficiente, la aplicación probablemente espera que se ejecute con más privilegios de los que tiene. <br/> LuaPriv marca los intentos de apertura de objetos que producen un error con ACCESS \_ DENIED y errores similares.<br/>                                                                                                                                                               |
| Denegar AEE                 | Si un objeto tiene ACE de denegación en su DACL, deniega explícitamente el acceso a entidades específicas. <br/> Esto no es habitual y dificulta la predicción, por lo que LuaPriv marca Denegar ACE cuando las encuentra.<br/>                                                                                                                                                                                                                                                                     |
| Acceso restringido         | Si una aplicación intenta abrir un objeto para los derechos que no se conceden a los usuarios normales (por ejemplo, al intentar escribir en un archivo que solo pueden escribir los administradores), es probable que la aplicación no funcione igual cuando se ejecuta como un usuario normal. <br/> LuaPriv marca estas operaciones.<br/>                                                                                                                                                                      |
| MÁXIMO \_ PERMITIDO          | Si una aplicación abre un objeto para MAXIMUM ALLOWED, la comprobación de acceso real en el objeto \_ se producirá en otro lugar. La mayoría del código que lo hace no funciona correctamente y casi seguro que funcionará de forma diferente cuando se ejecute sin privilegios. <br/> LuaPriv marca así todos los incidentes de MAXIMUM \_ ALLOWED. <br/>                                                                                                                                                            |



 

Los problemas que se pasan por alto normalmente se capturan en las comprobaciones erróneas nebulosas:

-   Detalles de detenciones de API peligrosas
-   Detalles de detenciones de pilas desatendadas
-   Subrecuper de hora

Hemos agregado un nuevo comprobador de impresión. Esta capa ayuda a buscar y solucionar problemas que pueden producirse cuando una aplicación llama al subsistema de impresión. El comprobador de impresión tiene como destino las dos capas del subsistema de impresión, la capa PrintAPI y la capa PrintDriver.

*Capa de API de impresión*

Print Verifier prueba la interfaz entre un programa y Winspool.drv y prntvpt.dll prueba las interfaces de esos archivos DLL. Puede revisar las reglas para llamar a funciones en esta interfaz en la sección de ayuda de MSDN para las API exportadas por winspool.drv y prntvpt.dll.

*Imprimir capa de controlador*

Print Verifier también prueba la interfaz entre un controlador de impresión principal, como UNIDRV.DLL, UNIDRUI.DLL, PSCRIPT5.DLL, PS5UI.DLL o MXDWDRV.DLL, y los complementos del controlador de impresión. Puede encontrar información sobre esta interfaz en MSDN y WDK.

Tenga en cuenta que algunas de estas comprobaciones son solo para Windows 7 y otras simplemente tendrán un mejor rendimiento en Windows 7.

Normalmente, solo las versiones de depuración ejecutan Application Verifier, por lo que el rendimiento no suele ser un problema. Si surgen problemas de rendimiento por el uso de este o cualquier otro Application Verifier comprobación, ejecute una comprobación a la vez hasta que haya realizado todas las comprobaciones necesarias.

Casi el 10 % de los bloqueos de aplicaciones en Windows se deben a daños en el montón. Estos bloqueos son casi imposibles de depurar después del hecho. La mejor manera de evitar estos problemas es probar con las características del montón de páginas que se encuentran en Application Verifier. Hay dos tipos de montón de páginas: "Full" y "Light". Full es el valor predeterminado; obligará a un depurador a detenerse al instante al detectar daños. Esta característica DEBE ejecutarse mientras se encuentra en el depurador. Sin embargo, también es el recurso más exigente. Si un usuario tiene problemas de tiempo y ya ha ejecutado un escenario en el montón de páginas "Completa", establecerlo en "Light" probablemente solucionará estos problemas. Además, el montón de páginas ligeras no se bloquea hasta que se cierra el proceso. Proporciona un seguimiento de pila a la asignación, pero puede tardar considerablemente más tiempo en diagnosticar que aprovechar su homólogo full.

Supervise el estado de confiabilidad de las aplicaciones a través del portal web winqual. En este portal se muestran los informes de errores recopilados Informe de errores de Windows, por lo que es fácil identificar los errores más frecuentes. Obtenga información sobre esto en Informe de errores de Windows: Tareas iniciales. Microsoft no cobra por este servicio.

Para aprovechar las ventajas de WinQual, debe:

1.  Registre su empresa para WinQual, que requiere un identificador de VeriSign. Puede encontrar información Windows 7 sobre WinQual en el portal para desarrolladores agrupado en Windows Vista SP1 \\ Windows Server 2008. Pronto tendrá una ubicación Windows 7.
2.  Asigne las aplicaciones de ISV a un nombre de producto y el nombre del ISV, que vincula los informes de error a la empresa. Otros ISV no pueden ver los informes de errores.
3.  Use el portal para identificar los principales problemas. Los ISV también pueden crear respuestas que informan a los clientes sobre los pasos que deben seguirse después de un error. El sistema de respuesta admite más de 10 idiomas en todo el mundo.

Una nota adicional: Application Verifier solo es tan bueno como las rutas de acceso de código con las que se ejecuta. El valor de combinar esta herramienta con una herramienta de cobertura de código no se puede sobresalar.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

**Herramientas de depuración para Windows:**

-   [Información general y sitio de descarga](https://msdn.microsoft.com/windows/hardware/bg127145)
-   [Documentación en línea de MSDN](/windows-hardware/drivers/debugger/)

**Application Verifier:**

-   [Información general](/previous-versions/ms220948(v=vs.80))
-   [Descargar](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&amp;DisplayLang=en)
-   [Application Verifier para Microsoft Visual Studio 2008/.NET Framework 3.5](/previous-versions/ms220948(v=vs.80))

    **Nota:** la Application Verifier que se incluye en Visual Studio está bastante fechada. Si es posible, use el paquete independiente en su lugar. Por esta razón, las versiones futuras de Visual Studio ya no tendrán Application Verifier.

**WinQual:**

-   [Windows Quality Online Services (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)
-   [Informe de errores de Windows: Tareas iniciales](../wer/using-wer.md)

 

 
