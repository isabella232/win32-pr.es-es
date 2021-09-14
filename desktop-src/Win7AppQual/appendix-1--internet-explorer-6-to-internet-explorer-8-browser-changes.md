---
description: En la tabla siguiente se describen los cambios entre Microsoft Internet Explorer 6 y Windows Internet Explorer 8.
ms.assetid: 5A7DDFC4-69A4-4B5A-9C0A-6172E2142494
title: Cambios en el explorador de IE 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7abf978d2211a03b59a78847a66efc21f3213c41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249422"
---
# <a name="appendix-1-internet-explorer-6-to-internet-explorer-8-browser-changes"></a>Apéndice 1: Internet Explorer 6 a Internet Explorer 8 cambios en el explorador

En la tabla siguiente se describen los cambios entre Microsoft Internet Explorer 6 y Windows Internet Explorer 8.



Diseño de cambios de Internet Explorer 6 a Internet Explorer 7

Cambios de diseño de Internet Explorer 7 a Internet Explorer 8

${ROWSPAN2}$Internet Explorer versioning${REMOVE}$  

Compruebe si hay código que no sea correcto para casos especiales en torno a Internet Explorer 6, Windows Internet Explorer 7 o Internet Explorer 8 a través del control de cadenas de agente de [usuario, vectores](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))de versiones o comentarios condicionales .

-   Cuando una cadena larga del Agente de usuario (UA) encuentra un servidor que solo acepta cadenas de UA más cortas, los usuarios ven [una página de error](https://www.enhanceie.com/ua.aspx).

<!-- -->

-   El Vista de compatibilidad en Internet Explorer 8, que está activado de forma predeterminada para los sitios de intranet, envía una Internet Explorer agente de usuario 7. Para diferenciar entre Internet Explorer 7 y Vista de compatibilidad, busque el nuevo [token de Trident.](/archive/blogs/ie/)

${ROWSPAN3}$ Actualizaciones de cumplimiento de estándares

-   Se aplica a [los modos de documento especificados.](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85))
-   [Internet Explorer modo 8 Vista de compatibilidad](/archive/blogs/ie/), que está en modo predeterminado para los sitios de intranet, normalmente revierte las actualizaciones de estándares de [Internet Explorer 7 a Internet Explorer 8](/archive/blogs/ie/site-compatibility-and-ie8).
-   Use el encabezado HTTP compatible con [X-UA EmulaIE7](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) o **el elemento meta** para habilitar Vista de compatibilidad sitios web o páginas web específicas.

${REMOVE}$  

Excepción de modo de quirks: no es necesario realizar cambios de cumplimiento de estándares para las páginas web que especifican el modo quirks DOCTYPE (estableciendo el modificador DOCTYPE "standards-compliance" en "off").

Se aplica al modo "Estricto" o Estándar de Internet Explorer 7 y posteriores:

