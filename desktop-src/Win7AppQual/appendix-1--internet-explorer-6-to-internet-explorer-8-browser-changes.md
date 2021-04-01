---
description: En la tabla siguiente se describen los cambios entre Microsoft Internet Explorer 6 y Windows Internet Explorer 8.
ms.assetid: 5A7DDFC4-69A4-4B5A-9C0A-6172E2142494
title: Cambios del explorador de IE 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7abf978d2211a03b59a78847a66efc21f3213c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103909974"
---
# <a name="appendix-1-internet-explorer-6-to-internet-explorer-8-browser-changes"></a>Apéndice 1: cambios del explorador de Internet Explorer 6 a Internet Explorer 8

En la tabla siguiente se describen los cambios entre Microsoft Internet Explorer 6 y Windows Internet Explorer 8.



Cambios de diseño de Internet Explorer 6 a Internet Explorer 7

Cambios de diseño de Internet Explorer 7 a Internet Explorer 8

$ {ROWSPAN2} $Internet Explorer control de versiones $ {REMOVE} $  

Busque código que tenga casos especiales incorrectamente relacionados con Internet Explorer 6, Windows Internet Explorer 7 o Internet Explorer 8 a través [del examen de cadenas de agente de usuario, vectores de versiones o Comentarios condicionales](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85)).

-   Cuando una cadena de agente de usuario largo (UA) encuentra un servidor que solo acepta cadenas de UA más cortas, los usuarios verán [una página de error](https://www.enhanceie.com/ua.aspx).

<!-- -->

-   La vista de compatibilidad de Internet Explorer 8, que está activada de forma predeterminada para los sitios de intranet, envía una cadena de agente de usuario de Internet Explorer 7. Para diferenciar entre Internet Explorer 7 y la vista de compatibilidad, busque el nuevo [token Trident](/archive/blogs/ie/).

$ {ROWSPAN3} $ actualizaciones de cumplimiento de estándares

-   Se aplica a los [modos de documento especificados](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)).
-   El [modo vista de compatibilidad de Internet Explorer 8](/archive/blogs/ie/), que está activado de forma predeterminada para los sitios de intranet, normalmente [revierte las actualizaciones de estándares de Internet Explorer 7 a Internet Explorer 8](/archive/blogs/ie/site-compatibility-and-ie8).
-   Use el encabezado HTTP o el elemento **meta** [EMULATEIE7 X-UA-compatible](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) para habilitar la vista de compatibilidad en sitios web o páginas web específicas.

$ {REMOVE} $  

Excepción del modo no estándar: no es necesario realizar cambios de cumplimiento de normas para las páginas web que especifican el DOCTYPE del modo no estándar (estableciendo el modificador de documento de cumplimiento de estándares en "desactivado").

Se aplica al modo "Estricto" o Estándar de Internet Explorer 7 y posteriores:

-   Los [proregistros XML](/previous-versions/windows/internet-explorer/ie-developer/) en la primera línea del código fuente ya no hacen que se produzca un error en las declaraciones DOCTYPE.
-   El contenido de desbordamiento del [modelo de cuadros](/previous-versions/windows/internet-explorer/ie-developer/) se cruza y ya no aumenta automáticamente el div de caja para ajustarse al contenido.
-   [Ciertos filtros CSS](/previous-versions/windows/internet-explorer/ie-developer/) (por ejemplo, \* HTML, \_ carácter de subrayado y/ \* \* /comentario) no se admiten.
-   Solo se crea una instancia [del elemento de objeto externo en objetos anidados](/previous-versions/windows/internet-explorer/ie-developer/) .
-   [Las aplicaciones que se basan en el elemento Select](/previous-versions/windows/internet-explorer/ie-developer/) para obtener un HWND para usarlo con las API de Microsoft Win32 podrían interrumpirse porque el [elemento Select](/archive/blogs/ie/) es ahora un control sin ventana.
-   El [formato de definición de canal (CDF)](/previous-versions/aa740486(v=msdn.10)) no se admite, en favor de fuentes RSS.
-   [XBM](/previous-versions/aa740486(v=msdn.10)), un formato de imagen diseñado para sistemas basados en X, no se admite.
-   No se permiten [etiquetas base](/previous-versions/aa740486(v=msdn.10)) fuera del documento principal.

Se aplica al modo Estándar de Internet Explorer 8 y posteriores:

