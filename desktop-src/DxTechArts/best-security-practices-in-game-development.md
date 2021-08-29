---
title: Procedimientos de seguridad recomendados en el desarrollo de juegos
description: En este artículo se de abordan los procedimientos recomendados para usarlos en el desarrollo de juegos.
ms.assetid: 20956529-42ed-722b-cfa3-e3230d89fdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4890030dc66277b3b4e4e63861a23fdc2776a357c2054b183041e2dd8cb6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051205"
---
# <a name="best-security-practices-in-game-development"></a>Procedimientos de seguridad recomendados en el desarrollo de juegos

En este artículo se de abordan los procedimientos recomendados para usarlos en el desarrollo de juegos.

-   [Introducción](#introduction)
-   [Ejemplos de código no seguro](#examples-of-insecure-code)
-   [Formas de mejorar la seguridad](#ways-to-improve-security)
-   [Resumen](#summary)

## <a name="introduction"></a>Introducción

Un número creciente de personas reproduce juegos y juegos en línea con contenido realizado por el usuario. Esto, combinado con la seguridad creciente del sistema operativo microsoft Windows, significa que los juegos son un objetivo cada vez mayor y más tentador para que los atacantes puedan aprovecharse. Los desarrolladores de juegos deben hacer especial hincapié en asegurarse de que los juegos que lanzan no crean nuevos huecos de seguridad para que los atacantes puedan aprovecharlos. Los desarrolladores de juegos tienen una responsabilidad y un interés en ayudar a evitar que los equipos de sus clientes sean hackeados por datos de red malintencionados, modificaciones de usuarios o alteraciones. Si se aprovecha una vulnerabilidad, podría provocar la pérdida de clientes o dinero. En este artículo se describen algunos métodos y herramientas comunes para aumentar la seguridad del código sin aumentar en exceso el tiempo de desarrollo.

Los tres errores más comunes que comete un equipo de desarrollo al lanzar un producto son:

-   Requerir privilegios administrativos. Los juegos no deben requerir privilegios administrativos. Para más información, consulte [Control de cuentas de usuario para desarrolladores de juegos.](./user-account-control-for-game-developers.md)
-   No se usa la protección automatizada. Por lo general, los desarrolladores **no usan /GS,** **/SAFESEH** o **/NX.** El uso de estas marcas de compilación o vínculo puede detectar o eliminar muchos huecos de seguridad básicos sin aumentar significativamente la carga de trabajo. Estas marcas se de abordan más adelante en este artículo.
-   Uso de API prohibidas. Hay muchas API **(strcpy,** **strncpy,** y así sucesivamente) que son propensas a errores del programador y generan fácilmente problemas de seguridad. Los desarrolladores deben reemplazar estas API por las versiones seguras. Visual Studio 2005 incluye una herramienta para analizar archivos binarios que pueden comprobar automáticamente los archivos de objeto en busca de referencias a API no seguras. Para obtener más información sobre qué hacer con la información generada con esta herramienta, vea Ataques a su código con las bibliotecas de [Visual Studio 2005 Caja fuerte C](/archive/msdn-magazine/2005/may/repel-attacks-with-visual-studio-2005-safe-c-and-c-libraries) y C++ de Codn Lovell. Además, puede obtener el archivo [de encabezado banned.h](https://www.microsoft.com/downloads/details.aspx?FamilyID=6aed14bd-4766-4d9d-9ee2-fa86aad1e3c9) que puede ayudarle a quitar las funciones prohibidas del código.

Cada uno de los errores enumerados no solo es común, sino que se puede corregir fácilmente sin ningún cambio significativo en la carga de trabajo de desarrollo, los estándares de codificación o la funcionalidad.

## <a name="examples-of-insecure-code"></a>Ejemplos de código no seguro

A continuación se muestra un ejemplo sencillo de todo lo que se necesita para permitir que un atacante realice un ataque de saturación del búfer:


```
void GetPlayerName(char *pDatafromNet)
{
    char playername[256]; 
    strncpy(playername, pDatafromNet, strlen(pDatafromNet));

    // ...
}
```



En la superficie, este código parece correcto: llama a una función segura, después de todo. Los datos de la red se copian en un búfer de 256 bytes. La **función strncpy** se basa en la búsqueda de un terminador NULL en la cadena de origen o está limitada por el recuento de búferes proporcionado. El problema es que el tamaño del búfer es incorrecto. Si no se validan los datos de la red o el tamaño del búfer es incorrecto (como en este ejemplo), un atacante podría simplemente proporcionar un búfer grande para sobrescribir los datos de la pila, una vez que finalice el búfer, con cualquier dato en el paquete de red. Esto permitiría al atacante ejecutar código arbitrario sobrescribiendo el puntero de instrucción y cambiando la dirección de devolución. La lección más básica de este ejemplo es no confiar nunca en la entrada hasta que se haya comprobado.

Incluso si los datos no proceden inicialmente de la red, existe un riesgo potencial. El desarrollo de juegos modernos requiere que muchas personas diseñe, desarrollen y prueban la misma base de código. No hay ninguna manera de saber cómo se llamará a la función en el futuro. Pregúntese siempre de dónde provenían los datos y ¿qué podría controlar un atacante? Aunque los ataques basados en red son los más comunes, no son los únicos métodos para crear huecos de seguridad. ¿Podría un atacante crear un mod o editar un archivo guardado de forma que se abra un hueco de seguridad? ¿Qué sucede con los archivos de imagen y sonido proporcionados por el usuario? Las versiones malintencionadas de estos archivos podrían publicarse en Internet y crear riesgos de seguridad peligrosos para los clientes.

Como nota lateral, use strsafe.h o Caja fuerte CRT en lugar de **strncpy** para corregir el ejemplo. Caja fuerte CRT es una revisión de seguridad completa del entorno de ejecución de C y viene con parte de Visual Studio 2005. Puede encontrar más información Caja fuerte CRT en [Mejoras de seguridad en CRT](https://msdn.microsoft.com/library/8ef0s5kh(VS.80).aspx) de Michael Howard.

## <a name="ways-to-improve-security"></a>Formas de mejorar la seguridad

Hay varias maneras de mejorar la seguridad en el ciclo de desarrollo. Estas son algunas de las mejores maneras:

<dl> <dt>

<span id="Reading_about_security"></span><span id="reading_about_security"></span><span id="READING_ABOUT_SECURITY"></span>Lectura sobre la seguridad
</dt> <dd>

El libro *Writing Secure Code, Second Edition* (Escritura de código seguro, segunda edición), de Michael Howard y David LePlot, proporciona una explicación detallada y clara de las estrategias y los métodos para evitar ataques y mitigar las vulnerabilidades de seguridad. A partir de los métodos de diseño de seguridad en una versión para técnicas de protección de aplicaciones de red, el libro trata todos los aspectos que un desarrollador de juegos necesita para ayudar a protegerse a sí mismo, sus productos y sus clientes de los atacantes. El libro se puede usar para crear una cultura de seguridad en un estudio de desarrollo. No piense simplemente en la seguridad del código como un problema de un desarrollador o un problema del evaluador. Piense en la seguridad como algo en lo que todo el equipo, desde el administrador de programas hasta el diseñador y el desarrollador hasta el evaluador, debe pensar en cuándo trabaja en un proyecto. Cuando más ojos forman parte del proceso de revisión, mayor será la posibilidad de detectar un hueco de seguridad antes del lanzamiento.

*Escribir código seguro, segunda* edición se puede encontrar en [Microsoft Learning](https://www.microsoftpressstore.com/store/writing-secure-code-9780735617223) [](/previous-versions/ms972812(v=msdn.10)) y puede encontrar información de seguridad más general en La protección frente a ataques futuros mediante la reducción de la superficie de ataque de Michael Howard.

Michael Howard, David LeSeguridad y John Viega han escrito otro libro sobre el tema que trata todos los sistemas operativos comunes y los lenguajes de programación *titulados 19 Deadly Sins of Software Security*.

Las presentaciones de seguridad centradas en los juegos se pueden encontrar en la página [de descarga de Microsoft XNA Developer Presentations.](/previous-versions/dn629515(v=msdn.10))

</dd> <dt>

<span id="Threat_Modeling_Analysis"></span><span id="threat_modeling_analysis"></span><span id="THREAT_MODELING_ANALYSIS"></span>Análisis de modelado de amenazas
</dt> <dd>

Un análisis de modelado de amenazas es una buena manera de evaluar la seguridad del sistema, no en un lenguaje específico o mediante una herramienta, sino en un método amplio y completo que se puede lograr en algunas reuniones. Cuando se implementa correctamente, un modelo de subprocesos puede identificar todos los puntos fuertes y débiles de un sistema, sin agregar una carga de trabajo significativa ni tiempo de reunión al proyecto. El método de modelado de amenazas también resalta la idea de evaluar la seguridad del sistema antes y durante el proceso de desarrollo para ayudar a garantizar que se realiza una evaluación completa al tiempo que se centra en las características más arriesgadas. Se puede pensar en como un profiler para la seguridad. Al no basarse en un lenguaje determinado o confiar en una herramienta específica, el modelado de amenazas se puede usar en cualquier estudio de desarrollo que trabaje en cualquier proyecto de cualquier género. El modelado de amenazas también es un método excelente para reforzar la idea de que la seguridad es responsabilidad de todos y no del problema de otra persona.

Al modelar amenazas, preste especial atención a:

-   Orígenes de datos UDP
-   Orígenes de datos que no requieren autenticación
-   Orígenes de datos que se sondean con frecuencia y normalmente como parte de la recopilación de información a gran escala
-   Cualquier capacidad de un cliente para enviar datos directamente a otros clientes

Estas son las áreas que tienen un buen potencial para los puntos débiles de seguridad.

Puede encontrar más información sobre el modelado de amenazas en [El](https://technet.microsoft.com/security/) modelado de amenazas en el Centro de desarrollo de seguridad de MSDN y en el libro [Modelado](https://www.amazon.com/Threat-Modeling-Microsoft-Professional-Swiderski/dp/0735619913) de amenazas de Frank Swiderski y Window Snyder.

</dd> <dt>

<span id="Data_Execution_Prevention___NX_"></span><span id="data_execution_prevention___nx_"></span><span id="DATA_EXECUTION_PREVENTION___NX_"></span>Prevención de ejecución de datos (/NX)
</dt> <dd>

Una herramienta reciente para mitigar varias vulnerabilidades de seguridad es la prevención de ejecución de datos (DEP). Si incluye el modificador **/NX** en el comando de compilación, Visual Studio marcará las páginas de memoria con marcas que denota si el código tiene derecho a ejecutarse o no. Cualquier programa que intente ejecutarse en una página de memoria no marcada con el permiso EXECUTE provocará una finalización forzosa del programa. La prevención se aplica en el nivel de procesador y afectará a los desarrolladores que usan código auto modifying o compiladores nativos del lenguaje JIT. Actualmente, solo los procesadores Athlon64 y Opteron de AMD y los procesadores Itanium y Pentium 4 más recientes de Intel admiten la prevención de ejecución, pero se espera que todos los procesadores de 32 y 64 bits admitan la prevención de ejecución en el futuro. (Un esquema de protección de copia utilizado por un desarrollador puede verse afectado por la prevención de ejecución, pero Microsoft ha estado trabajando con proveedores de protección de copia para minimizar el impacto). Es un procedimiento recomendado usar DEP.

Para obtener más información sobre DEP, vea [Prevención de ejecución de datos.](../memory/data-execution-prevention.md)

</dd> <dt>

<span id="Buffer_Security_Check___GS__and_Image_has_Safe_Exception_Handlers___SAFESEH_"></span><span id="buffer_security_check___gs__and_image_has_safe_exception_handlers___safeseh_"></span><span id="BUFFER_SECURITY_CHECK___GS__AND_IMAGE_HAS_SAFE_EXCEPTION_HANDLERS___SAFESEH_"></span>Buffer Security Check (/GS) and Image has Caja fuerte Exception Handlers (/SAFESEH)
</dt> <dd>

*La* comprobación de seguridad del búfer , especificada por la marca del compilador **/GS**, y la imagen tiene controladores de excepciones de Caja fuerte , *especificados* por la marca del vinculador **/SAFESEH** (implementada por primera vez en Visual Studio .NET 2003), pueden facilitar un poco el trabajo del desarrollador de proteger el código.

El uso **de la marca /GS** hace que el compilador cree una comprobación de algunas formas de saturaciones de búfer basadas en la pila que podrían aprovecharse para sobrescribir la dirección de devolución de una función. El **uso de /GS** no detectará todas las posibles saturaciones del búfer y no debe considerarse como un control general, sino una buena tecnología de defensa en profundidad.

El uso de la marca **/SAFESEH** indicará al vinculador que solo genere un archivo ejecutable o DLL si también puede generar una tabla de los controladores de excepciones seguros del archivo ejecutable o dll. Caja fuerte El control estructurado de excepciones (SafeSEH) elimina el control de excepciones como destino de ataques de saturación de búfer al garantizar que, antes de enviar una excepción, el controlador de excepciones se registra en la tabla de funciones ubicada en el archivo de imagen. Estas ventajas de protección se habilitan con Windows XP SP2, Windows Server 2003, Windows Vista y Windows 7. Además, **para que /SAFESEH** funcione correctamente, debe usarse en un método all-or-nothing. Todas las bibliotecas que contienen código enlazado a un archivo ejecutable o DLL deben compilarse con **/SAFESEH** o no se generará la tabla.

Puede encontrar más información sobre [la comprobación](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) de seguridad de búfer (**/GS**) e [Image has Caja fuerte Exception Handlers](https://msdn.microsoft.com/library/9a89h429(vs.71).aspx) (**/SAFESEH**) en MSDN.

Consulte también información sobre la Microsoft Visual Studio [ **/SDL**](/cpp/build/reference/sdl-enable-additional-security-checks?view=vs-2019) de Microsoft Visual Studio 2012 y las mejoras de Visual Studio 2012 en la [ **marca /GS**](https://www.microsoft.com/security/blog/2012/01/26/enhancements-to-gs-in-visual-studio-11/).

</dd> <dt>

<span id="PREfast"></span><span id="prefast"></span><span id="PREFAST"></span>PREfast
</dt> <dd>

PREfast es una herramienta gratuita que ofrece Microsoft y que analiza las rutas de ejecución en C o C++ compilados para ayudar a encontrar errores en tiempo de ejecución. PREfast funciona trabajando a través de todas las rutas de ejecución en todas las funciones y evaluando cada ruta de acceso para ver si hay problemas. Usada originalmente para desarrollar controladores y otro código kernel, esta herramienta puede ayudar a los desarrolladores de juegos a ahorrar tiempo mediante la eliminación de algunos errores que son difíciles de encontrar o que el compilador ignora. El uso de PREfast es una excelente manera de reducir la carga de trabajo y centrar los esfuerzos tanto del equipo de desarrollo como del equipo de prueba. PREfast está disponible en Visual Studio Team Suite y Visual Studio Team Edition para Software Developers como Code Analysis, habilitado por el modificador del compilador **/analyze**. (Esta opción también está disponible en la versión gratuita del compilador que se incluye con Windows Kit de desarrollo de software).

> [!Note]  
> Visual Studio 2012 admite **/analyze** en todas las ediciones. Para obtener más información sobre la disponibilidad del análisis de código en todas las ediciones de Visual Studio, vea Novedades [de Code Analysis](/archive/blogs/codeanalysis/?m=20123).

 

Mediante el uso de la anotación de encabezado (especialmente para los argumentos de puntero de búfer), PREfast puede exponer problemas adicionales, como errores de sobrescritura de memoria, una fuente común de bloqueos y posibles vulnerabilidades de seguridad. Para ello, se usa el Lenguaje de anotación estándar (SAL), que es una forma de marcado para prototipos de función de C/C++ que proporcionan información adicional sobre la semántica esperada de argumentos de puntero y la correlación con parámetros de longitud, tamaños de búfer declarados, etc. Se anotan todos los encabezados de los sistemas operativos de Windows y la adición de marca sal en encabezados de API públicas en sus propias bibliotecas permite a PREfast realizar comprobaciones más detalladas y agresivas en el código de cliente para dichas API. Para obtener una introducción a SAL y vínculos a más información, vea la entrada de blog de Michael Howard,["A Brief Introduction to the Standard Annotation Language (SAL)](/archive/blogs/michael_howard/a-brief-introduction-to-the-standard-annotation-language-sal)." (Una breve introducción al lenguaje de anotación estándar [SAL]).

</dd> <dt>

<span id="Windows_Application_Verifier"></span><span id="windows_application_verifier"></span><span id="WINDOWS_APPLICATION_VERIFIER"></span>Windows Application Verifier
</dt> <dd>

El Windows Application Verifier, o AppVerifier, puede ayudar a los evaluadores proporcionando varias funciones en una herramienta. AppVerifier es una herramienta que se desarrolló para que los errores de programación comunes se puedan probar. AppVerifier puede comprobar los parámetros pasados a las llamadas API, insertar entradas erróneas para comprobar la capacidad de control de errores y registrar cambios en el registro y el sistema de archivos. AppVerifier también puede detectar saturaciones de búfer en el montón, comprobar que se ha definido correctamente una lista de Access Control (ACL) y aplicar el uso seguro de las API de socket. Aunque no es exhaustiva, AppVerifier puede ser una herramienta en el cuadro de herramientas del evaluador para ayudar a un estudio de desarrollo a lanzar un producto de calidad.

Para obtener más información sobre [](/previous-versions/visualstudio/visual-studio-2008/ms220948(v=vs.90)) Application Verifier, vea Application Verifier y Uso de Application Verifier dentro del ciclo de vida de desarrollo [de software](/previous-versions/aa480483(v=msdn.10)) en MSDN.

</dd> <dt>

<span id="Fuzz_Testing"></span><span id="fuzz_testing"></span><span id="FUZZ_TESTING"></span>Pruebas aproximadas
</dt> <dd>

*Las pruebas aproximadas* son un método de pruebas semiauto automated que puede mejorar las metodologías de pruebas actuales. La idea central detrás de las pruebas aproximadas es realizar una evaluación completa de todas las entradas mediante la entrada de datos aleatorios para ver qué se interrumpe. esto incluye todos los datos de red, mods y juegos guardados, etc. Las pruebas aproximadas son bastante fáciles de hacer. Simplemente modifique los archivos o datos de red correctos insertando bytes aleatorios, volteando bytes adyacentes o negando valores numéricos. 0xff, 0xffff, 0xffffffff, 0x00, 0x0000, 0x00000000 y 0x80000000 son valores que son buenos para exponer los huecos de seguridad durante las pruebas aproximadas. Puede observar las combinaciones de interacción resultantes mediante AppVerifier. Aunque la información aproximada no es exhaustiva, es fácil de implementar y automatizar, y puede detectar los errores más elusivos e impredecibles.

Para obtener más información sobre las pruebas aproximadas, vea la presentación [de Gamefest 2007](/previous-versions/dn629515(v=msdn.10)) *Pasos prácticos en seguridad de juegos.*

</dd> <dt>

<span id="Authenticode_Signing"></span><span id="authenticode_signing"></span><span id="AUTHENTICODE_SIGNING"></span>Firma de Authenticode
</dt> <dd>

Authenticode es un método para garantizar que los archivos ejecutables, los archivos DLL y los paquetes del instalador de Windows (.msi) que recibe el usuario no se alteren desde lo que un desarrollador publicó. Al usar una combinación de principios criptográficos, entidades de confianza y estándares del sector, Authenticode comprueba la integridad del contenido ejecutable. Microsoft proporciona una API criptográfica, CryptoAPI, que se puede usar para detectar automáticamente la manipulación de código firmado. Si se produce una pérdida de seguridad después de una versión, se puede revocar un certificado y todo el código firmado con ese certificado dejará de autenticarse. Revocar un certificado revocará la validación de todos los títulos firmados con ese certificado. Windows se ha diseñado para trabajar con la firma Authenticode y avisará a un usuario de código sin firmar, en situaciones específicas, que podría exponer el equipo de un usuario a ataques.

Authenticode no debe considerarse un método para eliminar problemas de seguridad, sino un método para detectar la manipulación después de que se haya publicado un archivo ejecutable. Un archivo ejecutable o DLL que contiene un problema de seguridad que se puede aprovechar se puede firmar y comprobar mediante Authenticode, pero seguirá incorporando el problema de seguridad al nuevo sistema. Solo después de comprobar que un producto o actualización es seguro, el código debe firmarse para garantizar a los usuarios que tienen una versión que no se ha alterado.

Incluso si un desarrollador considera que no hay ninguna amenaza de que se modifiquen sus versiones, otras tecnologías y servicios dependen de Authenticode. La firma de código es fácil de integrar y automatizar; no hay ninguna razón para que los desarrolladores no tengan sus versiones firmadas.

Para obtener más información sobre la firma de Authenticode, vea [Firma de Authenticode para desarrolladores de juegos.](./authenticode-signing-for-game-developers.md)

</dd> <dt>

<span id="Minimize_Privileges"></span><span id="minimize_privileges"></span><span id="MINIMIZE_PRIVILEGES"></span>Minimizar privilegios
</dt> <dd>

En general, los procesos deben ejecutarse con el conjunto mínimo de privilegios necesarios para funcionar. En Windows Vista y Windows 7, esto se logra mediante el [control](./user-account-control-for-game-developers.md)de cuentas de usuario, lo que permite que el juego se ejecute como un usuario estándar en lugar de como administrador. Para Windows XP, normalmente los juegos siempre se ejecutan como administrador. Incluso en Windows Vista y Windows 7, a veces es necesario elevar a derechos de administrador completos para algunas operaciones específicas.

En los casos en los que el proceso se ejecuta con derechos administrativos completos, normalmente solo se necesitan algunos derechos más allá de los de un usuario estándar. El acceso administrativo incluye muchos derechos que no son necesarios para el código legítimo, pero que un atacante podría usar, a través de algún punto débil del proceso. Algunos ejemplos de estos derechos son SE \_ TAKE \_ OWNERSHIP, SE \_ DEBUG, SE \_ CREATE \_ TOKEN, SE \_ ASSIGNPRIMARYTOKEN, SE \_ TCB, SE \_ SECURITY, SE LOAD \_ \_ DRIVER, SE \_ SYSTEMTIME, SE \_ BACKUP, SE RESTORE, SE SHUTDOWN y SE AUDIT \_ \_ \_ (consulte [Constantes Priviledge).](../secauthz/privilege-constants.md)

Aunque un proceso no puede obtener más derechos una vez iniciado, puede dejar de tener derechos fácilmente. En el inicio, el proceso puede usar inmediatamente las API de Win32 para quitar los derechos que no necesita.

</dd> <dt>

<span id="Utilize_Windows_Security_Features"></span><span id="utilize_windows_security_features"></span><span id="UTILIZE_WINDOWS_SECURITY_FEATURES"></span>Uso de Seguridad de Windows características
</dt> <dd>

Windows Vista y Windows 7 incluyen una serie de nuevas características que mejoran la seguridad del código. [El control de cuentas](./user-account-control-for-game-developers.md) de usuario es sin duda el más importante que se debe comprender y adoptar, pero también hay otras características. Además de las tecnologías de Windows XP SP2, como firewall de Windows, prevención de ejecución de datos, comprobación de seguridad de búfer y controladores de excepciones de Caja fuerte que también están disponibles en Windows Vista y Windows 7, hay tres características de seguridad más recientes que se deben tener en cuenta:

-   Característica de selección aleatoria del diseño del espacio de direcciones. Esto se habilita mediante la vinculación con la opción **/DYNAMICBASE** en Visual Studio 2005 Service Pack 1 o Visual Studio 2008. Esto hace que el sistema aleatorice las posiciones de muchos de los archivos DLL clave del sistema en el espacio de proceso, lo que hace que sea mucho más difícil escribir programas de ataques que se puedan aprovechar y que se propaguen ampliamente por Internet. Esta marca de vinculador se omite en Windows XP y versiones anteriores de Windows.
-   Los daños en el montón pueden dar lugar a una clase completa de vulnerabilidades de seguridad, por lo que el sistema de memoria de Windows Vista y Windows 7 ahora admite un modo que finaliza el proceso si se detectan daños en el montón. Llamar [**a HeapSetInformation**](/windows/win32/api/heapapi/nf-heapapi-heapsetinformation) **con HeapEnableTermianteOnCorruption** participará en este comportamiento. Se produce un error en esta Windows XP y la versión anterior de Windows.
-   Al escribir servicios, se pueden configurar mediante una nueva característica para especificar qué privilegios son realmente necesarios, así como para limitar el acceso a los recursos a un SID específico. Esto se realiza a través [de ChangeSeviceConfig2,](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a)mediante SERVICE CONFIG REQUIRED PRIVILEGES INFO y \_ SERVICE CONFIG SERVICE \_ \_ \_ \_ \_ \_ SID \_ INFO.

</dd> </dl>

## <a name="summary"></a>Resumen

Desarrollar un juego para el marketplace actual y futuro es costoso y lento. Lanzar un juego con problemas de seguridad en última instancia costará más dinero y tiempo para corregirlo correctamente. Por lo tanto, es en interés de todos los desarrolladores de juegos integrar herramientas y técnicas para mitigar las vulnerabilidades de seguridad antes del lanzamiento.

La información de este artículo es simplemente una introducción a lo que un estudio de desarrollo puede hacer para ayudarse a sí mismo y a sus clientes. Puede encontrar más información sobre las prácticas de seguridad generales y la información de seguridad en [el Centro para desarrolladores de seguridad de Microsoft](https://technet.microsoft.com/security/).

 

 