-   [Los prólogos XML](/previous-versions/windows/internet-explorer/ie-developer/) de la primera línea del código fuente ya no provocan errores en las declaraciones DOCTYPE.
-   [El contenido de desbordamiento](/previous-versions/windows/internet-explorer/ie-developer/) del modelo de cuadro forma una intersección con el cuadro y ya no aumenta automáticamente el contenido del elemento div del cuadro.
-   [No se admiten](/previous-versions/windows/internet-explorer/ie-developer/) determinados filtros CSS (por ejemplo, HTML, carácter de subrayado y \* \_ \* \* //comentario).
-   [Solo se crea una instancia del elemento OBJECT](/previous-versions/windows/internet-explorer/ie-developer/) más externo de los objetos anidados.
-   [Las aplicaciones que se basan](/previous-versions/windows/internet-explorer/ie-developer/) en el elemento SELECT para obtener un HWND para usarlo con las API de Microsoft Win32 pueden interrumpirse porque el elemento [SELECT](/archive/blogs/ie/) es ahora un control sin ventanas.
-   No se admite el formato de definición de canal [(CDF),](/previous-versions/aa740486(v=msdn.10)) en favor de las fuentes RSS.
-   [XBM,](/previous-versions/aa740486(v=msdn.10))un formato de creación de imágenes diseñado para sistemas basados en X, no se admite.
-   [No se](/previous-versions/aa740486(v=msdn.10)) permiten etiquetas BASE fuera del documento HEAD.

Se aplica al modo Estándar de Internet Explorer 8 y posteriores:

-   [Los elementos P sin](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) cerrar se cierran automáticamente cuando van seguidos de [**elementos TABLE**](https://msdn.microsoft.com/library/ms535901(v=VS.85).aspx), [**FORM,**](https://msdn.microsoft.com/library/ms535249(v=VS.85).aspx) [**NOFRAMES**](https://msdn.microsoft.com/library/ms535857(v=VS.85).aspx) [**o NOSCRIPT.**](https://msdn.microsoft.com/library/ms535858(v=VS.85).aspx)
-   [No se admite HTML con](/archive/blogs/ie/site-compatibility-and-ie8) formato correcto, en favor del marcado válido y correcto.
-   No se admite la sintaxis del atributo ["className",](/archive/blogs/ie/site-compatibility-and-ie8) en favor de la sintaxis "class".
-   [La colección de atributos](/archive/blogs/ie/site-compatibility-and-ie8) no contiene todos los atributos posibles que Windows Internet Explorer reconoce.
-   [La ordenación de atributos ha cambiado,](/archive/blogs/ie/site-compatibility-and-ie8)lo que afecta a la colección de atributos, innerHTML y outerHTML.
-   [GetElementById distingue mayúsculas](/archive/blogs/ie/site-compatibility-and-ie8) de minúsculas y no busca atributos de nombre.
-   [No se admiten selectores de](/archive/blogs/ie/site-compatibility-and-ie8) prefijo CSS genéricos (es decir, v : sintaxis), en favor de \\ nombres de etiqueta \* explícitos.
-   [No se admiten expresiones CSS,](/archive/blogs/ie/site-compatibility-and-ie8) en favor de la compatibilidad mejorada con CSS o la lógica DHTML.
-   El código destinado a métodos de objeto JSON personalizados podría estar en conflicto con el nuevo objeto [JSON nativo](/archive/blogs/ie/site-compatibility-and-ie8) Internet Explorer 8.
-   [Las propiedades iniciales de unset](/archive/blogs/ie/site-compatibility-and-ie8) en el objeto currentStyle devuelven su valor inicial.
-   [Los valores](/archive/blogs/ie/site-compatibility-and-ie8) de propiedades no especificados en el objeto de estilo de objeto currentStyle devuelven una cadena vacía (por ejemplo, vea la entrada de blog del problema de representación en blanco del menú [ASP.NET e IE8).](/archive/blogs/giorgio/)

<!-- -->

-   Para sitios y aplicaciones en los que la accesibilidad es un problema, actualice la [sintaxis de ARIA](/archive/blogs/ie/)en todos Internet Explorer modos de representación .
-   Compruebe la [lista completa de actualizaciones de CSS de Internet Explorer 6 a Internet Explorer 8](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx).

Mejoras de seguridad

-   Se aplica independientemente del modo de documento.
-   Puede desactivar las características de seguridad mediante [directiva de grupo](https://www.microsoft.com/p/group-policy/9wzdncrfjtm4?activetab=pivot:overviewtab).

<!-- -->

-   No [se permite la omisión de window.opener](/previous-versions/aa740486(v=msdn.10)) al símbolo del sistema window.close.
-   [](/previous-versions/windows/internet-explorer/ie-developer/) La protección de almacenamiento en caché de objetos está habilitada de forma predeterminada, lo que bloquea el acceso a las referencias de objetos cuando los usuarios navegan a un nuevo dominio (se aplica a Internet Explorer 6 y versiones posteriores en Windows XP con Service Pack 2 (SP2) y versiones posteriores).
-   [Los scriptlets DHTML están deshabilitados](/previous-versions/windows/internet-explorer/ie-developer/) de forma predeterminada.
-   [Los scripts que escriben en la barra de estado](/previous-versions/windows/internet-explorer/ie-developer/) están bloqueados.
-   [La creación de direcciones URL podría producir un error](/previous-versions/windows/internet-explorer/ie-developer/) si las direcciones URL no cumplen las directrices de RFC.
-   Las [páginas HTTPS](/previous-versions/windows/internet-explorer/ie-developer/) muestran una página de error si el sitio está configurado solo para SSLv2, o si el certificado de seguridad del sitio no está actualizado o no es válido, tiene errores o tiene cifrados débiles.
-   Solo se admiten nombres de dominio [internacionalizados codificados "Punycode".](/previous-versions/windows/internet-explorer/ie-developer/) Otros formatos como ANSI y UTF-8 están bloqueados.
-   [Se bloquean las direcciones URL de script entre](/previous-versions/windows/internet-explorer/ie-developer/)dominios, la navegación redirigida en objetos DOM y las navegaciones de fotogramas.
-   [Los cuadros de diálogo modales o](/previous-versions/aa740486(v=msdn.10)) no modales que se crean a partir del script pueden parecer [ligeramente más grandes.](/archive/blogs/ie/)
-   [Los protocolos no](/previous-versions/aa740486(v=msdn.10)) seguros view-source, Gopher (en el nivel WinINET) y Telnet no funcionan.

<!-- -->

-   El filtro [XSS](/archive/blogs/ie/) está en activarse de forma predeterminada, lo que bloquea los patrones de script que suelen parecerse a ataques XSS de tipo 1, a menos que los deshabilite a través de un encabezado HTTP X-XSS-Protection.
-   No se admiten ataques de comunicación entre dominios y documentos, como [SCRIPT SRC,](/archive/blogs/jscript/) en favor de características de AJAX XDM y XDR más [seguras.](/archive/blogs/ie/)
-   La nueva propiedad de navegación window.location.hash podría dividir los sitios habilitados para AJAX que manipulan manualmente el [hash](/previous-versions//cc891506(v=vs.85)) de la dirección URL.
-   [Las nuevas características de AJAX,](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) [como XDM,](/archive/blogs/ie/) tienen [**propiedades nativas**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc288548(v=vs.85)) que podrían estar en conflicto con las propiedades personalizadas existentes.
-   [El control de carga](/archive/blogs/ie/) de archivos envía solo la ruta de acceso del archivo, no la ruta de acceso completa, al servidor.
-   Se bloquea la ejecución de código HTML o script que se entrega con un [tipo \* MIME "image/".](/archive/blogs/ie/)
-   [Al navegar por un marco de nivel](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565638(v=vs.85)) superior a un sitio en un contexto de seguridad diferente, se abre una nueva ventana o pestaña en lugar de navegar dentro del marco existente.
-   [El script con codificación UTF-7](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565635(v=vs.85)) se fuerza en la codificación Windows-1252, lo que podría provocar la representación de texto sin formato.
-   [Las páginas "modo mixto" HTTP/HTTPS](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0) muestran un cuadro de diálogo que muestra de forma predeterminada solo elementos seguros (frente al valor predeterminado anterior no seguro). Los usuarios podrían elegir por error [bloquear elementos HTTP,](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0)como imágenes clave.
-   [DEP/NX](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#depnx)está encendido de forma predeterminada, lo que impide que determinados complementos (es decir, controles ActiveX y objetos COM) creados mediante versiones anteriores de ATL ejecuten código marcado como "no ejecutable" en memoria.
-   [El contenido devuelto por un proxy web](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565641(v=vs.85)) se bloquea si no se establece un túnel SSL en respuesta a una solicitud CONNECT al servidor original.

Cambios de arquitectura

-   Se aplica independientemente del documento o del modo de compatibilidad.

<!-- -->

-   [El modo protegido](/previous-versions/windows/internet-explorer/ie-developer/) está habilitado de forma predeterminada para las zonas [De Internet, Intranet y Sitios restringidos.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537187(v=vs.85)) Este [](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565645(v=vs.85)) modo impide que las extensiones del explorador que podrían suponer un riesgo de seguridad al ejecutar aplicaciones con privilegios más bajos accedan a procesos con privilegios más [altos,](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565646(v=vs.85))como menú Inicio, Panel de control y el Registro de Microsoft Windows (se aplica a Internet Explorer 7 y versiones posteriores en Windows Vista y versiones posteriores).

<!-- -->

-   [Actualización del modo protegido:](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565648(v=vs.85))la intranet se ejecuta en un nivel de integridad medio (en lugar de bajo) de forma predeterminada.
-   [Las Internet Explorer](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#lcie) de acoplamiento flexible pueden bloquear complementos (es decir, controles ActiveX y objetos COM) que realicen una de las siguientes acciones:
    -   Use técnicas de jerarquía de windows para buscar ventanas de tabulación y marco de interfaz de usuario (que ahora se ejecutan en procesos independientes en distintos niveles de integridad).
    -   Cree una subclase del marco de interfaz de usuario (ahora en el nivel de integridad medio) a partir de un proceso de pestaña de baja integridad.
    -   Use técnicas de mensajería no admitidas entre el marco de interfaz de usuario y las pestañas.



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Abordar la compatibilidad de aplicaciones al migrar a Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 