-   [Los elementos P](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) no cerrados se cierran automáticamente cuando van seguidos de elementos de [**tabla**](https://msdn.microsoft.com/library/ms535901(v=VS.85).aspx), [**formulario**](https://msdn.microsoft.com/library/ms535249(v=VS.85).aspx), [**noframes**](https://msdn.microsoft.com/library/ms535857(v=VS.85).aspx)o [**NoScript**](https://msdn.microsoft.com/library/ms535858(v=VS.85).aspx) .
-   No se admite [HTML con formato](/archive/blogs/ie/site-compatibility-and-ie8) incorrecto, en favor del marcado válido y con formato correcto.
-   No se admite la sintaxis de [atributo "className"](/archive/blogs/ie/site-compatibility-and-ie8) , en favor de la sintaxis de "class".
-   [La colección de atributos](/archive/blogs/ie/site-compatibility-and-ie8) no contiene todos los atributos posibles que reconoce Windows Internet Explorer.
-   El orden de los [atributos ha cambiado](/archive/blogs/ie/site-compatibility-and-ie8), lo que afecta a la colección de atributos, innerHTML y outerHTML.
-   [GetElementById](/archive/blogs/ie/site-compatibility-and-ie8) distingue mayúsculas de minúsculas y no busca atributos de nombre.
-   Los [selectores de prefijos CSS genéricos](/archive/blogs/ie/site-compatibility-and-ie8) (es decir, v \\ : \* Syntax) no se admiten, en favor de los nombres de etiqueta explícitos.
-   No se admiten las [expresiones CSS](/archive/blogs/ie/site-compatibility-and-ie8) , en favor de la compatibilidad mejorada con CSS o la lógica DHTML.
-   El código que está destinado a los métodos de objeto JSON personalizados puede entrar en conflicto con el [nuevo objeto JSON nativo](/archive/blogs/ie/site-compatibility-and-ie8) en Internet Explorer 8.
-   Si no se [anulan las propiedades iniciales](/archive/blogs/ie/site-compatibility-and-ie8) del objeto currentstyle devuelven, se devuelve su valor inicial.
-   [Los valores de las propiedades no especificadas](/archive/blogs/ie/site-compatibility-and-ie8) en el objeto de estilo de objeto currentstyle devuelven devuelven una cadena vacía (por ejemplo, consulte el menú ASP.net y la entrada de blog sobre la [representación de IE8 en blanco](/archive/blogs/giorgio/) ).

<!-- -->

-   En el caso de los sitios y las aplicaciones en los que la accesibilidad es un problema, actualice la [Sintaxis de Aria en todos los modos de representación de Internet Explorer](/archive/blogs/ie/).
-   Consulte la [lista completa de actualizaciones de CSS de Internet Explorer 6 a Internet Explorer 8](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx).

Mejoras de seguridad

-   Se aplica independientemente del modo de documento.
-   Puede desactivar las características de seguridad mediante [Directiva de grupo](https://www.microsoft.com/p/group-policy/9wzdncrfjtm4?activetab=pivot:overviewtab).

<!-- -->

-   No se permite la omisión de [window. Opener](/previous-versions/aa740486(v=msdn.10)) en el símbolo del sistema Window. Close.
-   La [protección del almacenamiento en caché de objetos](/previous-versions/windows/internet-explorer/ie-developer/) está habilitada de forma predeterminada, lo que bloquea el acceso a las referencias de objetos cuando los usuarios navegan a un nuevo dominio (se aplica a Internet Explorer 6 y versiones posteriores en Windows XP con Service Pack 2 (SP2) y versiones posteriores).
-   Los [scriptlets DHTML](/previous-versions/windows/internet-explorer/ie-developer/) están deshabilitados de forma predeterminada.
-   [Los scripts que escriben en la barra de estado](/previous-versions/windows/internet-explorer/ie-developer/) están bloqueados.
-   [Podría producirse un error](/previous-versions/windows/internet-explorer/ie-developer/) en la creación de direcciones URL si las direcciones URL no cumplen las directrices de RFC.
-   [Las páginas HTTPS muestran una página de error](/previous-versions/windows/internet-explorer/ie-developer/) si el sitio está configurado para SSLv2 solo, o si el certificado de seguridad del sitio está obsoleto o no es válido, tiene errores o tiene cifrados débiles.
-   Solo se admiten [nombres de dominio internacionalizados codificados con "Punycode"](/previous-versions/windows/internet-explorer/ie-developer/) . Otros formatos como ANSI y UTF-8 están bloqueados.
-   Las [direcciones URL de script entre dominios](/previous-versions/windows/internet-explorer/ie-developer/), la navegación redirigida en objetos DOM y las navegaciones de fotogramas están bloqueadas.
-   Los [cuadros de diálogo modales o no modales](/previous-versions/aa740486(v=msdn.10)) que se crean a partir de script pueden parecer [ligeramente más grandes](/archive/blogs/ie/).
-   Los [protocolos no seguros](/previous-versions/aa740486(v=msdn.10)) View-source, Gopher (en el nivel WinINET) y telnet no funcionan.

<!-- -->

-   El [filtro XSS](/archive/blogs/ie/) está activado de forma predeterminada, lo que impide que los patrones de script se parezcan a los ataques XSS de tipo 1, a menos que los deshabilite a través de un encabezado HTTP X-XSS-Protection.
-   No se admiten ataques de comunicación entre dominios y entre documentos, como [script src](/archive/blogs/jscript/) , en favor de las características más seguras de [XDM y XDR Ajax](/archive/blogs/ie/).
-   Los sitios habilitados para AJAX que [manipulan manualmente el hash de la dirección URL](/previous-versions//cc891506(v=vs.85)) podrían estar rotos por la nueva propiedad de navegación Window. Location. hash.
-   [Las nuevas características de Ajax](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) como [XDM](/archive/blogs/ie/) tienen [**propiedades nativas**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc288548(v=vs.85)) que pueden entrar en conflicto con las propiedades personalizadas existentes.
-   El [control de carga de archivos](/archive/blogs/ie/) solo envía al servidor la ruta de acceso del archivo, no la ruta de acceso completa.
-   No se pudo ejecutar el código HTML o el script que se entrega con un [ \* tipo MIME "Image/"](/archive/blogs/ie/) .
-   Al [navegar por un marco de nivel superior](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565638(v=vs.85)) a un sitio en un contexto de seguridad diferente, se abre una nueva ventana o pestaña en lugar de navegar dentro del marco existente.
-   El [script codificado UTF-7](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565635(v=vs.85)) se fuerza a la codificación Windows-1252, lo que podría producir una representación de texto sin formato.
-   [Las páginas http/https "modo mixto"](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0) muestran un cuadro de diálogo que tiene como valor predeterminado Mostrar solo los elementos seguros (frente a los valores predeterminados no seguros anteriores). Los usuarios pueden [optar por erróneas a bloquear elementos http](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0), como imágenes de clave.
-   [DEP/NX está activado de forma predeterminada](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#depnx), lo que impide que determinados complementos (es decir, controles ActiveX y objetos com) compilados con versiones anteriores de ATL ejecuten código marcado como "no ejecutable" en la memoria.
-   El [contenido devuelto por un proxy web](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565641(v=vs.85)) se bloquea si no se establece un túnel SSL en respuesta a una solicitud de conexión al servidor original.

Cambios de arquitectura

-   Se aplica independientemente del documento o del modo de compatibilidad.

<!-- -->

-   El [modo protegido](/previous-versions/windows/internet-explorer/ie-developer/) está habilitado de forma predeterminada para las [zonas de Internet, intranet y sitios restringidos](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537187(v=vs.85)). Este modo [bloquea las extensiones del explorador que podrían suponer un riesgo para la seguridad](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565645(v=vs.85)) que impiden que las aplicaciones con privilegios de ejecución y [menos tengan acceso a procesos de privilegios más elevados](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565646(v=vs.85)), como el menú Inicio, el panel de control y el registro de Microsoft Windows (se aplica a Internet Explorer 7 y versiones posteriores en Windows Vista y versiones posteriores).

<!-- -->

-   [Actualización en modo protegido](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565648(v=vs.85)): la intranet se ejecuta de forma predeterminada en el nivel de integridad medio (en lugar de bajo).
-   [Internet Explorer de acoplamiento flexible](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#lcie) podría bloquear complementos (es decir, controles ActiveX y objetos com) que realizan una de las acciones siguientes:
    -   Use las técnicas de la jerarquía de Windows para buscar el marco de interfaz de usuario y las ventanas de pestaña (que ahora se ejecutan en procesos independientes con diferentes niveles de integridad).
    -   Cree una subclase del marco de la interfaz de usuario (ahora en el nivel de integridad medio) desde un proceso de la pestaña de integridad baja.
    -   Usar técnicas de mensajería no admitidas entre las pestañas y el marco de la interfaz de usuario.



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Abordar la compatibilidad de aplicaciones al migrar a Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 
