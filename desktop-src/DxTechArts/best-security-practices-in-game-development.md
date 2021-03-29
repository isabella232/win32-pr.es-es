---
title: Procedimientos de seguridad recomendados en el desarrollo de juegos
description: En este artículo se describen los procedimientos recomendados para usar en el desarrollo de juegos.
ms.assetid: 20956529-42ed-722b-cfa3-e3230d89fdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba4f02d5e1a2e3da2e50feedd89f085a0c063be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904693"
---
# <a name="best-security-practices-in-game-development"></a>Procedimientos de seguridad recomendados en el desarrollo de juegos

En este artículo se describen los procedimientos recomendados para usar en el desarrollo de juegos.

-   [Introducción](#introduction)
-   [Ejemplos de código no seguro](#examples-of-insecure-code)
-   [Formas de mejorar la seguridad](#ways-to-improve-security)
-   [Resumen](#summary)

## <a name="introduction"></a>Introducción

Un número creciente de personas Juega juegos y juegos en línea con contenido realizado por el usuario. Esto, combinado con la creciente seguridad del sistema operativo Microsoft Windows, significa que los juegos son un objetivo cada vez mayor y más tentador para que los atacantes los aprovechen. Los desarrolladores de juegos deben poner un énfasis fuerte en asegurarse de que los juegos que liberan no crean nuevos agujeros de seguridad para que los atacantes puedan aprovecharlos. Los desarrolladores de juegos tienen una responsabilidad y un interés atribuido para evitar que los equipos de sus clientes se consuman contra ataques de datos de red malintencionados, modificaciones de usuarios o alteraciones. Si se aprovecha una vulnerabilidad, podría provocar la pérdida de clientes o dinero. En este artículo se describen y se explican algunos métodos y herramientas comunes para aumentar la seguridad del código sin tener que aumentar el tiempo de desarrollo.

Los tres errores más comunes que realiza un equipo de desarrollo al publicar un producto son:

-   Requiere privilegios administrativos. Los juegos no deben requerir privilegios administrativos. Para obtener más información, consulte [control de cuentas de usuario para desarrolladores de juegos](./user-account-control-for-game-developers.md).
-   No se usa la protección automatizada. Por lo general, los desarrolladores no usan **/GS**, **/SAFESEH** o **/NX**. El uso de estas marcas de compilación o vínculo puede detectar o eliminar muchos agujeros de seguridad básicos sin aumentar significativamente la carga de trabajo. Estas marcas se describen más adelante en este artículo.
-   Usar las API prohibidas. Hay muchas API (**strcpy**, **strncpy**, etc.) que son propensos a errores del programador y generan fácilmente brechas de seguridad. Los desarrolladores deben reemplazar estas API por las versiones seguras. Visual Studio 2005 incluye una herramienta para analizar archivos binarios que pueden comprobar automáticamente si hay referencias a las API no seguras en los archivos objeto. Para obtener más información sobre qué hacer con la información generada con esta herramienta, vea [rechazar ataques en el código con las bibliotecas seguras de C y C++ de Visual Studio 2005](/archive/msdn-magazine/2005/may/repel-attacks-with-visual-studio-2005-safe-c-and-c-libraries) Martyn Lovell. Además, puede obtener el archivo de encabezado [. h prohibido](https://www.microsoft.com/downloads/details.aspx?FamilyID=6aed14bd-4766-4d9d-9ee2-fa86aad1e3c9) , que puede ayudarle a quitar funciones prohibidas del código.

Cada uno de los errores de la lista no solo es común, pero es fácil de corregir sin ningún cambio significativo en la carga de trabajo de desarrollo, los estándares de codificación o la funcionalidad.

## <a name="examples-of-insecure-code"></a>Ejemplos de código no seguro

A continuación se presenta un ejemplo sencillo de todo lo que se necesita para permitir que un atacante realice un ataque de saturación del búfer:


```
void GetPlayerName(char *pDatafromNet)
{
    char playername[256]; 
    strncpy(playername, pDatafromNet, strlen(pDatafromNet));

    // ...
}
```



En la superficie en la que este código es correcto, llama a una función segura, después de todo. Los datos de la red se copian en un búfer de 256 bytes. La función **strncpy** se basa en encontrar un terminador nulo en la cadena de origen o está limitado por el número de búferes proporcionado. El problema es que el tamaño del búfer es incorrecto. Si no se validan los datos de la red o el tamaño del búfer es incorrecto (como en este ejemplo), un atacante podría simplemente proporcionar un búfer grande para sobrescribir los datos de la pila, después de que el búfer acabe, con los datos del paquete de red. Esto permitiría que el atacante ejecutara código arbitrario sobrescribiendo el puntero de instrucción y cambiando la dirección de retorno. La lección más básica de este ejemplo es que nunca confíe en la entrada hasta que se haya comprobado.

Aunque los datos no provienen inicialmente de la red, todavía existe un riesgo potencial. El desarrollo de juegos modernos requiere que muchas personas diseñen, desarrollen y prueben la misma base de código. No hay ninguna manera de saber cómo se llamará a la función en el futuro. Pregunte siempre de dónde proceden los datos y qué podría controlar un atacante. Aunque los ataques basados en red son los más comunes, no son los únicos métodos de creación de carencias de seguridad. ¿Un atacante podría crear un mod o editar un archivo guardado de manera que se abra una brecha de seguridad? ¿Qué ocurre con los archivos de sonido y imagen proporcionados por el usuario? Las versiones malintencionadas de estos archivos se pueden publicar en Internet y crear riesgos de seguridad peligrosos para los clientes.

Como nota lateral, use strsafe. h o CRT seguro en lugar de **strncpy** para corregir el ejemplo. Safe CRT es una revisión de seguridad completa del tiempo de ejecución de C y se incluye en Visual Studio 2005. Puede encontrar más información acerca de Safe CRT en [mejoras de seguridad en el CRT](https://msdn.microsoft.com/library/8ef0s5kh(VS.80).aspx) de Michael Howard.

## <a name="ways-to-improve-security"></a>Formas de mejorar la seguridad

Hay varias maneras de mejorar la seguridad en el ciclo de desarrollo. Estas son algunas de las mejores maneras:

<dl> <dt>

<span id="Reading_about_security"></span><span id="reading_about_security"></span><span id="READING_ABOUT_SECURITY"></span>Leer sobre la seguridad
</dt> <dd>

En el libro, *escritura de código seguro, segunda edición* de Michael Howard y David LeBlanc, se proporciona una explicación detallada y clara de las estrategias y los métodos para evitar ataques y mitigar las vulnerabilidades de seguridad. A partir de los métodos de diseño de la seguridad en una versión a técnicas para proteger las aplicaciones de red, el libro cubre todos los aspectos que un desarrollador de juegos necesita para protegerse a sí mismo, a sus productos y a sus clientes de atacantes. El libro se puede usar para inculcarr una referencia cultural de seguridad en un desarrollo Studio. No solo piense en la seguridad del código como el problema de un desarrollador o el problema de un evaluador. Considere la seguridad como algo que todo el equipo, desde el administrador de programas hasta el diseñador hasta el evaluador, debe estar pensando en Cuándo funcionan en un proyecto. Cuanto más ojos formen parte del proceso de revisión, mayor será la posibilidad de detectar un agujero de seguridad antes del lanzamiento.

La *escritura de código seguro, la segunda edición* se puede encontrar en [Microsoft Learning](https://www.microsoftpressstore.com/store/writing-secure-code-9780735617223) y se puede encontrar información de seguridad más general a la vez que se [reduce la superficie expuesta a ataques a través](/previous-versions/ms972812(v=msdn.10)) de Michael Howard.

Michael Howard, David LeBlanc y John Viega han escrito otro libro sobre el asunto que abarca todos los sistemas operativos y lenguajes de programación comunes con derechos *de 19 Sins de seguridad de software*.

Las presentaciones de seguridad centradas en los juegos se pueden encontrar en la página de descarga de [presentaciones para desarrolladores de Microsoft XNA](/previous-versions/dn629515(v=msdn.10)) .

</dd> <dt>

<span id="Threat_Modeling_Analysis"></span><span id="threat_modeling_analysis"></span><span id="THREAT_MODELING_ANALYSIS"></span>Análisis de modelado de amenazas
</dt> <dd>

Un análisis de modelado de amenazas es una buena forma de evaluar la seguridad del sistema, no en un lenguaje específico o mediante una herramienta, sino en un método completo de un extremo a otro que se puede realizar en algunas reuniones. Cuando se implementa correctamente, un modelo de subprocesos puede identificar todos los puntos fuertes y débiles de un sistema, sin agregar una carga de trabajo significativa o una hora de reunión al proyecto. El método de modelado de amenazas también enfatiza la idea de evaluar la seguridad del sistema antes y durante el proceso de desarrollo para ayudar a garantizar que se realice una evaluación completa mientras se centra en las características más peligrosas. Puede considerarse como un generador de perfiles para la seguridad. Al no basarse en un lenguaje determinado o confiar en una herramienta específica, se puede usar el modelado de amenazas en cualquier estudio de desarrollo que trabaje en cualquier proyecto de cualquier género. El modelado de amenazas es también un método excelente para reforzar la idea de que la seguridad es responsabilidad de todo el mundo y no de otro problema.

Cuando el modelado de amenazas, preste especial atención a:

-   Orígenes de datos UDP
-   Orígenes de datos que no requieren autenticación
-   Orígenes de datos que se sondean con frecuencia y normalmente como parte de la recopilación de información de gran escala
-   Cualquier capacidad de un cliente para enviar datos directamente a otros clientes.

Estas son las áreas que tienen un buen potencial para los puntos débiles de seguridad.

Puede encontrar más información sobre el modelado de amenazas en el [modelo de amenazas](https://technet.microsoft.com/security/) en el centro de desarrollo de seguridad de MSDN y en el libro de [modelado de amenazas](https://www.amazon.com/Threat-Modeling-Microsoft-Professional-Swiderski/dp/0735619913) de Frank Swiderski y de la ventana Snyder.

</dd> <dt>

<span id="Data_Execution_Prevention___NX_"></span><span id="data_execution_prevention___nx_"></span><span id="DATA_EXECUTION_PREVENTION___NX_"></span>Prevención de ejecución de datos (/NX)
</dt> <dd>

Una herramienta reciente en la mitigación de varios ataques es la prevención de ejecución de datos (DEP). Si incluye el modificador **/NX** en el comando de compilación, Visual Studio marcará las páginas de memoria con marcas que denotan si el código tiene derecho a ejecutarse o no. Cualquier programa que intente ejecutarse en una página de memoria no marcada con el permiso de ejecución provocará una finalización forzosa del programa. La prevención se aplica en el nivel de procesador y afectará a los desarrolladores que utilicen código automodificante o compiladores de lenguaje JIT nativos. Actualmente, solo los procesadores Athlon64 y Opteron de AMD y los procesadores Intel Itanium y más recientes de Pentium 4 admiten la prevención de ejecución, pero se espera que todos los procesadores de 32 bits y 64 bits admitan la prevención de ejecución en el futuro. (Un esquema de protección de copia que usa un desarrollador puede verse afectado por la prevención de ejecución, pero Microsoft ha estado trabajando con proveedores de protección de copia para minimizar el impacto). Se recomienda usar DEP.

Para obtener más detalles sobre DEP, consulte [prevención de ejecución de datos](../memory/data-execution-prevention.md).

</dd> <dt>

<span id="Buffer_Security_Check___GS__and_Image_has_Safe_Exception_Handlers___SAFESEH_"></span><span id="buffer_security_check___gs__and_image_has_safe_exception_handlers___safeseh_"></span><span id="BUFFER_SECURITY_CHECK___GS__AND_IMAGE_HAS_SAFE_EXCEPTION_HANDLERS___SAFESEH_"></span>La comprobación de seguridad de búfer (/GS) y la imagen tienen controladores de excepciones seguros (/SAFESEH)
</dt> <dd>

La *comprobación de seguridad del búfer*, especificada por la marca de compilador **/GS**, y la *imagen tiene controladores de excepciones seguros*, especificados por la marca del enlazador **/SAFESEH** (que primero se implementó en Visual Studio .NET 2003), puede hacer que el trabajo del desarrollador proteja el código un poco más sencillo.

El uso de la marca **/GS** hace que el compilador construya una comprobación de algunas formas de saturaciones del búfer basado en la pila que podrían aprovecharse para sobrescribir la dirección de retorno de una función. El uso de **/GS** no detectará cada posible saturación del búfer y no debe considerarse una buena tecnología de defensa en profundidad.

El uso de la marca **/SAFESEH** indica al enlazador que solo genere un archivo ejecutable o dll si también puede generar una tabla de los controladores de excepciones seguros del archivo ejecutable o dll. El control de excepciones estructurado seguro (SafeSEH) elimina el control de excepciones como destino de los ataques de saturación del búfer asegurándose de que, antes de que se envíe una excepción, el controlador de excepciones se registre en la tabla de funciones ubicada en el archivo de imagen. Estas ventajas de protección se habilitan con Windows XP SP2, Windows Server 2003, Windows Vista y Windows 7. Además, para que **/SAFESEH** funcione correctamente, se debe usar en un método All-o-Nothing. Todas las bibliotecas que contienen código enlazado a un archivo ejecutable o DLL deben compilarse con **/SAFESEH** o la tabla no se generará.

Puede encontrar más información sobre la [comprobación de seguridad de búfer](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) (**/GS**) y la imagen de los [controladores de excepciones seguros](https://msdn.microsoft.com/library/9a89h429(vs.71).aspx) (**/SAFESEH**) en MSDN.

Vea también información sobre la [marca **/SDL**](/cpp/build/reference/sdl-enable-additional-security-checks?view=vs-2019) de Microsoft Visual Studio 2012 y las mejoras de Visual Studio 2012 [en la marca **/GS**](https://www.microsoft.com/security/blog/2012/01/26/enhancements-to-gs-in-visual-studio-11/).

</dd> <dt>

<span id="PREfast"></span><span id="prefast"></span><span id="PREFAST"></span>PREfast
</dt> <dd>

PREfast es una herramienta gratuita ofrecida por Microsoft que analiza las rutas de acceso de ejecución de C o C++ compiladas para ayudar a encontrar errores en tiempo de ejecución. La función PREfast funciona a través de todas las rutas de ejecución en todas las funciones y la evaluación de cada ruta de acceso. Usado originalmente para desarrollar controladores y otro código de kernel, esta herramienta puede ayudar a los desarrolladores de juegos a ahorrar tiempo eliminando algunos errores que son difíciles de encontrar o que el compilador pasa por alto. Usar la velocidad rápida es una forma excelente de reducir la carga de trabajo y de centrar los esfuerzos del equipo de desarrollo y del equipo de pruebas. PREfast está disponible en Visual Studio Team Suite y Visual Studio Team Edition para Software Developers como análisis de código, habilitado por el modificador del compilador **/Analyze**. (Esta opción también está disponible en la versión gratuita del compilador que se incluye con el kit de desarrollo de software de Windows).

> [!Note]  
> Visual Studio 2012 admite **/Analyze** en todas las ediciones. Para obtener más información sobre la disponibilidad del análisis de código en todas las ediciones de Visual Studio, vea [novedades del análisis de código](/archive/blogs/codeanalysis/?m=20123).

 

Mediante el uso de la anotación de encabezado (especialmente en el caso de los argumentos de puntero de búfer), la rápida puede exponer otros problemas, como errores de sobrescritura de memoria, una fuente común de bloqueos y posibles vulnerabilidades de seguridad. Esto se hace mediante el lenguaje de anotación estándar (SAL), que es una forma de marcado para prototipos de funciones de C/C++ que proporcionan información adicional sobre la semántica esperada de los argumentos de puntero y la correlación con parámetros de longitud, tamaños de búfer declarados, etc. Se anotan todos los encabezados de los sistemas operativos Windows y la adición de la marca SAL en los encabezados de API públicas de sus propias bibliotecas permite realizar comprobaciones más detalladas y agresivas en el código de cliente para dichas API. Para ver una introducción a SAL y vínculos a más información, consulte la entrada de blog de Michael Howard, "[Introducción breve al lenguaje de anotación estándar (sal)](/archive/blogs/michael_howard/a-brief-introduction-to-the-standard-annotation-language-sal)".

</dd> <dt>

<span id="Windows_Application_Verifier"></span><span id="windows_application_verifier"></span><span id="WINDOWS_APPLICATION_VERIFIER"></span>comprobador de aplicaciones de Windows
</dt> <dd>

Windows comprobador de aplicaciones, o AppVerifier, pueden ayudar a los evaluadores proporcionando varias funciones en una herramienta. AppVerifier es una herramienta que se desarrolló para que los errores comunes de programación sean más comprobables. AppVerifier puede comprobar los parámetros que se pasan a las llamadas API, inyectar entradas erróneas para comprobar la capacidad de control de errores y registrar los cambios en el registro y el sistema de archivos. AppVerifier también puede detectar saturaciones de búfer en el montón, comprobar que se ha definido correctamente una lista de Access Control (ACL) y aplicar el uso seguro de las API de socket. Aunque no es exhaustivo, AppVerifier puede ser una herramienta en el cuadro de herramientas del evaluador para ayudar a una versión de Development Studio a un producto de calidad.

Para obtener más información acerca de comprobador de aplicaciones, vea [Comprobador de aplicaciones](/previous-versions/visualstudio/visual-studio-2008/ms220948(v=vs.90)) y [uso de Comprobador de aplicaciones dentro del ciclo de vida de desarrollo de software](/previous-versions/aa480483(v=msdn.10)) en MSDN.

</dd> <dt>

<span id="Fuzz_Testing"></span><span id="fuzz_testing"></span><span id="FUZZ_TESTING"></span>Pruebas de aproximación
</dt> <dd>

La *prueba aproximada* es un método semiautomatizado de pruebas que puede mejorar las metodologías de pruebas actuales. La idea central detrás de las pruebas aproximadas consiste en realizar una evaluación completa de todas las entradas mediante la entrada de datos aleatorios para ver qué interrupciones se producen. Esto incluye todos los datos de red, mods y juegos guardados, etc. La prueba aproximada es bastante fácil de hacer. Simplemente modifique los archivos con formato correcto o los datos de red insertando bytes aleatorios, volteando bytes adyacentes o negando valores numéricos. 0xFF, 0xFFFF, 0xFFFFFFFF, 0x00, 0x0000, 0x00000000 y 0x80000000 son valores que son buenos en la exposición de los agujeros de seguridad durante las pruebas aproximadas. Puede observar las combinaciones de interacción resultantes mediante AppVerifier. Aunque la aproximación no es exhaustiva, es fácil de implementar y automatizar, y puede detectar los errores más escurridizoss e imprevisibles.

Para obtener más información sobre las pruebas aproximadas, vea la presentación de [Gamefest 2007](/previous-versions/dn629515(v=msdn.10)) *pasos prácticos de la seguridad de juegos*.

</dd> <dt>

<span id="Authenticode_Signing"></span><span id="authenticode_signing"></span><span id="AUTHENTICODE_SIGNING"></span>Firma de Authenticode
</dt> <dd>

Authenticode es un método para garantizar que los archivos ejecutables, los archivos DLL y los paquetes de Windows Installer (archivos. msi) que recibe el usuario no se modifican de lo que un desarrollador ha publicado. Mediante el uso de una combinación de principios criptográficos, entidades de confianza y estándares del sector, Authenticode comprueba la integridad del contenido ejecutable. Microsoft proporciona una API criptográfica, CryptoAPI, que se puede usar para detectar automáticamente la alteración del código firmado. Si se produce una fuga de seguridad después de una versión, se puede revocar un certificado y todo el código firmado con ese certificado dejará de autenticarse. Al revocar un certificado, se revocará la validación de todos los títulos firmados con ese certificado. Windows se ha diseñado para trabajar con la firma Authenticode y alerta a un usuario de código sin firmar, en situaciones específicas, que podría exponer el equipo de un usuario para atacar.

Authenticode no debe considerarse un método para eliminar los problemas de seguridad, sino un método para detectar la alteración después de liberar un ejecutable. Un archivo ejecutable o DLL que contenga un problema de seguridad aprovechable puede firmarse y comprobarse mediante Authenticode, pero seguirá introduciendo el problema de seguridad en el nuevo sistema. Solo después de que se haya comprobado que un producto o actualización es seguro, debe firmarse el código para garantizar que los usuarios tengan una versión que no se haya alterado.

Incluso si un desarrollador considera que no hay ninguna amenaza de que se modifiquen sus versiones, otras tecnologías y servicios se basan en Authenticode. La firma de código es fácil de integrar y automatizar; no hay ningún motivo por el que los desarrolladores no tengan las versiones firmadas.

Para obtener más información sobre la firma Authenticode, consulte [firma de Authenticode para desarrolladores de juegos](./authenticode-signing-for-game-developers.md).

</dd> <dt>

<span id="Minimize_Privileges"></span><span id="minimize_privileges"></span><span id="MINIMIZE_PRIVILEGES"></span>Minimizar privilegios
</dt> <dd>

En general, los procesos deben ejecutarse con el conjunto mínimo de privilegios necesarios para funcionar. En Windows Vista y Windows 7, esto se logra mediante el [control de cuentas de usuario](./user-account-control-for-game-developers.md), lo que permite que el juego se ejecute como un usuario estándar en lugar de un administrador. En Windows XP, normalmente los juegos siempre se ejecutan como administrador. Incluso en Windows Vista y Windows 7, a veces es necesario elevar a derechos de administrador completos para algunas operaciones específicas.

En los casos en los que el proceso se ejecuta con derechos administrativos completos, normalmente solo se necesitan unos pocos derechos más allá de los de un usuario estándar. El acceso administrativo incluye muchos derechos que no son necesarios para el código legítimo, pero que un atacante podría usar a través de alguna debilidad del proceso. Entre los ejemplos de estos derechos SE incluyen las siguientes: \_ Take \_ Ownership, se \_ depure, se \_ crea \_ token, se \_ ASSIGNPRIMARYTOKEN, se ha \_ \_ descargado, se seguridad de se, se ha \_ cargado el \_ controlador, es SYSTEMTIME, se realiza \_ \_ una copia de seguridad, se restaura, se \_ \_ cierra y se \_ audita (consulte [constantes de privilegio](../secauthz/privilege-constants.md)).

Aunque un proceso no puede obtener más derechos una vez que se inicia, puede otorgar derechos fácilmente. En el inicio, el proceso puede utilizar inmediatamente las API de Win32 para quitar los derechos que no necesita.

</dd> <dt>

<span id="Utilize_Windows_Security_Features"></span><span id="utilize_windows_security_features"></span><span id="UTILIZE_WINDOWS_SECURITY_FEATURES"></span>Uso de las características de seguridad de Windows
</dt> <dd>

Windows Vista y Windows 7 incluyen una serie de características nuevas que mejoran la seguridad del código. El [control de cuentas de usuario](./user-account-control-for-game-developers.md) es ciertamente el más importante que debe comprender y adoptar, pero también hay otras características. Además de las tecnologías de Windows XP SP2, como firewall de Windows, prevención de ejecución de datos, comprobación de seguridad de búfer y controladores de excepciones seguros que también están disponibles en Windows Vista y Windows 7, hay tres características de seguridad más recientes que se deben tener en cuenta:

-   La característica de selección aleatoria del diseño del espacio de direcciones de participación. Esto se habilita mediante la vinculación con la opción **/dynamicbase** en visual Studio 2005 Service Pack 1 o visual Studio 2008. Esto hace que el sistema aleatoriza las posiciones de muchos de los archivos DLL del sistema clave en el espacio de proceso, lo que dificulta mucho más la escritura de programas de ataque explotables que se propagan en gran medida a través de Internet. Windows XP y versiones anteriores de Windows omiten esta marca del enlazador.
-   Los daños en el montón pueden dar lugar a una clase completa de vulnerabilidades de seguridad, por lo que el sistema de memoria de Windows Vista y Windows 7 ahora es compatible con un modo que finaliza el proceso si se detectan daños en el montón. La llamada a [**HeapSetInformation**](/windows/win32/api/heapapi/nf-heapapi-heapsetinformation) con **HeapEnableTermianteOnCorruption** le permitirá participar en este comportamiento. Se produce un error en esta llamada en Windows XP y en la versión anterior de Windows.
-   Al escribir servicios, se pueden configurar con una característica nueva para especificar los privilegios que se requieren realmente, así como para limitar el acceso a los recursos a un SID específico. Esto se hace a través de [ChangeSeviceConfig2](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a), mediante la \_ configuración \_ de servicio \_ \_ información de privilegios necesaria y la información del SID del servicio de configuración de servicio \_ \_ \_ \_ .

</dd> </dl>

## <a name="summary"></a>Resumen

Desarrollar un juego para el Marketplace actual y futuro es costoso y lento. Publicar un juego con problemas de seguridad supondrá en última instancia más dinero y tiempo para corregirlos correctamente. Por lo tanto, está en interés de que todos los desarrolladores de juegos integren herramientas y técnicas para mitigar las vulnerabilidades de seguridad antes del lanzamiento.

La información de este artículo es una introducción a lo que puede hacer un estudio de desarrollo para ayudarlo a sí mismo y a sus clientes. Puede encontrar más información sobre los procedimientos de seguridad generales y la información de seguridad en el [Centro para desarrolladores de seguridad de Microsoft](https://technet.microsoft.com/security/).

 

 