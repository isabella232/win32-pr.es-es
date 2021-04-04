---
title: Preguntas más frecuentes sobre DirectX
description: Este artículo contiene una colección de preguntas más frecuentes (p + f) acerca de Microsoft DirectX.
ms.assetid: 58d9fe45-a2c7-8280-2826-e2e14ecea983
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd5fd70f1a651121b8d977dbb9479cef6edd024
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078033"
---
# <a name="directx-frequently-asked-questions"></a>Preguntas más frecuentes sobre DirectX

Este artículo contiene una colección de preguntas más frecuentes (p + f) acerca de Microsoft DirectX.

-   [Problemas generales de desarrollo de DirectX](#general-directx-development-issues)
-   [Preguntas de Direct3D](#direct3d-questions)
    -   [Preguntas generales sobre Direct3D](#general-direct3d-questions)
    -   [Procesamiento de geometría (vértice)](#geometry-vertex-processing)
    -   [Optimización del rendimiento](#performance-tuning)
    -   [Biblioteca de utilidades de D3DX](#d3dx-utility-library)
-   [Preguntas sobre DirectSound](#directsound-questions)
-   [Extensiones de DirectX para el alias Maya](#directx-extensions-for-alias-maya)
-   [Preguntas sobre XInput](#xinput-questions)

## <a name="general-directx-development-issues"></a>Problemas generales de desarrollo de DirectX

<dl> <dt>

<span id="Should_game_developers_really_care_about_supporting_x64_editions_"></span><span id="should_game_developers_really_care_about_supporting_x64_editions_"></span><span id="SHOULD_GAME_DEVELOPERS_REALLY_CARE_ABOUT_SUPPORTING_X64_EDITIONS_"></span>**¿Los desarrolladores de juegos deben tener la misma atención sobre la compatibilidad con las ediciones x64?**
</dt> <dd>

Totalmente. la tecnología x64 está ampliamente disponible en el mercado. La mayoría de las nuevas CPU vendidas en los últimos años, y casi todas las líneas de procesador en desarrollo de AMD e Intel, son compatibles con x64. Windows XP Professional x64 Edition presentó la tecnología de habilitación del sistema operativo para x64 Publicada en abril de 2005. Dado que las ediciones x64 requieren una nueva generación de controladores nativos de 64 bits, esta primera versión se limitaba a la distribución de OEM.

Con Windows Vista, los clientes pueden elegir las ediciones de 32 bits o 64 bits al adquirir equipos basados en Windows, y las licencias de Windows Vista son válidas para las ediciones de 32 bits o de 64 bits del sistema operativo. Además, muchos controladores de 64 bits están disponibles en el cuadro, y los fabricantes de dispositivos deben proporcionar controladores nativos de 32 bits y de 64 bits como parte del programa de certificación de Windows.

Todos estos factores aumentarán considerablemente las implementaciones de las ediciones de 64 bits de Windows. A medida que los nuevos equipos empiecen a distribuirse con más de 2 GB de RAM física, el incentivo para usar un sistema operativo de 32 bits disminuirá considerablemente en favor de las ediciones de 64 bits. La tecnología de 64 bits es totalmente compatible con el código nativo de 32 bits, aunque se requieren implementaciones nativas de 64 bits para sacar el máximo partido del nuevo espacio de memoria de 64 bits. Cada aplicación de 32 bits debe tener compatibilidad de 64 bits como requisito de envío mínimo y cumplir este requisito es un requisito básico para la compatibilidad con Windows Vista. Las incompatibilidades suelen surgir por el uso de código de 16 bits diseñado para el sistema operativo Windows 3,1 o la instalación de controladores que no se proporcionan en los formularios nativos de 32 bits y de 64 bits.

Para obtener más información sobre la tecnología de 64 bits, consulte [programación de 64 bits para desarrolladores de juegos](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers).

</dd> <dt>

<span id="Should_game_developers_still_be_publishing_games_for_Windows_95__Windows_98_or_Windows_ME_"></span><span id="should_game_developers_still_be_publishing_games_for_windows_95__windows_98_or_windows_me_"></span><span id="SHOULD_GAME_DEVELOPERS_STILL_BE_PUBLISHING_GAMES_FOR_WINDOWS_95__WINDOWS_98_OR_WINDOWS_ME_"></span>**¿Los desarrolladores de juegos deben seguir publicando juegos para Windows 95, Windows 98 o Windows ME?**
</dt> <dd>

Ya no es por dos motivos: rendimiento y conjunto de características.

Si la velocidad de CPU mínima necesaria para el juego es de 1,2 GHz o superior (que es más común para los títulos de alto rendimiento), la gran mayoría de los equipos que cumplan los requisitos ejecutarán Windows XP. En el momento en que se venden los equipos con velocidades de CPU por encima de 1,2 GHz, Windows XP se instaló como el sistema operativo predeterminado por parte de casi todos los fabricantes. Esto significa que hay muchas características que se encuentran en Windows XP que los desarrolladores de juegos de hoy en día deben aprovechar:

-   Multitarea mejorado, lo que da como resultado una experiencia mejor y más fluida para vídeo, audio y juegos.
-   Modelo de controlador de vídeo más estable, que permite una depuración más sencilla, una reproducción más fluida y un mejor rendimiento.
-   Configuración más sencilla para redes: permite el acceso más sencillo a los juegos de varios jugadores.
-   Compatibilidad con transferencias DMA de forma predeterminada desde unidades de disco duro, lo que da como resultado aplicaciones más suaves y de carga más rápidas.
-   Informe de errores de Windows, que da como resultado un sistema operativo, controladores y aplicaciones más estables.
-   Compatibilidad con Unicode, que simplifica considerablemente los problemas de localización.
-   Mayor seguridad y estabilidad, lo que da lugar a mejores experiencias del consumidor.
-   Mejor compatibilidad con el hardware moderno (la mayoría de los cuales ya no usa controladores de Windows 98).
-   Administración de memoria mejorada, lo que da como resultado una mayor estabilidad y seguridad.
-   Sistema de archivos NTFS mejorado, que es más resistente a los errores y tiene un mejor rendimiento con las características de seguridad.

</dd> <dt>

<span id="Should_game_developers_still_be_publishing_games_for_Windows_2000_"></span><span id="should_game_developers_still_be_publishing_games_for_windows_2000_"></span><span id="SHOULD_GAME_DEVELOPERS_STILL_BE_PUBLISHING_GAMES_FOR_WINDOWS_2000_"></span>**¿Los desarrolladores de juegos deben seguir publicando juegos para Windows 2000?**
</dt> <dd>

Ya no es así. Además de los motivos que se indican en **¿los desarrolladores de juegos deben seguir publicando juegos para windows 95, windows 98 o Windows me?**, Windows 2000 no tiene estas características:

-   Windows XP admite características avanzadas del procesador como Hyper-Threading, varios núcleos y x64.
-   Windows XP admite componentes en paralelo, lo que reduce significativamente los conflictos de control de versiones de la aplicación.
-   Windows XP admite la protección de memoria sin ejecución, lo que ayuda a evitar programas malintencionados y puede ayudar a la depuración.
-   Windows XP ha mejorado la compatibilidad con tarjetas de vídeo basadas en AGP y PCI Express avanzadas.
-   Windows XP admite el cambio rápido de usuario, el escritorio remoto y la asistencia remota, lo que puede ayudar a reducir los costes de soporte técnico.
-   Las herramientas de rendimiento como PIX (en el SDK para desarrolladores de DirectX) ya no admiten Windows 2000.

En Resumen, Windows 2000 nunca se diseñó o se comercializa como sistema operativo del consumidor.

</dd> <dt>

<span id="What_are_the_differences_between_the_various_editions_of_Windows_Vista__How_do_they_impact_my_DirectX_application_"></span><span id="what_are_the_differences_between_the_various_editions_of_windows_vista__how_do_they_impact_my_directx_application_"></span><span id="WHAT_ARE_THE_DIFFERENCES_BETWEEN_THE_VARIOUS_EDITIONS_OF_WINDOWS_VISTA__HOW_DO_THEY_IMPACT_MY_DIRECTX_APPLICATION_"></span>**¿Cuáles son las diferencias entre las distintas ediciones de Windows Vista? ¿Cómo afectan a la aplicación de DirectX?**
</dt> <dd>

La familia de Windows Vista incluye cinco ediciones:

-   Windows Vista Home Basic
-   Windows Vista Home Premium
-   Windows Vista Business
-   Windows Vista Enterprise
-   Windows Vista Ultimate

Home Basic y Home Premium son versiones centradas en el consumidor, con características como la seguridad de la familia (anteriormente conocida como control parental) y Home Premium incluye Media Center. Business y Enterprise son ediciones orientadas a la empresa, con características como la Unión a un dominio y el Escritorio remoto/Terminal Services. La edición Ultimate combina todas las características de las ediciones de consumidor y corporativas en una versión. Todas las ediciones se incluyen en las ediciones de 32 bits (x86) y 64 bits (x64), y los usuarios pueden usar el mismo identificador de producto para ambas plataformas.

La tecnología subyacente a las distintas ediciones es idéntica y todas tienen la misma versión del tiempo de ejecución de DirectX y otros componentes. Sin embargo, las ediciones tienen algunas diferencias menores con respecto a los juegos:

-   El explorador de juegos existe en todas las ediciones, pero el acceso directo de juegos en el menú Inicio solo está en Home Basic, Home Premium y Ultimate. El explorador de juegos se puede encontrar en todas las ediciones (haciendo clic en Inicio, seleccionando todos los programas y, a continuación, haciendo clic en juegos), y la interfaz IGameExplorer funciona en todas las ediciones.
-   Los juegos que se incluyen con Windows no están disponibles de forma predeterminada en Business y Enterprise, pero pueden ser habilitados por el administrador.
-   La protección de la familia y las clasificaciones de juegos no muestran ni influyen en el comportamiento de empresa o empresa, y se deshabilitan en Ultimate cuando se une un dominio.

La configuración del control de cuentas de usuario tiene los mismos valores predeterminados en todas las ediciones, pero puede reemplazarse por directiva de grupo configuración del dominio en Business, Enterprise y Ultimate. Por ejemplo, la configuración de directiva control de cuentas de usuario: comportamiento de la petición de elevación para los usuarios estándar puede establecerse correctamente para que deniegue automáticamente las solicitudes de elevación en muchas configuraciones empresariales para mejorar la seguridad, y muchos usuarios de esos entornos siempre se ejecutarán como usuarios estándar sin la capacidad de elegir ejecutar como administrador. Cualquier programa (como un instalador) que requiera derechos administrativos, ya sea debido a la detección de la instalación heredada o a tener un manifiesto que especifique el nivel de ejecución solicitado como "requireAdministrator", siempre producirá un error al iniciarse en tales situaciones. Otras configuraciones de Directiva, como control de cuentas de usuario: elevar solo los ejecutables firmados y validados, también puede impedir que el instalador funcione si no se firma el archivo ejecutable con Authenticode.

Estos tipos de cambios de Directiva se pueden aplicar a cualquier edición de Windows Vista, pero es más probable que se encuentren en equipos Unidos a un dominio.

</dd> <dt>

<span id="What_are_the_differences_between_the_various_editions_of_Windows_7__How_do_they_impact_my_DirectX_application__"></span><span id="what_are_the_differences_between_the_various_editions_of_windows_7__how_do_they_impact_my_directx_application__"></span><span id="WHAT_ARE_THE_DIFFERENCES_BETWEEN_THE_VARIOUS_EDITIONS_OF_WINDOWS_7__HOW_DO_THEY_IMPACT_MY_DIRECTX_APPLICATION__"></span>**¿Cuáles son las diferencias entre las distintas ediciones de Windows 7? ¿Cómo afectan a la aplicación de DirectX?** 
</dt> <dd>

La mayoría de los usuarios de Windows 7 probablemente tendrán una de estas dos ediciones: Windows 7 Home Premium, para usuarios particulares o Windows 7 Professional, para usuarios empresariales y desarrolladores. En el caso de grandes corporaciones, hay una edición Enterprise de Windows 7 Enterprise con licencias por volumen, que incluye todas las características de Windows 7. Windows 7 Ultimate es el equivalente comercial de esa edición.

Windows 7 Starter Edition está disponible en todo el mundo para los OEM y se espera que se implemente principalmente con equipos con netbooks, Ultra-Low-Power Notebook. Windows 7 Home Basic solo está disponible en los mercados emergentes.

Tenga en cuenta que todas las ediciones de Windows 7 (excepto Starter Edition) están disponibles para las versiones 32 bits (x86) y 64 bits (x64), y todos los paquetes comerciales de Windows 7 incluyen medios para ambas versiones. Como con Windows Vista, los usuarios pueden usar el mismo identificador de producto comercial en cualquier plataforma.

La tecnología subyacente en las distintas ediciones es idéntica y todas las ediciones tienen la misma versión que el tiempo de ejecución de DirectX y otros componentes. Tienen algunas diferencias con respecto a las características de juegos:

-   El explorador de juegos existe en todas las ediciones, pero el acceso directo de juegos del menú Inicio está oculto de forma predeterminada en Windows 7 Professional y Enterprise. El explorador de juegos se puede encontrar en el menú Inicio (si hace clic en todos los programas y, a continuación, hace doble clic en juegos) y el usuario puede habilitar el acceso directo a juegos directos.
-   Los juegos que se incluyen con Windows no están disponibles de forma predeterminada en Windows 7 Professional y Enterprise, pero pueden ser habilitados por el administrador.
-   La seguridad familiar y las clasificaciones de juegos están disponibles en todas las ediciones, pero están deshabilitadas en Windows 7 Professional, Enterprise y Ultimate cuando el sistema operativo se une a un dominio. Al igual que con Windows Vista Ultimate, esta característica se puede volver a habilitar en el equipo que se ha unido a un dominio.

La configuración de control de cuentas de usuario (UAC) puede verse afectada por directiva de grupo configuración en las ediciones Professional, Enterprise y Ultimate de Windows 7, de forma similar a Windows Vista. Para obtener más información, consulte **¿Cuáles son las diferencias entre las distintas ediciones de Windows Vista? ¿Cómo afectan a la aplicación de DirectX?**

</dd> <dt>

<span id="Will_DirectX_10_be_available_for_Windows_XP__"></span><span id="will_directx_10_be_available_for_windows_xp__"></span><span id="WILL_DIRECTX_10_BE_AVAILABLE_FOR_WINDOWS_XP__"></span>**¿DirectX 10 estará disponible para Windows XP?** 
</dt> <dd>

No. Windows Vista, que tiene DirectX 10, incluye un tiempo de ejecución de DirectX actualizado basado en el tiempo de ejecución en Windows XP SP2 (DirectX 9.0 c) con cambios para trabajar con el nuevo modelo de controladores de pantalla (WDDM) de Windows y la nueva pila de controladores de audio y con otras actualizaciones en el sistema operativo. Además de Direct3D 9, Windows Vista admite dos nuevas interfaces cuando el hardware y los controladores de vídeo correctos están presentes: Direct3D9Ex y Direct3D10.

Puesto que estas nuevas interfaces se basan en la tecnología WDDM, nunca estarán disponibles en versiones anteriores de Windows. Todos los demás cambios realizados en las tecnologías de DirectX para Windows Vista también son específicos de la nueva versión de Windows. El nombre DirectX 10 es engañoso debido a que muchas tecnologías que se distribuyen en el SDK de DirectX (XACT, XINPUT, D3DX) no están englobadas por este número de versión. Por lo tanto, hacer referencia al número de versión del tiempo de ejecución de DirectX como un conjunto ha perdido gran parte de su significado, incluso para 9.0 c. La herramienta de diagnóstico de DirectX (DXdiag.exe) en Windows Vista informa de DirectX 10, pero esto solo hace referencia a Direct3D 10.

</dd> <dt>

<span id="Will_DirectX_11_be_available_for_Windows_Vista_or_Windows_XP__"></span><span id="will_directx_11_be_available_for_windows_vista_or_windows_xp__"></span><span id="WILL_DIRECTX_11_BE_AVAILABLE_FOR_WINDOWS_VISTA_OR_WINDOWS_XP__"></span>**¿Estará DirectX 11 disponible para Windows Vista o Windows XP?** 
</dt> <dd>

DirectX 11 está integrado en Windows 7 y está disponible como actualización para Windows Vista (consulte <https://go.microsoft.com/fwlink/p/?linkid=160189> ). Esto incluye la API de Direct3D 11, la infraestructura de gráficos de DirectX (DXGI) 1,1, los niveles de características de 10Level9, la plataforma de rasterización avanzada de Windows (WARP) 10 dispositivo de representación de software, Direct2D, DirectWrite y una actualización a la API de Direct3D 10,1 para admitir 10Level9 y WARP 10.

Por las mismas razones indicadas en la pregunta anterior (**¿DirectX 10 estará disponible para Windows XP?** ), Direct3D 11 y las API relacionadas no están disponibles en Windows XP.

</dd> <dt>

<span id="What_Happened_to_DirectShow__I_can_t_find_it_in_the_DirectX_SDK._"></span><span id="what_happened_to_directshow__i_can_t_find_it_in_the_directx_sdk._"></span><span id="WHAT_HAPPENED_TO_DIRECTSHOW__I_CAN_T_FIND_IT_IN_THE_DIRECTX_SDK._"></span>**¿Qué ha ocurrido con DirectShow? No se encuentra en el SDK de DirectX.** 
</dt> <dd>

DirectShow se quitó del SDK de DirectX a partir del 2005 de abril. Puede obtener los encabezados, bibliotecas, herramientas y ejemplos de DirectShow en el kit de desarrollo de software de Windows (anteriormente conocido como Platform SDK). DirectSetup en el SDK de DirectX sigue siendo compatible con la redistribución de los componentes del sistema de DirectShow y los componentes más recientes ya están instalados en los siguientes sistemas operativos: Microsoft Windows XP Service Pack 2, Windows XP Professional x64 Edition, Windows Server 2003 Service Pack 1 y Windows Vista.

</dd> <dt>

<span id="What_changes_were_made_to_the_DirectX_runtime_for_Windows_Vista__"></span><span id="what_changes_were_made_to_the_directx_runtime_for_windows_vista__"></span><span id="WHAT_CHANGES_WERE_MADE_TO_THE_DIRECTX_RUNTIME_FOR_WINDOWS_VISTA__"></span>**¿Qué cambios se realizaron en el tiempo de ejecución de DirectX para Windows Vista?** 
</dt> <dd>

Se realizaron los cambios principales para admitir el nuevo WDDM. Para obtener más información sobre el nuevo modelo de controlador, sobre los impactos en Direct3D 9 y en las dos nuevas interfaces de gráficos, Direct3D 9Ex y Direct3D 10, revise las [API de gráficos en Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista). Las nuevas API de gráficos para Windows 7 (Direct3D 11, Direct2D, DirectWrite, DXGI 1,1 y un Direct3D 10.1 actualizado) están disponibles como actualización para Windows Vista (vea <https://go.microsoft.com/fwlink/p/?linkid=160189> ).

Windows Vista Service Pack 1 incluye una versión actualizada del tiempo de ejecución de DirectX. Esta actualización amplía la compatibilidad de Windows Vista para incluir Direct3D 10,1, lo que expone nuevas características de hardware opcionales. (Todo el hardware que es capaz de admitir Direct3D 10,1 también es totalmente compatible con todas las características de Direct3D 10).

DirectSound se actualizó para exponer las capacidades de la nueva pila de controladores de audio de Windows Vista, que admite búferes de software de varios canales. La API de modo retenido de Direct3D se quitó completamente de Windows Vista. También se quitó DirectPlay Voice, así como la aplicación auxiliar NAT de DirectPlay y la interfaz de usuario del asignador de acciones de DirectInput. La compatibilidad con las interfaces DirectX 7 y DirectX 8 para Visual Basic 6,0 no está disponible en Windows Vista.

</dd> <dt>

<span id="What_changes_were_made_to_the_DirectX_runtime_for_Windows_7__"></span><span id="what_changes_were_made_to_the_directx_runtime_for_windows_7__"></span><span id="WHAT_CHANGES_WERE_MADE_TO_THE_DIRECTX_RUNTIME_FOR_WINDOWS_7__"></span>**¿Qué cambios se realizaron en el tiempo de ejecución de DirectX para Windows 7?** 
</dt> <dd>

Windows 7 incluye todos los componentes de tiempo de ejecución de DirectX que se encuentran en Windows Vista y agrega los niveles de características Direct3D 11, DXGI 1,1, 10Level9, el dispositivo de software WARP10, Direct2D, DirectWrite y una actualización a Direct3D 10,1 para admitir 10Level9 y WARP10. Para obtener más información, consulte [API de gráficos en Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista).

Todos los demás componentes son idénticos a Windows Vista, con la adición de compatibilidad nativa de 64 bits (x64) para la API principal de DirectMusic relacionada con el MIDI con marca de tiempo. El nivel de rendimiento de DirectMusic sigue en desuso y solo está disponible para aplicaciones de 32 bits en Windows 7 para la compatibilidad de aplicaciones. Tenga en cuenta que la compatibilidad nativa de 64 bits de DirectMusic no está disponible en Windows Vista.

</dd> <dt>

<span id="I_think_I_have_found_a_driver_bug__what_do_I_do__"></span><span id="i_think_i_have_found_a_driver_bug__what_do_i_do__"></span><span id="I_THINK_I_HAVE_FOUND_A_DRIVER_BUG__WHAT_DO_I_DO__"></span>**Creo que he encontrado un error de controlador, ¿qué hago?** 
</dt> <dd>

En primer lugar, asegúrese de que ha comprobado los resultados con el rasterizador de referencia. A continuación, compruebe los resultados con la versión más reciente con certificación de WHQL del controlador IHV. Puede comprobar mediante programación el estado de WHQL mediante el método GetAdapterIdentifier () en la interfaz IDirect3D9 que pasa la \_ marca D3DENUM WHQL \_ Level.

</dd> <dt>

<span id="Why_do_I_get_so_many_error_messages_when_I_try_to_compile_the_samples__"></span><span id="why_do_i_get_so_many_error_messages_when_i_try_to_compile_the_samples__"></span><span id="WHY_DO_I_GET_SO_MANY_ERROR_MESSAGES_WHEN_I_TRY_TO_COMPILE_THE_SAMPLES__"></span>**¿Por qué obtengo muchos mensajes de error al intentar compilar los ejemplos?** 
</dt> <dd>

Probablemente no tenga la ruta de acceso de inclusión establecida correctamente. Muchos compiladores, incluido Microsoft Visual C++, incluyen una versión anterior del SDK, por lo que si la ruta de acceso de inclusión busca primero en los directorios de inclusión del compilador estándar, obtendrá versiones incorrectas de los archivos de encabezado. Para solucionar este problema, asegúrese de que las rutas de acceso de inclusión y de biblioteca están configuradas para buscar primero en las rutas de acceso de inclusión y biblioteca de Microsoft DirectX. Vea también el archivo dxreadme.txt en el SDK. Si instala el SDK de DirectX y usa Visual C++, el instalador puede configurar opcionalmente las rutas de acceso de inclusión.

</dd> <dt>

<span id="I_get_linker_errors_about_multiple_or_missing_symbols_for_globally_unique_identifiers__GUIDs___what_do_I_do__"></span><span id="i_get_linker_errors_about_multiple_or_missing_symbols_for_globally_unique_identifiers__guids___what_do_i_do__"></span><span id="I_GET_LINKER_ERRORS_ABOUT_MULTIPLE_OR_MISSING_SYMBOLS_FOR_GLOBALLY_UNIQUE_IDENTIFIERS__GUIDS___WHAT_DO_I_DO__"></span>**Obtengo errores del vinculador sobre varios o símbolos que faltan para los identificadores únicos globales (GUID), ¿qué hago?** 
</dt> <dd>

Los distintos GUID que use deben definirse una vez y solo una vez. La definición del GUID se insertará si se \# define el símbolo INITGUID antes de incluir los archivos de encabezado de DirectX. Por lo tanto, debe asegurarse de que esto solo se produce para una unidad de compilación. Una alternativa a este método es vincular con la biblioteca dxguid. lib, que contiene las definiciones de todos los GUID de DirectX. Si usa este método (que se recomienda), nunca debe \# definir el símbolo INITGUID.

</dd> <dt>

<span id="Can_I_cast_a_pointer_to_a_DirectX_interface_to_a_lower_version_number__"></span><span id="can_i_cast_a_pointer_to_a_directx_interface_to_a_lower_version_number__"></span><span id="CAN_I_CAST_A_POINTER_TO_A_DIRECTX_INTERFACE_TO_A_LOWER_VERSION_NUMBER__"></span>**¿Se puede convertir un puntero a una interfaz de DirectX a un número de versión inferior?** 
</dt> <dd>

No. Las interfaces de DirectX son interfaces COM. Esto significa que no hay ningún requisito para que las interfaces con números más altos se deriven de las correspondientes números inferiores. Por lo tanto, la única manera segura de obtener una interfaz diferente para un objeto de DirectX es usar el método QueryInterface de la interfaz. Este método forma parte de la interfaz IUnknown estándar, de la que deben derivarse todas las interfaces COM.

</dd> <dt>

<span id="Can_I_mix_the_use_of_DirectX_9_components_and_DirectX_8_or_earlier_components_within_the_same_application__"></span><span id="can_i_mix_the_use_of_directx_9_components_and_directx_8_or_earlier_components_within_the_same_application__"></span><span id="CAN_I_MIX_THE_USE_OF_DIRECTX_9_COMPONENTS_AND_DIRECTX_8_OR_EARLIER_COMPONENTS_WITHIN_THE_SAME_APPLICATION__"></span>**¿Puedo combinar el uso de componentes de DirectX 9 y DirectX 8 o componentes anteriores en la misma aplicación?** 
</dt> <dd>

Puede mezclar libremente diferentes componentes de una versión diferente. por ejemplo, puede usar DirectInput 8 con Direct3D 9 en la misma aplicación. Sin embargo, por lo general no se pueden mezclar versiones diferentes del mismo componente dentro de la misma aplicación; por ejemplo, no puede mezclar DirectDraw 7 con Direct3D 9 (dado que se trata realmente del mismo componente que DirectDraw se ha incorporado a Direct3D a partir de DirectX 8). Sin embargo, hay excepciones, como el uso de Direct3D 9 y Direct3D 10 en la misma aplicación, que se permite.

</dd> <dt>

<span id="Can_I_mix_the_use_of_Direct3D_9_and_Direct3D_10_within_the_same_application__"></span><span id="can_i_mix_the_use_of_direct3d_9_and_direct3d_10_within_the_same_application__"></span><span id="CAN_I_MIX_THE_USE_OF_DIRECT3D_9_AND_DIRECT3D_10_WITHIN_THE_SAME_APPLICATION__"></span>**¿Puedo combinar el uso de Direct3D 9 y Direct3D 10 dentro de la misma aplicación?** 
</dt> <dd>

Sí, puede usar estas versiones de Direct3D juntas en la misma aplicación.

</dd> <dt>

<span id="What_do_the_return_values_from_the_Release_or_AddRef_methods_mean__"></span><span id="what_do_the_return_values_from_the_release_or_addref_methods_mean__"></span><span id="WHAT_DO_THE_RETURN_VALUES_FROM_THE_RELEASE_OR_ADDREF_METHODS_MEAN__"></span>**¿Qué significan los valores devueltos de los métodos Release o AddRef?** 
</dt> <dd>

El valor devuelto será el recuento de referencias actual del objeto. Sin embargo, la especificación COM indica que no debe confiar en esto y que el valor generalmente solo está disponible para fines de depuración. Los valores que observa pueden ser inesperados, ya que otros objetos del sistema pueden contener referencias a los objetos de DirectX que cree. Por esta razón, no debe escribir código que llame repetidamente a Release hasta que el recuento de referencias sea cero, ya que el objeto se puede liberar incluso aunque otro componente aún pueda hacer referencia a él.

</dd> <dt>

<span id="Does_it_matter_in_which_order_I_release_DirectX_interfaces__"></span><span id="does_it_matter_in_which_order_i_release_directx_interfaces__"></span><span id="DOES_IT_MATTER_IN_WHICH_ORDER_I_RELEASE_DIRECTX_INTERFACES__"></span>**¿Es importante el orden en que se publican las interfaces de DirectX?** 
</dt> <dd>

No importa porque se cuentan las interfaces COM. Sin embargo, hay algunos errores conocidos con el orden de lanzamiento de las interfaces en algunas versiones de DirectX. Por motivos de seguridad, se recomienda liberar las interfaces en orden de creación inversa siempre que sea posible.

</dd> <dt>

<span id="What_is_a_smart_pointer_and_should_I_use_it__"></span><span id="what_is_a_smart_pointer_and_should_i_use_it__"></span><span id="WHAT_IS_A_SMART_POINTER_AND_SHOULD_I_USE_IT__"></span>**¿Qué es un puntero inteligente y debo usarlo?** 
</dt> <dd>

Un puntero inteligente es una clase de plantilla de C++ diseñada para encapsular la funcionalidad de puntero. En concreto, hay clases de puntero inteligente estándar diseñadas para encapsular punteros de interfaz COM. Estos punteros realizan automáticamente QueryInterface en lugar de una conversión y controlan AddRef y Release. El uso de ellos es en gran medida una cuestión de sabor. Si el código contiene una gran cantidad de copias de punteros de interfaz, con varios AddRefs y versiones, los punteros inteligentes pueden hacer que el código sea más fácil y menos propenso a errores. De lo contrario, puede hacerlo sin ellos. Visual C++ incluye un puntero inteligente COM estándar de Microsoft, definido en el archivo de encabezado "comdef. h" (buscar com \_ ptr \_ t en la ayuda).

</dd> <dt>

<span id="I_have_trouble_debugging_my_DirectX_application__any_tips__"></span><span id="i_have_trouble_debugging_my_directx_application__any_tips__"></span><span id="I_HAVE_TROUBLE_DEBUGGING_MY_DIRECTX_APPLICATION__ANY_TIPS__"></span>**Tengo problemas para depurar la aplicación DirectX, ¿tiene alguna sugerencia?** 
</dt> <dd>

El problema más común con la depuración de aplicaciones DirectX está intentando depurar mientras se bloquea una superficie DirectDraw. Esta situación puede provocar un "bloqueo de Win16" en los sistemas de Microsoft Windows 9x, lo que evita que se dibuje la ventana del depurador. La especificación de la \_ marca D3DLOCK NOSYSLOCK cuando se bloquea la superficie normalmente puede eliminar esto. Windows 2000 no sufre este problema. Al desarrollar una aplicación, es útil ejecutar con la versión de depuración del tiempo de ejecución de DirectX (seleccionada al instalar el SDK), que realiza algunas validaciones de parámetros y genera mensajes útiles para la salida del depurador.

</dd> <dt>

<span id="What_s_the_correct_way_to_check_return_codes__"></span><span id="what_s_the_correct_way_to_check_return_codes__"></span><span id="WHAT_S_THE_CORRECT_WAY_TO_CHECK_RETURN_CODES__"></span>**¿Cuál es la manera correcta de comprobar los códigos de retorno?** 
</dt> <dd>

Use las macros SUCCEEDED y FAILed. Los métodos de DirectX pueden devolver varios códigos de error y correctos, por lo que un simple:

``` syntax
== D3D_OK
```

o una prueba similar no siempre será suficiente.

</dd> <dt>

<span id="How_do_I_disable_ALT_TAB_and_other_task_switching__"></span><span id="how_do_i_disable_alt_tab_and_other_task_switching__"></span><span id="HOW_DO_I_DISABLE_ALT_TAB_AND_OTHER_TASK_SWITCHING__"></span>**¿Cómo deshabilitar ALT + TAB y otro cambio de tarea?** 
</dt> <dd>

¡ No! Los juegos deben ser capaces de controlar correctamente el cambio de tareas, ya que muchas cosas hacen que esto suceda: ALT + TAB, conexiones a escritorio remoto, cambio rápido de usuario, límites de uso de controles parentales y muchos otros eventos.

Al mismo tiempo, dos orígenes comunes de conmutación accidental de tareas en juegos con esquemas de control centrados en el teclado son presionar la tecla del logotipo de Windows y activar la característica de accesibilidad StickyKeys con la tecla Mayús. Para solucionar estos casos deshabilitando la funcionalidad, vea las técnicas descritas en [deshabilitar teclas de método abreviado en juegos](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games).

</dd> <dt>

<span id="Is_there_a_recommended_book_explaining_COM__"></span><span id="is_there_a_recommended_book_explaining_com__"></span><span id="IS_THERE_A_RECOMMENDED_BOOK_EXPLAINING_COM__"></span>**¿Hay un libro recomendado que explique COM?** 
</dt> <dd>

*Dentro de com* , Dale Rogerson, publicado por Microsoft Press, es una excelente introducción a com. Para obtener una visión más detallada de COM, también se recomienda encarecidamente el libro *Essential com* de Don Box, publicado por el de gran tamaño.

</dd> <dt>

<span id="What_is_managed_code__"></span><span id="what_is_managed_code__"></span><span id="WHAT_IS_MANAGED_CODE__"></span>**¿Qué es el código administrado?** 
</dt> <dd>

El código administrado es código cuya ejecución está administrada por el .NET Framework Common Language Runtime (CLR). Hace referencia a un contrato de cooperación entre el código que se ejecuta de forma nativa y el tiempo de ejecución. Este contrato especifica que, en cualquier punto de ejecución, el tiempo de ejecución puede detener una CPU en ejecución y recuperar información específica de la dirección de la instrucción de la CPU actual. La información que debe estar disponible en las consultas suele pertenecer al estado en tiempo de ejecución, como el contenido del registro o de la memoria de la pila.

Antes de ejecutar el código, el IL se compila en código ejecutable nativo. Y, puesto que esta compilación se produce por el entorno de ejecución administrado (o, más bien, por un compilador compatible con tiempo de ejecución que sabe cómo establecer como destino el entorno de ejecución administrado), el entorno de ejecución administrado puede realizar garantías sobre lo que el código va a hacer. Puede insertar capturas y enlaces adecuados para la recolección de elementos no utilizados, el control de excepciones, la seguridad de tipos, los límites de matriz y la comprobación de índices, etc. Por ejemplo, este tipo de compilador se asegura de diseñar marcos de pila y todo lo correcto para que el recolector de elementos no utilizados pueda ejecutarse en segundo plano en un subproceso independiente, recorriendo constantemente la pila de llamadas activa, buscando todas las raíces y cometiendo todos los objetos activos. Además, dado que el IL tiene un concepto de seguridad de tipos, el motor de ejecución mantendrá la garantía de seguridad de tipos, eliminando una clase completa de errores de programación que a menudo conducen a brechas de seguridad.

A diferencia de esto en el mundo no administrado: los archivos ejecutables no administrados son básicamente una imagen binaria, código x86, cargados en la memoria. El contador del programa se coloca ahí y es el último que conoce el sistema operativo. Existen protecciones en cuanto a la administración de memoria y la e/s del puerto, etc., pero el sistema no sabe realmente lo que está haciendo la aplicación. Por lo tanto, no puede garantizar ninguna garantía sobre lo que ocurre cuando se ejecuta la aplicación.

</dd> <dt>

<span id="What_books_are_there_about_general_Windows_programming__"></span><span id="what_books_are_there_about_general_windows_programming__"></span><span id="WHAT_BOOKS_ARE_THERE_ABOUT_GENERAL_WINDOWS_PROGRAMMING__"></span>**¿Qué libros hay en la programación general de Windows?** 
</dt> <dd>

Una gran cantidad. Sin embargo, las dos que se recomiendan son:

-   Programación de Windows con Charles Petzold (Microsoft Press)
-   Programación de aplicaciones para Windows por Jeffrey Richter (Microsoft Press)

</dd> <dt>

<span id="How_do_I_debug_using_the_Windows_symbol_files__"></span><span id="how_do_i_debug_using_the_windows_symbol_files__"></span><span id="HOW_DO_I_DEBUG_USING_THE_WINDOWS_SYMBOL_FILES__"></span>**Cómo depurar con los archivos de símbolos de Windows** 
</dt> <dd>

Microsoft publica símbolos eliminados para todos los archivos DLL del sistema (además de otros). Para acceder a ellos, agregue lo siguiente a la ruta de acceso de símbolos en la configuración del proyecto en Visual Studio:

``` syntax
srv*https://msdl.microsoft.com/download/symbols
```

para almacenar en caché símbolos localmente, use la sintaxis siguiente:

``` syntax
srv*c:\cache*https://msdl.microsoft.com/download/symbols
```

Donde c: \\ Cache es un directorio local para almacenar en caché los archivos de símbolos.

</dd> </dl>

## <a name="direct3d-questions"></a>Preguntas de Direct3D

### <a name="general-direct3d-questions"></a>Preguntas generales sobre Direct3D

<dl> <dt>

<span id="Where_can_I_find_information_about_3D_graphics_techniques__"></span><span id="where_can_i_find_information_about_3d_graphics_techniques__"></span><span id="WHERE_CAN_I_FIND_INFORMATION_ABOUT_3D_GRAPHICS_TECHNIQUES__"></span>**¿Dónde puedo encontrar información acerca de las técnicas de gráficos 3D?** 
</dt> <dd>

El libro estándar en el asunto es gráficos del equipo: principios y prácticas por Foley, furgoneta Dam et al. Es un recurso valioso para cualquier persona que quiera comprender las bases matemáticas de las técnicas de geometría, rasterización e iluminación. Las preguntas más frecuentes sobre el grupo de Usenet comp. Graphics. algorithm también contiene material útil.

</dd> <dt>

<span id="Does_Direct3D_emulate_functionality_not_provided_by_hardware__"></span><span id="does_direct3d_emulate_functionality_not_provided_by_hardware__"></span><span id="DOES_DIRECT3D_EMULATE_FUNCTIONALITY_NOT_PROVIDED_BY_HARDWARE__"></span>**¿Direct3D emula la funcionalidad no proporcionada por el hardware?** 
</dt> <dd>

Depende. Direct3D tiene una canalización de procesamiento de vértices de software totalmente destacada (incluida la compatibilidad con los sombreadores de vértices personalizados). Sin embargo, no se proporciona ninguna emulación para las operaciones de nivel de píxel; las aplicaciones deben comprobar los bits de Cap adecuados y usar la API de ValidateDevice para determinar la compatibilidad.

</dd> <dt>

<span id="Is_there_a_software_rasterizer_included_with_Direct3D__"></span><span id="is_there_a_software_rasterizer_included_with_direct3d__"></span><span id="IS_THERE_A_SOFTWARE_RASTERIZER_INCLUDED_WITH_DIRECT3D__"></span>**¿Hay un rasterizador de software incluido en Direct3D?** 
</dt> <dd>

No para las aplicaciones de rendimiento. Se proporciona un rasterizador de referencia para la validación del controlador, pero la implementación está diseñada para proporcionar precisión y no rendimiento. Direct3D admite rasterizadores de software de complementos.

</dd> <dt>

<span id="How_can_I_perform_color_keying_with_DirectX_graphics__"></span><span id="how_can_i_perform_color_keying_with_directx_graphics__"></span><span id="HOW_CAN_I_PERFORM_COLOR_KEYING_WITH_DIRECTX_GRAPHICS__"></span>**¿Cómo se puede realizar la creación de claves de color con gráficos de DirectX?** 
</dt> <dd>

La incrustación de colores no se admite directamente; en su lugar, tendrá que usar la combinación alfa para emular la incrustación de color. La función D3DXCreateTextureFromFileEx () se puede usar para facilitar esto. Esta función acepta un parámetro de color de clave y reemplazará todos los píxeles de la imagen de origen que contengan el color especificado por píxeles negros transparentes en la textura creada.

</dd> <dt>

<span id="Does_the_Direct3D_geometry_code_utilize_3DNow__and_or_Pentium_III_SIMD_instructions__"></span><span id="does_the_direct3d_geometry_code_utilize_3dnow__and_or_pentium_iii_simd_instructions__"></span><span id="DOES_THE_DIRECT3D_GEOMETRY_CODE_UTILIZE_3DNOW__AND_OR_PENTIUM_III_SIMD_INSTRUCTIONS__"></span>**¿El código de geometría de Direct3D usan las instrucciones 3DNow! y/o Pentium III SIMD?** 
</dt> <dd>

Sí. La canalización de geometría de Direct3D tiene varias rutas de acceso de código diferentes, dependiendo del tipo de procesador, y utilizará las operaciones especiales de punto flotante que proporciona el 3DNow! o las instrucciones SIMD de Pentium III donde están disponibles. Esto incluye el procesamiento de sombreadores de vértices personalizados.

</dd> <dt>

<span id="How_do_I_prevent_transparent_pixels_being_written_to_the_z-buffer__"></span><span id="how_do_i_prevent_transparent_pixels_being_written_to_the_z-buffer__"></span><span id="HOW_DO_I_PREVENT_TRANSPARENT_PIXELS_BEING_WRITTEN_TO_THE_Z-BUFFER__"></span>**Cómo evitar que se escriban píxeles transparentes en el búfer z** 
</dt> <dd>

Puede filtrar los píxeles con un valor alfa por encima o por debajo de un umbral determinado. Puede controlar este comportamiento mediante renderstates ALPHATESTENABLE, ALPHAREF y ALPHAFUNC.

</dd> <dt>

<span id="What_is_a_stencil_buffer__"></span><span id="what_is_a_stencil_buffer__"></span><span id="WHAT_IS_A_STENCIL_BUFFER__"></span>**¿Qué es un búfer de estarcido?** 
</dt> <dd>

Un búfer de estarcido es un búfer adicional de información por píxel, de forma muy similar a un búfer z. De hecho, reside en algunos de los bits de un búfer z. Los formatos de búfer de la galería de símbolos z o z son de 15 bits y de 1 bit, o de una galería de símbolos de 24 bits y de 8 bits. Es posible realizar operaciones aritméticas simples en el contenido del búfer de estarcido por píxel a medida que se representan polígonos. Por ejemplo, el búfer de estarcido se puede aumentar o reducir, o bien se puede rechazar el píxel si el valor de la galería de símbolos produce un error en una prueba de comparación simple. Esto resulta útil para los efectos que implican marcar una región del búfer de fotogramas y, a continuación, realizar la representación solo de la región marcada (o sin marcar). Los buenos ejemplos son efectos volumétricos como los volúmenes de instantáneas.

</dd> <dt>

<span id="How_do_I_use_a_stencil_buffer_to_render_shadow_volumes__"></span><span id="how_do_i_use_a_stencil_buffer_to_render_shadow_volumes__"></span><span id="HOW_DO_I_USE_A_STENCIL_BUFFER_TO_RENDER_SHADOW_VOLUMES__"></span>**Cómo usar un búfer de estarcido para representar volúmenes de instantáneas** 
</dt> <dd>

La clave para este y otros efectos de búfer de estarcido volumétricos es la interacción entre el búfer de estarcido y el búfer z. Una escena con un volumen de sombra se representa en tres fases. En primer lugar, la escena sin la sombra se representa como de costumbre, mediante el uso del búfer z. A continuación, la sombra se marca en el búfer de la galería de símbolos como se indica a continuación. Las caras frontales del volumen de la sombra se dibujan mediante polígonos invisibles, con las pruebas de z habilitadas pero las escrituras en z están deshabilitadas y el búfer de estarcido se incrementa en cada píxel pasando la prueba z. Los lados traseros del volumen de instantánea se representan de forma similar, pero disminuyen el valor de la galería de símbolos en su lugar.

Ahora, considere un solo píxel. Suponiendo que la cámara no está en el volumen de instantáneas, hay cuatro posibilidades para el punto correspondiente de la escena. Si el rayo de la cámara al punto no forma una intersección con el volumen de la instantánea, no se dibujará ningún polígono de sombra y el búfer de estarcido seguirá siendo cero. De lo contrario, si el punto se encuentra delante del volumen de la instantánea, los polígonos de la sombra se almacenarán en búfer z y la galería de símbolos permanecerá sin cambios. Si los puntos se encuentran detrás del volumen de la instantánea, se representará el mismo número de caras frontales que las caras, y la galería de símbolos será cero, que se habrá incrementado tantas veces como se haya disminuido.

La posibilidad final es que el punto se encuentra dentro del volumen de la instantánea. En este caso, la cara posterior del volumen de la instantánea se almacenará en búfer de z, pero no la cara frontal, por lo que el búfer de estarcido será un valor distinto de cero. El resultado son partes del búfer de fotogramas que están en la sombra con un valor de galería de símbolos distinto de cero. Por último, para representar la sombra realmente, toda la escena se lava con un polígono mezclado alfa establecido para que solo afecte a los píxeles con un valor de galería de símbolos distinto de cero. Un ejemplo de esta técnica se puede observar en el ejemplo "Volume Shadow" que se incluye con el SDK de DirectX.

</dd> <dt>

<span id="What_are_the_texel_alignment_rules__How_do_I_get_a_one-to-one_mapping__"></span><span id="what_are_the_texel_alignment_rules__how_do_i_get_a_one-to-one_mapping__"></span><span id="WHAT_ARE_THE_TEXEL_ALIGNMENT_RULES__HOW_DO_I_GET_A_ONE-TO-ONE_MAPPING__"></span>**¿Cuáles son las reglas de alineación de textura? ¿Cómo obtener una asignación uno a uno?** 
</dt> <dd>

Esto se explica completamente en la documentación de Direct3D 9. Sin embargo, el Resumen Ejecutivo es que debe desviar las coordenadas de pantalla por 0,5 de un píxel para que se alinee correctamente con textura. La mayoría de las tarjetas se ajustan ahora correctamente a las reglas de alineación de textura; sin embargo, hay algunas tarjetas o controladores más antiguos que no lo hacen. Para controlar estos casos, el mejor Consejo es ponerse en contacto con el proveedor de hardware en cuestión y solicitar controladores actualizados o su solución sugerida. Tenga en cuenta que en Direct3D 10, esta regla ya no se incluye.

</dd> <dt>

<span id="What_is_the_purpose_of_the_D3DCREATE_PUREDEVICE_flag__"></span><span id="what_is_the_purpose_of_the_d3dcreate_puredevice_flag__"></span><span id="WHAT_IS_THE_PURPOSE_OF_THE_D3DCREATE_PUREDEVICE_FLAG__"></span>**¿Cuál es el propósito de la \_ marca D3DCREATE PUREDEVICE?** 
</dt> <dd>

Use la \_ marca D3DCREATE PUREDEVICE durante la creación del dispositivo para crear un dispositivo puro. Un dispositivo puro no guarda el estado actual (durante los cambios de estado), lo que a menudo mejora el rendimiento. Este dispositivo también requiere procesamiento de vértices de hardware. Un dispositivo puro se utiliza normalmente cuando se completa el desarrollo y la depuración, y se desea lograr el mejor rendimiento.

Un inconveniente de un dispositivo puro es que no admite todas las \* llamadas Get API; esto significa que no se puede usar un dispositivo puro para consultar el estado de la canalización. Esto hace que sea más difícil depurar mientras se ejecuta una aplicación. A continuación se muestra una lista de todos los métodos deshabilitados por un dispositivo puro.

-   [**IDirect3DDevice9::GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane)
-   [**IDirect3DDevice9::GetClipStatus**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipstatus)
-   [**IDirect3DDevice9::GetLight**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlight)
-   [**IDirect3DDevice9::GetLightEnable**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlightenable)
-   [**IDirect3DDevice9::GetMaterial**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getmaterial)
-   [**IDirect3DDevice9::GetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstantf)
-   [**IDirect3DDevice9::GetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstanti)
-   [**IDirect3DDevice9::GetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstantb)
-   [**IDirect3DDevice9::GetRenderState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getrenderstate)
-   [**IDirect3DDevice9::GetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getsamplerstate)
-   [**IDirect3DDevice9::GetTextureStageState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettexturestagestate)
-   [**IDirect3DDevice9::GetTransform**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettransform)
-   [**IDirect3DDevice9::GetVertexShaderConstantF**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstantf)
-   [**IDirect3DDevice9::GetVertexShaderConstantI**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstanti)
-   [**IDirect3DDevice9::GetVertexShaderConstantB**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstantb)

Un segundo inconveniente de un dispositivo puro es que no filtre ningún cambio de estado redundante. Cuando se usa un dispositivo puro, la aplicación debe reducir el número de cambios de estado en el bucle de representación al mínimo; Esto puede incluir cambios en el estado del filtrado para asegurarse de que los Estados no se establecen más de una vez. Este equilibrio es dependiente de la aplicación. Si usa más de una llamada SET 1000 por fotograma, debería considerar la posibilidad de aprovechar el filtrado de redundancia que se realiza automáticamente mediante un dispositivo no puro.

Al igual que con todos los problemas de rendimiento, la única forma de saber si su aplicación funcionará mejor con un dispositivo puro es comparar el rendimiento de la aplicación con un dispositivo puro y no puro. Un dispositivo puro tiene la posibilidad de acelerar una aplicación reduciendo la sobrecarga de la CPU de la API. Pero tenga cuidado. En algunos escenarios, un dispositivo puro ralentizará la aplicación (debido al trabajo adicional de CPU causado por los cambios de estado redundantes). Si no está seguro de qué tipo de dispositivo funcionará mejor para su aplicación y no filtra los cambios redundantes en la aplicación, use un dispositivo no puro.

</dd> <dt>

<span id="How_do_I_enumerate_the_display_devices_in_a_multi-monitor_system__"></span><span id="how_do_i_enumerate_the_display_devices_in_a_multi-monitor_system__"></span><span id="HOW_DO_I_ENUMERATE_THE_DISPLAY_DEVICES_IN_A_MULTI-MONITOR_SYSTEM__"></span>**Cómo enumerar los dispositivos de pantalla en un sistema de varios monitores?** 
</dt> <dd>

La aplicación puede realizar la enumeración a través de una iteración simple mediante métodos de la interfaz IDirect3D9. Llame a GetAdapterCount para determinar el número de adaptadores de pantalla del sistema. Llame a GetAdapterMonitor para determinar a qué monitor físico está conectado un adaptador (este método devuelve una HMONITOR, que se puede usar en la GetMonitorInfo de la API Win32 para determinar la información sobre el monitor físico). Determinar las características de un adaptador de pantalla concreto o crear un dispositivo Direct3D en dicho adaptador es tan sencillo como pasar el número de adaptador adecuado en lugar del \_ valor predeterminado de D3DADAPTER al llamar a GetDeviceCaps, CreateDevice u otros métodos.

</dd> <dt>

<span id="What_happened_to_Fixed_Function_Bumpmapping_in_D3D9__"></span><span id="what_happened_to_fixed_function_bumpmapping_in_d3d9__"></span><span id="WHAT_HAPPENED_TO_FIXED_FUNCTION_BUMPMAPPING_IN_D3D9__"></span>**¿Qué ha ocurrido con la función Fixed BumpMapping en D3D9?** 
</dt> <dd>

A partir de Direct3D 9 hemos restringido la validación en tarjetas que solo podían admitir > 2 texturas simultáneas. Ciertas tarjetas antiguas solo tienen tres fases de textura disponibles cuando se usa una operación de alfa modular específica. El uso más común para el que los usuarios usan las 3 fases es el BumpMapping de relieve y puede seguir haciendo esto con D3D9.

El campo alto debe almacenarse en el canal alfa y se usa para modular la contribución de las luces, es decir:

``` syntax
// Stage 0 is the base texture, with the height map in the alpha channel
m_pd3dDevice->SetTexture(0, m_pEmbossTexture );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 0 );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLOROP,   D3DTOP_MODULATE );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAOP,   D3DTOP_SELECTARG1 );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE );
if( m_bShowEmbossMethod )
{
 // Stage 1 passes through the RGB channels (SELECTARG2 = CURRENT), and 
 // does a signed add with the inverted alpha channel. 
 // The texture coords associated with Stage 1 are the shifted ones, so 
 // the result is:
 //    (height - shifted_height) * tex.RGB * diffuse.RGB
   m_pd3dDevice->SetTexture( 1, m_pEmbossTexture );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_TEXCOORDINDEX, 1 );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_COLOROP, D3DTOP_SELECTARG2 );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG2, D3DTA_CURRENT );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_ALPHAOP, D3DTOP_ADDSIGNED );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_ALPHAARG1, D3DTA_TEXTURE|D3DTA_COMPLEMENT );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_ALPHAARG2, D3DTA_CURRENT );

   // Set up the alpha blender to multiply the alpha channel 
   // (monochrome emboss) with the src color (lighted texture)
   m_pd3dDevice->SetRenderState( D3DRS_ALPHABLENDENABLE, TRUE );
   m_pd3dDevice->SetRenderState( D3DRS_SRCBLEND,  D3DBLEND_SRCALPHA );
   m_pd3dDevice->SetRenderState( D3DRS_DESTBLEND, D3DBLEND_ZERO );
}
```

Este ejemplo, junto con otros ejemplos anteriores, ya no se incluye en la versión actual del SDK y no se incluirá en futuras versiones del SDK.

</dd> </dl>

### <a name="geometry-vertex-processing"></a>Procesamiento de geometría (vértice)

<dl> <dt>

<span id="Vertex_streams_confuse_me_how_do_they_work__"></span><span id="vertex_streams_confuse_me_how_do_they_work__"></span><span id="VERTEX_STREAMS_CONFUSE_ME_HOW_DO_THEY_WORK__"></span>**¿Cómo funcionan los flujos de vértices?** 
</dt> <dd>

Direct3D ensambla cada vértice que se inserta en la parte de procesamiento de la canalización desde uno o varios flujos de vértices. La existencia de un solo flujo de vértices corresponde al antiguo modelo anterior a DirectX 8, en el que los vértices proceden de un único origen. Con DirectX 8, diferentes componentes de vértice pueden provienen de diferentes orígenes; por ejemplo, un búfer de vértices podría contener posiciones y normales, mientras que otros valores de color y coordenadas de textura.

</dd> <dt>

<span id="What_is_a_vertex_shader__"></span><span id="what_is_a_vertex_shader__"></span><span id="WHAT_IS_A_VERTEX_SHADER__"></span>**¿Qué es un sombreador de vértices?** 
</dt> <dd>

Un sombreador de vértices es un procedimiento para procesar un solo vértice. Se define mediante un lenguaje sencillo de ensamblado que se ensambla mediante la biblioteca de utilidades de D3DX en una secuencia de token que Direct3D acepta. El sombreador de vértices toma como entrada un solo vértice y un conjunto de valores constantes; genera una posición de vértice (en el espacio de recorte) y, opcionalmente, un conjunto de colores y coordenadas de textura que se usan en la rasterización. Tenga en cuenta que cuando tiene un sombreador de vértices personalizado, los componentes de vértice ya no tienen ninguna semántica aplicada por Direct3D y los vértices son simplemente datos arbitrarios que interpreta el sombreador de vértices que cree.

</dd> <dt>

<span id="Does_a_vertex_shader_perform_perspective_division_or_clipping__"></span><span id="does_a_vertex_shader_perform_perspective_division_or_clipping__"></span><span id="DOES_A_VERTEX_SHADER_PERFORM_PERSPECTIVE_DIVISION_OR_CLIPPING__"></span>**¿Un sombreador de vértices realiza una división o recorte de la perspectiva?** 
</dt> <dd>

No. El sombreador de vértices genera una coordenada homogénea en el espacio de recorte para la posición del vértice transformado. La división y el recorte de la perspectiva se realizan automáticamente después del sombreador.

</dd> <dt>

<span id="Can_I_generate_geometry_with_a_vertex_shader__"></span><span id="can_i_generate_geometry_with_a_vertex_shader__"></span><span id="CAN_I_GENERATE_GEOMETRY_WITH_A_VERTEX_SHADER__"></span>**¿Puedo generar geometría con un sombreador de vértices?** 
</dt> <dd>

Un sombreador de vértices no puede crear ni destruir vértices; funciona en un solo vértice cada vez, tomando un vértice sin procesar como entrada y generando un único vértice procesado. Por lo tanto, se puede usar para manipular la geometría existente (aplicar las desformaciones o realizar operaciones de aplicación de aspectos), pero realmente no puede generar una nueva geometría por se.

</dd> <dt>

<span id="Can_I_apply_a_custom_vertex_shader_to_the_results_of_the_fixed-function_geometry_pipeline__or_vice-versa___"></span><span id="can_i_apply_a_custom_vertex_shader_to_the_results_of_the_fixed-function_geometry_pipeline__or_vice-versa___"></span><span id="CAN_I_APPLY_A_CUSTOM_VERTEX_SHADER_TO_THE_RESULTS_OF_THE_FIXED-FUNCTION_GEOMETRY_PIPELINE__OR_VICE-VERSA___"></span>**¿Se puede aplicar un sombreador de vértices personalizado a los resultados de la canalización de geometría de función fija (o viceversa)?** 
</dt> <dd>

No. Debe elegir uno u otro. Si usa un sombreador de vértices personalizado, es el responsable de realizar la transformación de vértices completa.

</dd> <dt>

<span id="Can_I_use_a_custom_vertex_shader_if_my_hardware_does_not_support_it__"></span><span id="can_i_use_a_custom_vertex_shader_if_my_hardware_does_not_support_it__"></span><span id="CAN_I_USE_A_CUSTOM_VERTEX_SHADER_IF_MY_HARDWARE_DOES_NOT_SUPPORT_IT__"></span>**¿Puedo usar un sombreador de vértices personalizado si el hardware no lo admite?** 
</dt> <dd>

Sí. El motor de procesamiento de vértices de software de Direct3D es totalmente compatible con los sombreadores de vértices personalizados con un nivel de rendimiento sorprendentemente alto.

</dd> <dt>

<span id="How_do_I_determine_if_the_hardware_supports_my_custom_vertex_shader__"></span><span id="how_do_i_determine_if_the_hardware_supports_my_custom_vertex_shader__"></span><span id="HOW_DO_I_DETERMINE_IF_THE_HARDWARE_SUPPORTS_MY_CUSTOM_VERTEX_SHADER__"></span>**Cómo determinar si el hardware es compatible con el sombreador de vértices personalizado?** 
</dt> <dd>

Los dispositivos capaces de admitir sombreadores de vértices en hardware son necesarios para rellenar el campo D3DCAPS9:: VertexShaderVersion para indicar el nivel de versión del sombreador de vértices que admiten. Cualquier dispositivo que afirme admitir un nivel determinado de sombreador de vértices debe admitir todos los sombreadores de vértices válidos que cumplan la especificación para ese nivel o a continuación.

</dd> <dt>

<span id="How_many_constant_registers_are_available_for_vertex_shaders__"></span><span id="how_many_constant_registers_are_available_for_vertex_shaders__"></span><span id="HOW_MANY_CONSTANT_REGISTERS_ARE_AVAILABLE_FOR_VERTEX_SHADERS__"></span>**¿Cuántos registros constantes están disponibles para los sombreadores de vértices?** 
</dt> <dd>

Los dispositivos compatibles con los sombreadores de vértices de vs 1,0 son necesarios para admitir un mínimo de 96 registros de constantes. Los dispositivos pueden admitir más de este número mínimo y pueden notificar esto a través del campo D3DCAPS9:: MaxVertexShaderConst.

</dd> <dt>

<span id="Can_I_share_position_data_between_vertices_with_different_texture_coordinates__"></span><span id="can_i_share_position_data_between_vertices_with_different_texture_coordinates__"></span><span id="CAN_I_SHARE_POSITION_DATA_BETWEEN_VERTICES_WITH_DIFFERENT_TEXTURE_COORDINATES__"></span>**¿Puedo compartir datos de posición entre vértices con distintas coordenadas de textura?** 
</dt> <dd>

El ejemplo habitual de esta situación es un cubo en el que desea utilizar una textura diferente para cada una de las caras. Desafortunadamente, la respuesta es no, actualmente no es posible indexar los componentes de vértice por separado. Incluso con varios flujos de vértices, todos los flujos se indexan juntos.

</dd> <dt>

<span id="When_I_submit_an_indexed_list_of_primitives__does_Direct3D_process_all_of_the_vertices_in_the_buffer__or_just_the_ones_I_indexed__"></span><span id="when_i_submit_an_indexed_list_of_primitives__does_direct3d_process_all_of_the_vertices_in_the_buffer__or_just_the_ones_i_indexed__"></span><span id="WHEN_I_SUBMIT_AN_INDEXED_LIST_OF_PRIMITIVES__DOES_DIRECT3D_PROCESS_ALL_OF_THE_VERTICES_IN_THE_BUFFER__OR_JUST_THE_ONES_I_INDEXED__"></span>**Cuando envío una lista indizada de primitivas, ¿Direct3D procesa todos los vértices del búfer o solo los que se indexan?** 
</dt> <dd>

Cuando se usa la canalización de geometría de software, Direct3D transforma primero todos los vértices del intervalo enviado, en lugar de transformarlos "a petición" a medida que se indexan. En el caso de datos comprimidos de forma densa (es decir, donde se usan la mayoría de los vértices), es más eficaz, especialmente cuando hay instrucciones SIMD disponibles. Si los datos se empaquetan de forma dispersa (es decir, no se usan muchos vértices), puede que desee considerar la posibilidad de reorganizar los datos para evitar demasiadas transformaciones redundantes. Cuando se usa la aceleración de geometría de hardware, los vértices se transforman normalmente a petición a medida que son necesarios.

</dd> <dt>

<span id="What_is_an_index_buffer__"></span><span id="what_is_an_index_buffer__"></span><span id="WHAT_IS_AN_INDEX_BUFFER__"></span>**¿Qué es un búfer de índice?** 
</dt> <dd>

Un búfer de índice es exactamente análogo a un búfer de vértices, pero en su lugar contiene índices para su uso en llamadas a DrawIndexedPrimitive. Se recomienda encarecidamente que utilice búferes de índice en lugar de memoria sin procesar asignada a la aplicación cuando sea posible, por las mismas razones que los búferes de vértices.

</dd> <dt>

<span id="I_notice_that_32-bit_indices_are_a_supported_type__can_I_use_them_on_all_devices__"></span><span id="i_notice_that_32-bit_indices_are_a_supported_type__can_i_use_them_on_all_devices__"></span><span id="I_NOTICE_THAT_32-BIT_INDICES_ARE_A_SUPPORTED_TYPE__CAN_I_USE_THEM_ON_ALL_DEVICES__"></span>**Observe que los índices de 32 bits son un tipo admitido. ¿puedo utilizarlos en todos los dispositivos?** 
</dt> <dd>

No. Debe comprobar el campo D3DCAPS9:: MaxVertexIndex para determinar el valor de índice máximo compatible con el dispositivo. Este valor debe ser mayor que 2 para el 16 de Power-1 (0xFFFF) con el fin de que se admitan los búferes de índice de tipo D3DFMT \_ INDEX32. Además, tenga en cuenta que algunos dispositivos pueden admitir índices de 32 bits, pero admiten un valor de índice máximo inferior a 2 para el 32 º Power-1 (0xFFFFFFFF); en este caso, la aplicación debe respetar el límite indicado por el dispositivo.

</dd> <dt>

<span id="Does_S_W_vertex_processing_support_64_bit__"></span><span id="does_s_w_vertex_processing_support_64_bit__"></span><span id="DOES_S_W_VERTEX_PROCESSING_SUPPORT_64_BIT__"></span>**¿El procesamiento de vértices S/W es compatible con 64 bits?** 
</dt> <dd>

Hay una canalización de vértices s/w optimizada para x64, pero no existe para IA64.

</dd> </dl>

### <a name="performance-tuning"></a>Optimización del rendimiento

<dl> <dt>

<span id="How_can_I_improve_the_performance_of_my_Direct3D_application__"></span><span id="how_can_i_improve_the_performance_of_my_direct3d_application__"></span><span id="HOW_CAN_I_IMPROVE_THE_PERFORMANCE_OF_MY_DIRECT3D_APPLICATION__"></span>**¿Cómo puedo mejorar el rendimiento de mi aplicación de Direct3D?** 
</dt> <dd>

A continuación se indican las áreas clave que se deben examinar al optimizar el rendimiento:

<dl> <dt>

<span id="Batch_size_"></span><span id="batch_size_"></span><span id="BATCH_SIZE_"></span>**Tamaño de lote** 
</dt> <dd>

Direct3D está optimizado para lotes grandes de primitivas. Cuanto mayor sea el número de polígonos que se pueden enviar en una sola llamada, mejor. Una buena regla general es dirigirse al promedio de vértices 1000 por llamada primitiva. Por debajo de ese nivel, es probable que no se obtenga un rendimiento óptimo, por encima de eso y que se encuentre en disminución de devoluciones y conflictos potenciales con consideraciones de simultaneidad (consulte a continuación).

</dd> <dt>

<span id="State_changes_"></span><span id="state_changes_"></span><span id="STATE_CHANGES_"></span>**Cambios de estado** 
</dt> <dd>

Cambiar el estado de representación puede ser una operación costosa, especialmente cuando se cambia la textura. Por esta razón, es importante minimizar tanto como sea posible el número de cambios de estado realizados por fotograma. Además, intente minimizar los cambios en el búfer de vértice o de índice.

> [!Note]  
> A partir de DirectX 8, el costo de cambiar el búfer de vértices ya no es tan caro como lo era con versiones anteriores, pero sigue siendo recomendable evitar cambios en el búfer de vértices siempre que sea posible.

 

</dd> <dt>

<span id="Concurrency"></span><span id="concurrency"></span><span id="CONCURRENCY"></span>**Simultaneidad**
</dt> <dd>

Si se puede organizar para realizar la representación simultáneamente con otro procesamiento, se aprovechará al máximo el rendimiento del sistema. Este objetivo puede entrar en conflicto con el objetivo de reducir los cambios de renderstate. Debe lograr un equilibrio entre el procesamiento por lotes para reducir los cambios de estado y la inserción de datos en el controlador antes de ayudar a conseguir la simultaneidad. El uso de varios búferes de vértices en modo Round Robin puede ayudar con la simultaneidad.

</dd> <dt>

<span id="Texture_uploads_"></span><span id="texture_uploads_"></span><span id="TEXTURE_UPLOADS_"></span>**Cargas de texturas** 
</dt> <dd>

La carga de texturas en el dispositivo consume ancho de banda y provoca una competición de ancho de banda con datos de vértice. Por lo tanto, es importante no sobrepasar la memoria de textura, lo que haría que el esquema de almacenamiento en caché cargara cantidades excesivas de texturas en cada fotograma.

</dd> <dt>

<span id="Vertex_and_index_buffers_"></span><span id="vertex_and_index_buffers_"></span><span id="VERTEX_AND_INDEX_BUFFERS_"></span>**Búferes de vértices y de índices** 
</dt> <dd>

Siempre debe usar búferes de vértices y de índices, en lugar de bloques sin formato de memoria asignada a la aplicación. Como mínimo, la semántica de bloqueo de los búferes de vértices y de índices puede evitar una operación de copia redundante. Con algunos controladores, el búfer de vértice o de índice se puede colocar en una memoria más óptima (quizás en la memoria de vídeo o AGP) para el acceso por parte del hardware.

</dd> <dt>

<span id="State_macro_blocks_"></span><span id="state_macro_blocks_"></span><span id="STATE_MACRO_BLOCKS_"></span>**Bloques de macros de estado** 
</dt> <dd>

Se introdujeron en DirectX 7,0. Proporcionan un mecanismo para registrar una serie de cambios de estado (incluidos los cambios de iluminación, material y matriz) en una macro, que después se puede reproducir mediante una sola llamada. Esto tiene dos ventajas:

-   Para reducir la sobrecarga de llamadas, realice una llamada en lugar de muchas.
-   Un controlador compatible puede realizar el análisis previo y la precompilación de los cambios de estado, lo que agiliza el envío al hardware de gráficos.

Los cambios de estado pueden seguir siendo caros, pero el uso de macros de estado puede ayudar a reducir al menos parte del costo. Use un solo dispositivo Direct3D. Si necesita representar varios destinos, use SetRenderTarget. Si va a crear una aplicación de ventana con varias ventanas 3D, use la API de CreateAdditionalSwapChain. El tiempo de ejecución está optimizado para un único dispositivo y existe una penalización de velocidad considerable para el uso de varios dispositivos.

</dd> </dl> </dd> <dt>

<span id="Which_primitive_types__strips__fans__lists_and_so_on__should_I_use__"></span><span id="which_primitive_types__strips__fans__lists_and_so_on__should_i_use__"></span><span id="WHICH_PRIMITIVE_TYPES__STRIPS__FANS__LISTS_AND_SO_ON__SHOULD_I_USE__"></span>**¿Qué tipos primitivos (tiras, ventiladores, listas, etc.) debo usar?** 
</dt> <dd>

Muchas de las mallas que se encuentran en los vértices de características de datos reales compartidas por varios polígonos. Para maximizar el rendimiento, es conveniente reducir la duplicación en los vértices transformados y enviados a través del bus al dispositivo de representación. Es evidente que el uso de listas de triángulos simples no consigue compartir vértices, por lo que es el método menos óptimo. La elección es después de usar tiras y fans, lo que implica una relación de conectividad específica entre polígonos y el uso de listas indizadas. En los casos en los que los datos se encuentran en bandas y ventiladores, se trata de la opción más adecuada, ya que minimizan los datos que se envían al controlador. Sin embargo, la descomposición de mallas en bandas y ventiladores suele tener como resultado un gran número de partes independientes, lo que implica un gran número de llamadas DrawPrimitive. Por esta razón, el método más eficaz suele usar una única llamada a DrawIndexedPrimitive con una lista de triángulos. Una ventaja adicional del uso de una lista indizada es que se puede obtener una ventaja incluso cuando los triángulos consecutivos solo comparten un único vértice. En Resumen, si los datos se encuentran en bandas o ventiladores grandes, Use tiras o ventiladores. de lo contrario, use listas indizadas.

</dd> <dt>

<span id="How_do_you_determine_the_total_texture_memory_a_card_has__excluding_AGP_memory__"></span><span id="how_do_you_determine_the_total_texture_memory_a_card_has__excluding_agp_memory__"></span><span id="HOW_DO_YOU_DETERMINE_THE_TOTAL_TEXTURE_MEMORY_A_CARD_HAS__EXCLUDING_AGP_MEMORY__"></span>**¿Cómo se determina la memoria de textura total que tiene una tarjeta, excluida la memoria AGP?** 
</dt> <dd>

[**IDirect3DDevice9:: GetAvailableTextureMem**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getavailabletexturemem) devuelve la memoria total disponible, incluida la AGP. Asignación de recursos en función de una suposición de la cantidad de memoria de vídeo que no es una buena idea. Por ejemplo, ¿qué ocurre si la tarjeta se está ejecutando en una arquitectura de memoria unificada (UMA) o puede comprimir las texturas? Puede haber más espacio disponible de lo que podría haber pensado. Debe crear recursos y comprobar si hay errores de memoria insuficiente y, a continuación, volver a escalar las texturas. Por ejemplo, puede quitar los niveles de MIP principales de las texturas.

</dd> <dt>

<span id="What_s_a_good_usage_pattern_for_vertex_buffers_if_I_m_generating_dynamic_data__"></span><span id="what_s_a_good_usage_pattern_for_vertex_buffers_if_i_m_generating_dynamic_data__"></span><span id="WHAT_S_A_GOOD_USAGE_PATTERN_FOR_VERTEX_BUFFERS_IF_I_M_GENERATING_DYNAMIC_DATA__"></span>**¿Qué es un buen patrón de uso de los búferes de vértices si se generan datos dinámicos?** 
</dt> <dd>

1.  Cree un búfer de vértices mediante las marcas de uso de D3DUSAGE \_ Dynamic y D3DUSAGE \_ WRITEONLY y el \_ marcador de grupo predeterminado D3DPOOL. (Especifique también D3DUSAGE \_ SOFTWAREPROCESSING si está utilizando el procesamiento de vértices de software).
2.  I = 0.
3.  Establezca el estado (texturas, renderstates, etc.).
4.  Compruebe si hay espacio en el búfer, es decir, por ejemplo, I + M <= N? (Donde M es el número de vértices nuevos).
5.  En caso afirmativo, bloquee VB con D3DLOCK \_ NOOVERWRITE. Esto indica a Direct3D y al controlador que va a agregar los vértices y no modificará los que previamente haya procesado por lotes. Por lo tanto, si una operación DMA estuviera en curso, no se interrumpe. Si no es así, vaya 11.
6.  Rellene los vértices M en I.
7.  Pulsa.
8.  Llame a Draw \[ indexed \] primitivo. En el caso de primitivas no indizadas, use I como parámetro StartVertex. En el caso de las primitivas indizadas, asegúrese de que los índices señalan a la parte correcta del búfer de vértices (puede que sea más fácil usar el parámetro BaseVertexIndex de la llamada a SetIndices para lograrlo).
9.  I + = M.
10. Goto 3.
11. Bien, no hay espacio suficiente, así que Permítanos empezar con un nuevo VB. No queremos usar el mismo, ya que puede haber una operación DMA en curso. Nos comunicamos con esto a Direct3D y el controlador mediante el bloqueo del mismo VB con la \_ marca discard de D3DLOCK. Lo que esto significa es "puede enviarme un nuevo puntero porque he terminado con el antiguo y no me importa realmente el contenido anterior".
12. I = 0.
13. Goto 4 (o 6).

</dd> <dt>

<span id="Why_do_I_have_to_specify_more_information_in_the_D3DVERTEXELEMENT9_structure__"></span><span id="why_do_i_have_to_specify_more_information_in_the_d3dvertexelement9_structure__"></span><span id="WHY_DO_I_HAVE_TO_SPECIFY_MORE_INFORMATION_IN_THE_D3DVERTEXELEMENT9_STRUCTURE__"></span>**¿Por qué tengo que especificar más información en la estructura D3DVERTEXELEMENT9?** 
</dt> <dd>

A partir de Direct3D 9, la declaración de flujo de vértices ya no es solo una matriz DWORD, ahora es una matriz de estructuras D3DVERTEXELEMENT9. El tiempo de ejecución usa la información semántica y de uso adicional para enlazar el contenido de los flujos de vértices con las variables o los registros de entrada de los sombreadores de vértices. En Direct3D 9, las declaraciones de vértices se desacoplan de los sombreadores de vértices, lo que facilita el uso de sombreadores con geometrías de diferentes formatos, ya que el tiempo de ejecución solo enlaza los datos que necesita el sombreador.

Las nuevas declaraciones de vértices se pueden usar con la canalización de función fija o con sombreadores. En el caso de la canalización de funciones fijas, no es necesario llamar a SetVertexShader. En cambio, si desea cambiar a la canalización de función fija y ha usado previamente un sombreador de vértices, llame a SetVertexShader (NULL). Una vez hecho esto, deberá llamar a SetFVF para declarar el código FVF.

Al usar sombreadores de vértices, llame a SetVertexShader con el objeto de sombreador de vértices. Además, llame a SetFVF para configurar una declaración de vértice. Usa la información implícita en el FVF. Se puede llamar a SetVertexDeclaration en lugar de SetFVF porque admite declaraciones de vértices que no se pueden expresar con un FVF.

</dd> </dl>

### <a name="d3dx-utility-library"></a>Biblioteca de utilidades de D3DX

<dl> <dt>

<span id="What_file_formats_are_supported_by_the_D3DX_image_file_loader_functions__"></span><span id="what_file_formats_are_supported_by_the_d3dx_image_file_loader_functions__"></span><span id="WHAT_FILE_FORMATS_ARE_SUPPORTED_BY_THE_D3DX_IMAGE_FILE_LOADER_FUNCTIONS__"></span>**¿Qué formatos de archivo son compatibles con las funciones del cargador de archivos de imagen de D3DX?** 
</dt> <dd>

Las funciones del cargador de archivos de imagen de D3DX admiten archivos BMP, TGA, JPG, DIB, PPM y DDS.

</dd> <dt>

<span id="The_text_rendering_functions_in_D3DX_don_t_seem_to_work__what_am_I_doing_wrong__"></span><span id="the_text_rendering_functions_in_d3dx_don_t_seem_to_work__what_am_i_doing_wrong__"></span><span id="THE_TEXT_RENDERING_FUNCTIONS_IN_D3DX_DON_T_SEEM_TO_WORK__WHAT_AM_I_DOING_WRONG__"></span>**Parece que las funciones de representación de texto en D3DX no funcionan, ¿qué estoy haciendo mal?** 
</dt> <dd>

Un error común al usar las funciones ID3DXFont::D rawText es especificar un componente alfa de cero para el parámetro de color; resultado en texto completamente transparente (es decir, invisible). En el caso de texto totalmente opaco, asegúrese de que el componente alfa del parámetro de color esté totalmente saturado (255).

</dd> <dt>

<span id="How_can_I_save_the_contents_of_a_surface_or_texture_to_a_file__"></span><span id="how_can_i_save_the_contents_of_a_surface_or_texture_to_a_file__"></span><span id="HOW_CAN_I_SAVE_THE_CONTENTS_OF_A_SURFACE_OR_TEXTURE_TO_A_FILE__"></span>**¿Cómo se puede guardar el contenido de una superficie o textura en un archivo?** 
</dt> <dd>

El SDK de DirectX 8,1 agregó dos funciones a la biblioteca de D3DX específicamente para este propósito: D3DXSaveSurfaceToFile () y D3DXSaveTextureToFile (). Estas funciones permiten guardar una imagen en un archivo en formato BMP o DDS. En versiones anteriores tendrá que bloquear la superficie y leer los datos de la imagen y, a continuación, escribirla en un archivo de mapa de bits. Para obtener información sobre cómo escribir una función para almacenar mapas de bits, consulte [almacenamiento de una imagen](/windows/desktop/gdi/storing-an-image).

Como alternativa, se podría usar GDI+ para guardar la imagen en una amplia variedad de formatos, aunque esto requiere que los archivos de compatibilidad adicionales se distribuyan con la aplicación.

</dd> <dt>

<span id="How_can_I_make_use_of_the_High_Level_Shader_Language__HLSL__in_my_game__"></span><span id="how_can_i_make_use_of_the_high_level_shader_language__hlsl__in_my_game__"></span><span id="HOW_CAN_I_MAKE_USE_OF_THE_HIGH_LEVEL_SHADER_LANGUAGE__HLSL__IN_MY_GAME__"></span>**¿Cómo puedo usar el lenguaje de sombreador de alto nivel (HLSL) en mi juego?** 
</dt> <dd>

El lenguaje de sombreador de alto nivel (HLSL) de Microsoft se puede incorporar en el motor de juegos de tres maneras:

-   Compile el origen del sombreador en el ensamblado de sombreado de vértices o píxeles (mediante la utilidad de línea de comandos fxc.exe) y use D3DXAssembleShader () en tiempo de ejecución. De este modo, incluso un juego de DirectX 8 puede incluso sacar provecho de la eficacia de HLSL.
-   Use D3DXCompileShader () para compilar el origen del sombreador en el flujo de tokens y en el formato de tabla de constantes. En tiempo de ejecución, cargue el flujo de tokens y la tabla de constantes, y llame a CreateVertexShader () o CreatePixelShader () en el dispositivo para crear los sombreadores.
-   La forma más fácil de empezar a trabajar es aprovechar el sistema de efectos de D3DX llamando a D3DXCreateEffectFromFile () o D3DXCreateEffectFromResource () con el archivo de efectos.

</dd> <dt>

<span id="What_is_the_purpose_of_the_new_shader_compiler_flag__"></span><span id="what_is_the_purpose_of_the_new_shader_compiler_flag__"></span><span id="WHAT_IS_THE_PURPOSE_OF_THE_NEW_SHADER_COMPILER_FLAG__"></span>**¿Cuál es el propósito de la nueva marca de compilador de sombreador?** 
</dt> <dd>

A partir del SDK de DirectX de diciembre de 2006, se ha habilitado el nuevo compilador de HLSL desarrollado para Direct3D 10 para los destinos de Direct3D 9. El nuevo compilador no admite los \_ destinos PS 1 \_ x y ahora es el compilador predeterminado para todos los sombreadores HLSL de Direct3D. Se puede usar una marca para la compatibilidad con versiones anteriores para forzar \_ \_ que los destinos de PS 1 x se compilen como \_ destinos PS 2 \_ 0.

Las aplicaciones que desean usar el compilador heredado pueden seguir haciendo esto proporcionando una marca en tiempo de ejecución (vea las [**marcas del compilador**](/windows/desktop/direct3d9/d3dxshader-flags)) o proporcionando un modificador cuando se usa FXC.

</dd> <dt>

<span id="What_is_the_correct_way_to_get_shaders_from_an_Effect__"></span><span id="what_is_the_correct_way_to_get_shaders_from_an_effect__"></span><span id="WHAT_IS_THE_CORRECT_WAY_TO_GET_SHADERS_FROM_AN_EFFECT__"></span>**¿Cuál es la manera correcta de obtener sombreadores de un efecto?** 
</dt> <dd>

Use D3DXCreateEffect para crear un ID3DXEffect y, a continuación, use GetPassDesc para recuperar una descripción de D3DXPASS \_ . Esta estructura contiene punteros a los sombreadores de vértices y píxeles.

No use ID3DXEffectCompiler:: GetPassDesc. Los identificadores de sombreador de vértices y píxeles devueltos por este método son NULL.

</dd> <dt>

<span id="What_is_the_HLSL_noise___intrinsic_for__"></span><span id="what_is_the_hlsl_noise___intrinsic_for__"></span><span id="WHAT_IS_THE_HLSL_NOISE___INTRINSIC_FOR__"></span>**¿Para qué sirve el intrínseco de ruido de HLSL ()?** 
</dt> <dd>

La función de ruido intrínseca genera Perl en el ruido tal y como se define en Ken Perl. Actualmente, la función HLSL solo se puede usar para rellenar las texturas en los sombreadores de textura, ya que la h/w actual no admite el método de forma nativa. Los sombreadores de textura se usan en conjuction con las \* funciones D3DXFill Texture (), que son funciones auxiliares útiles para generar texturas definidas por procedimientos durante el tiempo de carga.

</dd> <dt>

<span id="How_do_I_detect_whether_to_use_pixel_shader_model_2.0_or_2.a__"></span><span id="how_do_i_detect_whether_to_use_pixel_shader_model_2.0_or_2.a__"></span><span id="HOW_DO_I_DETECT_WHETHER_TO_USE_PIXEL_SHADER_MODEL_2.0_OR_2.A__"></span>**Cómo detectar si usar el modelo de sombreador de píxeles 2,0 o 2. a?** 
</dt> <dd>

Puede usar las funciones D3DXGetPixelShaderProfile () y D3DXGetPixelShaderProfile () que devuelven una cadena que determina qué Perfil de HLSL es más adecuado para el dispositivo que se ejecuta.

</dd> <dt>

<span id="How_do_I_access_the_Parameters_in_my_Precompiled_Effects_Shaders__"></span><span id="how_do_i_access_the_parameters_in_my_precompiled_effects_shaders__"></span><span id="HOW_DO_I_ACCESS_THE_PARAMETERS_IN_MY_PRECOMPILED_EFFECTS_SHADERS__"></span>**Cómo tener acceso a los parámetros de mis sombreadores de efectos precompilados** 
</dt> <dd>

A través de la interfaz ID3DXConstantTable que se usa para tener acceso a la tabla de constantes. Esta tabla contiene las variables que usan los sombreadores y efectos de lenguaje de alto nivel.

</dd> <dt>

<span id="Is_there_a_way_to_add_user_data_to_an_effect_or_other_resource__"></span><span id="is_there_a_way_to_add_user_data_to_an_effect_or_other_resource__"></span><span id="IS_THERE_A_WAY_TO_ADD_USER_DATA_TO_AN_EFFECT_OR_OTHER_RESOURCE__"></span>**¿Hay alguna manera de agregar datos de usuario a un efecto u otro recurso?** 
</dt> <dd>

Sí, para establecer datos privados se llama a SetPrivateData (pReal es el objeto de textura D3D, pSpoof es el objeto de textura ajustado).

``` syntax
hr = pReal->SetPrivateData(IID_Spoof, &pSpoof, 
            sizeof(IDirect3DResource9*), 0)));
```

Para buscar el puntero ajustado:

``` syntax
    IDirect3DResource9* pSpoof;
    DWORD dwSize = sizeof(pSpoof);
    hr = pReal->GetPrivateData(IID_Spoof, (void*) &pSpoof, &dwSize);
```

</dd> <dt>

<span id="Why_does_rendering_of_an_ID3DXMesh_object_slow_down_significantly_after_I_define_subsets__"></span><span id="why_does_rendering_of_an_id3dxmesh_object_slow_down_significantly_after_i_define_subsets__"></span><span id="WHY_DOES_RENDERING_OF_AN_ID3DXMESH_OBJECT_SLOW_DOWN_SIGNIFICANTLY_AFTER_I_DEFINE_SUBSETS__"></span>**¿Por qué la representación de un objeto ID3DXMesh se ralentiza significativamente después de definir subconjuntos?** 
</dt> <dd>

Probablemente no ha optimizado la malla después de definir los atributos de la superficie. Si especifica los atributos y, a continuación, llama a ID3DXMesh::D rawSubset (), este método debe realizar una búsqueda de la malla para todas las caras que contienen los atributos solicitados. Además, las caras representadas suelen estar en un patrón de acceso aleatorio, por lo que no se usa la caché de vértices. Después de definir los atributos de caras para los subconjuntos, llame a los métodos ID3DXMesh:: Optimize o ID3DXMesh:: OptimizeInPlace y especifique un método de optimización de D3DXMESHOPT \_ ATTRSORT o strong. Tenga en cuenta que, para un rendimiento óptimo, debe optimizar con la \_ marca D3DXMESHOPT VERTEXCACHE, que también reordenará los vértices para un uso óptimo de la memoria caché de vértices. La matriz de adyacencias generada para una malla de D3DX tiene tres entradas por cara, pero es posible que algunas caras no tengan caras adyacentes en los tres bordes. ¿Cómo se codifica? Las entradas en las que no hay caras adyacentes se codifican como 0xFFFFFFFF.

</dd> <dt>

<span id="I_ve_heard_a_lot_about_Pre-computed_Radiance_Transfer__PRT___where_can_I_learn_more__"></span><span id="i_ve_heard_a_lot_about_pre-computed_radiance_transfer__prt___where_can_i_learn_more__"></span><span id="I_VE_HEARD_A_LOT_ABOUT_PRE-COMPUTED_RADIANCE_TRANSFER__PRT___WHERE_CAN_I_LEARN_MORE__"></span>**Me he escuchado mucho sobre la transferencia Radiance (PRT) calculada previamente, ¿Dónde puedo obtener más información?** 
</dt> <dd>

PRT es una nueva característica de D3DX agregada en la actualización del SDK del verano de 2003. Permite la representación de escenarios de iluminación complejos como global-llumination, instantánea de software y dispersión de subsuperficies en tiempo real. El SDK contiene documentación y ejemplos de cómo integrar la tecnología en el juego. En el ejemplo de demostración de PRT y ejemplos de ejemplo LocalDeformablePRT se muestra cómo usar el simulador para escenarios de iluminación por vértice y por píxel respectivamente. También puede encontrar más información sobre este y otros temas en la Página Web de Peter Pikes Sloan.

</dd> <dt>

<span id="How_can_I_render_to_a_texture_and_make_use_of_Anti_Aliasing__"></span><span id="how_can_i_render_to_a_texture_and_make_use_of_anti_aliasing__"></span><span id="HOW_CAN_I_RENDER_TO_A_TEXTURE_AND_MAKE_USE_OF_ANTI_ALIASING__"></span>**¿Cómo puedo representar una textura y hacer uso del suavizado de contorno?** 
</dt> <dd>

Cree un destino de representación multimuestreado mediante Direct3DDevice9:: CreateRenderTarget. Después de representar la escena en ese destino de representación, StretchRect de ella a una textura de destino de representación. Si cambia el textre oculto (como desenfoque o floración), cópielo de nuevo en el búfer de reserva antes de presentar ().

</dd> </dl>

## <a name="directsound-questions"></a>Preguntas sobre DirectSound

<dl> <dt>

<span id="Why_do_I_get_a_burst_of_static_when_my_application_starts_up__I_notice_this_problem_with_other_applications_too._"></span><span id="why_do_i_get_a_burst_of_static_when_my_application_starts_up__i_notice_this_problem_with_other_applications_too._"></span><span id="WHY_DO_I_GET_A_BURST_OF_STATIC_WHEN_MY_APPLICATION_STARTS_UP__I_NOTICE_THIS_PROBLEM_WITH_OTHER_APPLICATIONS_TOO._"></span>**¿Por qué obtengo una ráfaga de estático cuando se inicia la aplicación? Observe también este problema con otras aplicaciones.** 
</dt> <dd>

Probablemente ha instalado el tiempo de ejecución de depuración de DirectX. La versión de depuración del tiempo de ejecución llena los búferes con static para ayudar a los desarrolladores a detectar errores con búferes no inicializados. No se puede garantizar el contenido de un búfer de DirectSound tras su creación; en concreto, no puede suponer que un búfer con se ponga en cero.

</dd> <dt>

<span id="Why_I_am_experiencing_a_delay_in_between_changing_an_effects_parameters_and_hearing_the_results__"></span><span id="why_i_am_experiencing_a_delay_in_between_changing_an_effects_parameters_and_hearing_the_results__"></span><span id="WHY_I_AM_EXPERIENCING_A_DELAY_IN_BETWEEN_CHANGING_AN_EFFECTS_PARAMETERS_AND_HEARING_THE_RESULTS__"></span>**¿Por qué tengo un retraso entre el cambio de parámetros de efectos y la audición de los resultados?** 
</dt> <dd>

Los cambios en los parámetros de efecto no siempre se realizan inmediatamente en DirectX 8. Por motivos de eficacia, DirectSound procesa 100 milisegundos de datos de sonido en un búfer, comenzando por el cursor de reproducción, antes de que se reproduzca el búfer. Este preprocesamiento se produce después de todas las llamadas siguientes:

``` syntax
IDirectSoundBuffer8::SetCurrentPosition
IDirectSoundBuffer8::SetFX
IDirectSoundBuffer8::Stop
IDirectSoundBuffer8::Unlock
```

A partir de DirectX 9, un nuevo algoritmo de procesamiento de FX que procesa los efectos Just-in-Time soluciona este problema y ha reducido la latencia. El algoritmo se ha agregado a la llamada IDirectSoundBuffer8::P (), junto con un subproceso adicional que procesa los efectos justo antes del cursor de escritura. Por lo tanto, puede establecer parámetros en cualquier momento y funcionan según lo previsto. Sin embargo, tenga en cuenta que en un búfer de reproducción habrá un pequeño retraso (normalmente 100 ms) antes de oír el cambio de parámetro, ya que el audio entre los cursores de reproducción y escritura (y un relleno de más bits) ya se ha procesado en ese momento.

</dd> <dt>

<span id="How_do_I_detect_if_DSound_is_installed__"></span><span id="how_do_i_detect_if_dsound_is_installed__"></span><span id="HOW_DO_I_DETECT_IF_DSOUND_IS_INSTALLED__"></span>**Cómo detectar si DSound está instalado?** 
</dt> <dd>

Si no necesita usar DirectSoundEnumerate () para enumerar los dispositivos DSound disponibles, no vincule la aplicación con dsound. lib y, en su lugar, úsela a través de com CoCreateInstance (CLSID \_ DirectSound...) y, a continuación, inicialice el objeto dsound mediante Initialize (NULL). Si necesita usar DirectSoundEnumerate (), puede cargar dinámicamente dsound.dll mediante LoadLibrary ("dsound.dll"); y tienen acceso a sus métodos mediante GetProcAddress ("DirectSoundEnumerateA/W") y GetProcAddress ("DirectSoundCreateA/W"), etc.

</dd> <dt>

<span id="How_do_I_create_multichannel_audio_with_WAVEFORMATEXTENSIBLE__"></span><span id="how_do_i_create_multichannel_audio_with_waveformatextensible__"></span><span id="HOW_DO_I_CREATE_MULTICHANNEL_AUDIO_WITH_WAVEFORMATEXTENSIBLE__"></span>**Cómo crear audio multicanal con WAVEFORMATEXTENSIBLE?** 
</dt> <dd>

Si no encuentra una respuesta a su pregunta en los archivos de ayuda de DirectSound, hay un buen artículo con más información disponible en varios archivos de audio y datos de audio de canal.

</dd> <dt>

<span id="How_can_I_use_the_DirectSound_Voice_Manager_with_property_sets_like_EAX__"></span><span id="how_can_i_use_the_directsound_voice_manager_with_property_sets_like_eax__"></span><span id="HOW_CAN_I_USE_THE_DIRECTSOUND_VOICE_MANAGER_WITH_PROPERTY_SETS_LIKE_EAX__"></span>**¿Cómo puedo usar el administrador de voz de DirectSound con conjuntos de propiedades como EAX?** 
</dt> <dd>

En DirectSound 9,0 al duplicar un búfer, ahora es posible obtener la interfaz IDirectSoundBuffer8 en el búfer duplicado, que le proporcionará acceso al método AcquireResources. Esto le permitirá asociar un búfer con la \_ marca LOCDEFER de DSBCAPS con un recurso de hardware. Después, puede establecer los parámetros de EAX en este búfer antes de tener que llamar a Play ().

</dd> <dt>

<span id="I_am_having_problems_with_unreliable_behavior_when_using_cursor_position_notifications._How_can_I_get_more_accurate_information__"></span><span id="i_am_having_problems_with_unreliable_behavior_when_using_cursor_position_notifications._how_can_i_get_more_accurate_information__"></span><span id="I_AM_HAVING_PROBLEMS_WITH_UNRELIABLE_BEHAVIOR_WHEN_USING_CURSOR_POSITION_NOTIFICATIONS._HOW_CAN_I_GET_MORE_ACCURATE_INFORMATION__"></span>**Tengo problemas con un comportamiento no confiable al usar las notificaciones de posición del cursor. ¿Cómo puedo obtener información más precisa?** 
</dt> <dd>

Hay algunos errores sutiles en varias versiones de DirectSound, la pila de audio básica de Windows y controladores de audio que hacen que las notificaciones de las posiciones de los cursores no sean confiables. A menos que tenga como destino una configuración de HW/SW conocida en la que sepa que las notificaciones están bien comportadas, evite las notificaciones de posición del cursor. Para el seguimiento de la posición, GetCurrentPosition () es una técnica más segura.

</dd> <dt>

<span id="I_am_suffering_from_performance_degradation_when_using_GetCurrentPosition__._What_can_I_do_to_improve_performance__"></span><span id="i_am_suffering_from_performance_degradation_when_using_getcurrentposition__._what_can_i_do_to_improve_performance__"></span><span id="I_AM_SUFFERING_FROM_PERFORMANCE_DEGRADATION_WHEN_USING_GETCURRENTPOSITION__._WHAT_CAN_I_DO_TO_IMPROVE_PERFORMANCE__"></span>**Estoy sufriendo la degradación del rendimiento cuando se usa GetCurrentPosition (). ¿Qué puedo hacer para mejorar el rendimiento?** 
</dt> <dd>

Cada llamada a GetCurrentPosition () en cada búfer produce una llamada del sistema y las llamadas del sistema se deben minimizar, ya que son un componente grande de la superficie de la CPU de DSound. En NT (Win2K y XP), los cursores de los búferes de software (y los búferes de HW en algunos dispositivos) se mueven en incrementos de 10 ms, por lo que llamar a GetCurrentPosition () cada 10 ms es ideal. Llamar a este método con mayor frecuencia que cada 5 ms producirá una degradación del rendimiento.

</dd> <dt>

<span id="My_DirectSound_application_is_taking_up_too_much_CPU_time_or_is_performing_slowly._Is_there_anything_I_can_do_to_optimize_my_code__"></span><span id="my_directsound_application_is_taking_up_too_much_cpu_time_or_is_performing_slowly._is_there_anything_i_can_do_to_optimize_my_code__"></span><span id="MY_DIRECTSOUND_APPLICATION_IS_TAKING_UP_TOO_MUCH_CPU_TIME_OR_IS_PERFORMING_SLOWLY._IS_THERE_ANYTHING_I_CAN_DO_TO_OPTIMIZE_MY_CODE__"></span>**Mi aplicación DirectSound está tardando demasiado tiempo de CPU o se está ejecutando lentamente. ¿Hay algo que pueda hacer para optimizar mi código?** 
</dt> <dd>

Hay varias cosas que puede hacer para mejorar el rendimiento del código de audio:

-   No llame a GetCurrentPosition con demasiada frecuencia. Cada llamada a GetCurrentPosition () en cada búfer produce una llamada del sistema y las llamadas del sistema se deben minimizar, ya que son un componente grande de la superficie de la CPU de DSound. En NT (Win2K y XP), los cursores de los búferes de software (y los búferes de HW en algunos dispositivos) se mueven en incrementos de 10 ms, por lo que llamar a GetCurrentPosition () cada 10 ms es ideal. Llamar a este método con mayor frecuencia que cada 5 ms producirá una degradación del rendimiento.
-   Use una velocidad de fotogramas independiente y menor para el audio. En la actualidad, muchos juegos de Windows pueden superar 100 fotogramas por segundo y no es necesario en la mayoría de los casos actualizar los parámetros de audio 3D a la misma velocidad de fotogramas. El procesamiento del audio cada segundo o tercer fotograma gráfico, o cada 30ms, puede reducir significativamente el número de llamadas de audio en toda la aplicación sin reducir la calidad del audio.
-   Use DS3D \_ diferido para objetos 3D. La mayoría de las tarjetas de sonido responden inmediatamente a los cambios de parámetros y, en un solo fotograma, pueden cambiar, especialmente si se cambia la posición o la orientación del agente de escucha. Esto hace que la tarjeta de sonido y la CPU realicen muchos cálculos innecesarios, por lo que otra optimización rápida y universal consiste en aplazar algunos cambios en los parámetros y confirmarlos al final del marco.

    o, al menos, use SetAllParameters en lugar de llamadas de Set3DParamX individuales en búferes.

    Del mismo modo, debe usar al menos llamadas a SetAllParamenters en búferes 3D, en lugar de llamadas a Set3DParamX individuales. Simplemente intente minimizar las llamadas del sistema siempre que sea posible.

-   No realizar llamadas redundantes; almacenar y ordenar una lista de llamadas de reproducción. A menudo, en un marco de actualización de audio hay dos solicitudes para reproducir nuevos sonidos. Si las solicitudes se procesan a medida que llegan, el primer sonido nuevo podría iniciarse y, a continuación, reemplazarse inmediatamente por el segundo sonido solicitado. Esto produce cálculos redundantes, una llamada de reproducción innecesaria y una llamada de detención innecesaria. Es mejor almacenar una lista de solicitudes para que se reproduzcan nuevos sonidos, de modo que la lista se pueda ordenar y solo se reproduzcan en realidad las voces que deberían comenzar a reproducirse.

    Además, debe almacenar las copias locales de los parámetros 3D y EAX de cada origen de sonido. Si se realiza una solicitud para establecer un parámetro en un valor determinado, puede comprobar si el valor es realmente diferente del último conjunto de valores. Si no es así, no es necesario realizar la llamada.

    Aunque el controlador de la tarjeta de sonido probablemente detectará este escenario y no realice el cálculo (el mismo) de nuevo, la llamada de audio tendrá que llegar al controlador de audio (a través de una transición de anillo) y esto ya es una operación lenta.

</dd> <dt>

<span id="When_I_stream_a_buffer_it_tends_to_glitch_and_perform_poorly._What_s_the_best_way_to_stream_a_buffer__"></span><span id="when_i_stream_a_buffer_it_tends_to_glitch_and_perform_poorly._what_s_the_best_way_to_stream_a_buffer__"></span><span id="WHEN_I_STREAM_A_BUFFER_IT_TENDS_TO_GLITCH_AND_PERFORM_POORLY._WHAT_S_THE_BEST_WAY_TO_STREAM_A_BUFFER__"></span>**Cuando streamo un búfer tiende a ser un problema y funciona mal. ¿Cuál es la mejor manera de transmitir un búfer?** 
</dt> <dd>

Al transmitir audio en un búfer, hay dos algoritmos básicos: After-Write-cursor (AWC) y Before-Play-cursor (BPC). AWC minimiza la latencia a costa de un problema, mientras que BPC es lo contrario. Dado que no suele haber cambios interactivos en el sonido transmitido, este tipo de latencia no suele ser un problema para juegos y aplicaciones similares, por lo que BPC es el algoritmo más adecuado. En AWC, cada vez que se ejecuta el subproceso de streaming, los datos de los búferes de bucle se encuentran hasta N MS más allá de los cursores de escritura (normalmente N = 40, o bien, para permitir la vibración de programación de Windows). En BPC, siempre se escriben tantos datos en los búferes como sea posible, y se rellenan justo hasta sus cursores de reproducción (o quizás 32 bytes antes de permitir los controladores que informan incorrectamente del progreso de los cursores de reproducción).

Use BPC para Mimimize el problema y use búferes de 100 ms o más, incluso si sus juegos no se ejecutan en el hardware de prueba, se producirá un problema en algunos equipos.

</dd> <dt>

<span id="I_am_playing_the_same_sounds_over_and_over_very_often_and_very_quickly_and_sometimes_they_don_t_play_properly__or_the_Play___call_takes_a_long_time._What_should_I_do__"></span><span id="i_am_playing_the_same_sounds_over_and_over_very_often_and_very_quickly_and_sometimes_they_don_t_play_properly__or_the_play___call_takes_a_long_time._what_should_i_do__"></span><span id="I_AM_PLAYING_THE_SAME_SOUNDS_OVER_AND_OVER_VERY_OFTEN_AND_VERY_QUICKLY_AND_SOMETIMES_THEY_DON_T_PLAY_PROPERLY__OR_THE_PLAY___CALL_TAKES_A_LONG_TIME._WHAT_SHOULD_I_DO__"></span>**Estoy reproduciendo los mismos sonidos una y otra vez con mucha frecuencia y rapidez y, en ocasiones, no se reproducen correctamente o la llamada de reproducción () tarda mucho tiempo. ¿Qué debo hacer?** 
</dt> <dd>

La latencia de inicio (que es diferente de la latencia de streaming mencionada anteriormente) puede ser un problema en el caso de algún hardware (la llamada de reproducción () solo tarda mucho tiempo en determinadas tarjetas de sonido). Si realmente desea reducir esta latencia, en el caso de los sonidos Twitch (disparos, iniciativa, etc.), un truco práctico es mantener algunos búferes siempre en bucle y reproducir silencio. Cuando necesite reproducir un sonido Twitch, elija un búfer libre, vea dónde se encuentra el cursor de escritura y coloque el sonido en el búfer que está más allá del cursor de escritura. Algunas de las funciones de tarjeta de sonido producen un error de QuerySupport para las propiedades diferidas que sé que admiten. ¿Hay alguna solución alternativa? Podría simplemente QuerySupport para las versiones no diferidas de las propiedades y usar la configuración aplazada de todos modos. Los controladores de la tarjeta de sonido más recientes también pueden solucionar este problema.

</dd> <dt>

<span id="How_do_I_encode_WAV_files_into_WMA__"></span><span id="how_do_i_encode_wav_files_into_wma__"></span><span id="HOW_DO_I_ENCODE_WAV_FILES_INTO_WMA__"></span>**¿Cómo codificar archivos WAV en WMA?** 
</dt> <dd>

Consulte la documentación del codificador de Windows Media en: Windows Media Encoder 9 series.

</dd> <dt>

<span id="How_do_I_decode_MP3_files_with_DirectSound__"></span><span id="how_do_i_decode_mp3_files_with_directsound__"></span><span id="HOW_DO_I_DECODE_MP3_FILES_WITH_DIRECTSOUND__"></span>**Cómo descodificar archivos MP3 con DirectSound** 
</dt> <dd>

DirectSound no admite de forma nativa la descodificación MP3. Puede descodificar los archivos por adelantado (mediante un códec ACM de un filtro DirectShow), o bien usar solo DirectShow, que puede realizar la descodificación automáticamente. después, puede copiar los datos de audio PCM resultantes en los búferes de DirectSound.

</dd> </dl>

## <a name="directx-extensions-for-alias-maya"></a>Extensiones de DirectX para el alias Maya

<dl> <dt>

<span id="Why_aren_t_my_NURBS_showing_up__"></span><span id="why_aren_t_my_nurbs_showing_up__"></span><span id="WHY_AREN_T_MY_NURBS_SHOWING_UP__"></span>**¿Por qué no aparece mi NURBS?** 
</dt> <dd>

No se admite NURBS. Puede convertirlas en mallas de polígonos.

</dd> <dt>

<span id="Why_aren_t_my_SUBDs_showing_up_"></span><span id="why_aren_t_my_subds_showing_up_"></span><span id="WHY_AREN_T_MY_SUBDS_SHOWING_UP_"></span>**¿Por qué no aparece mi SUBDs?**
</dt> <dd>

No se admiten SUBDs. Puede convertirlas en mallas de polígonos.

</dd> <dt>

<span id="Why_does_my_animation_in_the_X_file_look_different_than_the_animation_in_the_preview_window__"></span><span id="why_does_my_animation_in_the_x_file_look_different_than_the_animation_in_the_preview_window__"></span><span id="WHY_DOES_MY_ANIMATION_IN_THE_X_FILE_LOOK_DIFFERENT_THAN_THE_ANIMATION_IN_THE_PREVIEW_WINDOW__"></span>**¿Por qué la animación del archivo X es diferente de la animación de la ventana de vista previa?** 
</dt> <dd>

La ventana de vista previa no se anima en el sentido más estricto de la cuestión. No se está reproduciendo la animación, sino que se está sincronizando con el estado más reciente de la escena de Maya. Cuando se exporta la animación, las matrices de cada transformación se descomponen en componentes de escala, rotación (cuaternión) y de traducción (a menudo denominados SRTs). Los SRTs son más deseables que las matrices porque se interpolan bien, proporcionan una forma más compacta de los datos y se pueden comprimir de forma independiente. No todas las matrices se pueden desglosar en SRTs. Si no se pueden descomponer, el SRTs resultante será desconocido, por lo que se pueden detectar pequeños errores en la animación. Las dos características de Maya que suelen causar problemas durante la descomposición son las distorsiones y las rotaciones o escalas fuera del centro. Si se encuentra con este problema, ya que está usando giros o escalas fuera del centro, considere la posibilidad de agregar transformaciones adicionales aumentando el nivel de la jerarquía.

Donde la animación de D3DX es compatible con SRTs, tiene el siguiente aspecto:

``` syntax
[S]x[R]x[T]
```

Las matrices de Maya son mucho más complicadas y requieren una cantidad significativa de procesos adicionales, lo que tiene el siguiente aspecto:

``` syntax
[SpInv]x[S]x[Sh]x[Sp]x[St]x[RpInv]x[Ro]x[R]x[Rp]x[Rt]x[T]
```

</dd> <dt>

<span id="I_skinned_my_mesh_with_RigidSkin_but_the_mesh__or_portion__isn_t_moving._Why__"></span><span id="i_skinned_my_mesh_with_rigidskin_but_the_mesh__or_portion__isn_t_moving._why__"></span><span id="I_SKINNED_MY_MESH_WITH_RIGIDSKIN_BUT_THE_MESH__OR_PORTION__ISN_T_MOVING._WHY__"></span>**Desolla mi malla con RigidSkin, pero la malla (o la parte) no se mueve. ¿Por qué?** 
</dt> <dd>

En este momento no se admite la piel rígida de Maya. Use una máscara suave.

</dd> <dt>

<span id="Where_has_all_of_my_IK_gone_in_the_X-file__"></span><span id="where_has_all_of_my_ik_gone_in_the_x-file__"></span><span id="WHERE_HAS_ALL_OF_MY_IK_GONE_IN_THE_X-FILE__"></span>**¿Dónde se incluye toda la IK en el archivo X?** 
</dt> <dd>

Los archivos X no admiten IK. En su lugar, las soluciones de IK están integradas en los fotogramas almacenados en el archivo X.

</dd> <dt>

<span id="Why_do_none_of_my_materials_colors_show_up_except_DirectXShaders__"></span><span id="why_do_none_of_my_materials_colors_show_up_except_directxshaders__"></span><span id="WHY_DO_NONE_OF_MY_MATERIALS_COLORS_SHOW_UP_EXCEPT_DIRECTXSHADERS__"></span>**¿Por qué no aparece ninguno de los colores de mis materiales excepto DirectXShaders?** 
</dt> <dd>

Las extensiones de DirectX para Maya solo admiten actualmente materiales de DirectXShader para la vista previa y la exportación. En una versión futura, es posible que se admitan otros materiales.

</dd> </dl>

## <a name="xinput-questions"></a>Preguntas sobre XInput

<dl> <dt>

<span id="Can_I_use_DirectInput_to_read_the_triggers__"></span><span id="can_i_use_directinput_to_read_the_triggers__"></span><span id="CAN_I_USE_DIRECTINPUT_TO_READ_THE_TRIGGERS__"></span>**¿Puedo usar DirectInput para leer los desencadenadores?** 
</dt> <dd>

Sí, pero actúan como el mismo eje. Por lo tanto, no puede leer los desencadenadores de forma independiente con DirectInput. Con XInput, los desencadenadores devuelven valores independientes.

Para obtener más información sobre por qué DirectInput interpreta los desencadenadores como un eje, vea [usar el controlador de Xbox 360 con DirectInput](/windows/desktop/xinput/xinput-and-directinput).

</dd> <dt>

<span id="How_many_controllers_does_XInput_support__"></span><span id="how_many_controllers_does_xinput_support__"></span><span id="HOW_MANY_CONTROLLERS_DOES_XINPUT_SUPPORT__"></span>**¿Cuántos controladores admite XInput?** 
</dt> <dd>

XInput admite 4 controladores con conexión a la vez.

</dd> <dt>

<span id="Does_XInput_support_non-common_controllers__"></span><span id="does_xinput_support_non-common_controllers__"></span><span id="DOES_XINPUT_SUPPORT_NON-COMMON_CONTROLLERS__"></span>**¿Admite XInput controladores no comunes?** 
</dt> <dd>

No, no.

</dd> <dt>

<span id="Are_common_controllers_available_through_DirectInput__"></span><span id="are_common_controllers_available_through_directinput__"></span><span id="ARE_COMMON_CONTROLLERS_AVAILABLE_THROUGH_DIRECTINPUT__"></span>**¿Son controladores comunes disponibles a través de DirectInput?** 
</dt> <dd>

Sí, puede tener acceso a los controladores comunes a través de DirectInput.

</dd> <dt>

<span id="How_do_I_get_force_feedback_on_the_common_controllers__"></span><span id="how_do_i_get_force_feedback_on_the_common_controllers__"></span><span id="HOW_DO_I_GET_FORCE_FEEDBACK_ON_THE_COMMON_CONTROLLERS__"></span>**¿Cómo obtener comentarios de fuerza sobre los controladores comunes?** 
</dt> <dd>

Utilice la función [**XInputSetState**](/windows/desktop/api/xinput/nf-xinput-xinputsetstate) .

</dd> <dt>

<span id="Why_does_my_default_audio_device_change__"></span><span id="why_does_my_default_audio_device_change__"></span><span id="WHY_DOES_MY_DEFAULT_AUDIO_DEVICE_CHANGE__"></span>**¿Por qué cambia el dispositivo de audio predeterminado?** 
</dt> <dd>

Al conectar los auriculares, el casco del controlador actúa como un dispositivo de audio USB estándar, por lo que, cuando está conectado, Windows cambia automáticamente para usar este dispositivo de audio USB como valor predeterminado. Dado que es probable que el usuario no quiera que todo el audio pase por los auriculares, deberá ajustarlo manualmente de nuevo a la configuración original.

</dd> <dt>

<span id="How_do_I_control_the_lights_on_the_controller__"></span><span id="how_do_i_control_the_lights_on_the_controller__"></span><span id="HOW_DO_I_CONTROL_THE_LIGHTS_ON_THE_CONTROLLER__"></span>**¿Cómo controlar las luces en el controlador?** 
</dt> <dd>

Las luces del controlador están predeterminadas por el sistema operativo y no se pueden cambiar.

</dd> <dt>

<span id="How_do_I_access_the_Xbox_360_button_in_my_applications__"></span><span id="how_do_i_access_the_xbox_360_button_in_my_applications__"></span><span id="HOW_DO_I_ACCESS_THE_XBOX_360_BUTTON_IN_MY_APPLICATIONS__"></span>**Cómo acceder al botón Xbox 360 en mis aplicaciones** 
</dt> <dd>

Lo sentimos, este botón está reservado para uso futuro.

</dd> <dt>

<span id="Where_do_I_get_drivers__"></span><span id="where_do_i_get_drivers__"></span><span id="WHERE_DO_I_GET_DRIVERS__"></span>**¿Dónde obtengo los controladores?** 
</dt> <dd>

Los controladores estarán disponibles a través de Windows Update.

</dd> <dt>

<span id="How_is_controller_ID_determined__"></span><span id="how_is_controller_id_determined__"></span><span id="HOW_IS_CONTROLLER_ID_DETERMINED__"></span>**¿Cómo se determina el identificador de controlador?** 
</dt> <dd>

En el inicio de XInput, el motor de XInput determina de forma no determinista el identificador y los controladores que están conectados. Si los controladores están conectados mientras se está ejecutando una aplicación XInput, el sistema asignará el número más bajo disponible al nuevo controlador. Si un controlador está desconectado, su número volverá a estar disponible.

</dd> <dt>

<span id="How_do_I_get_the_audio_devices_for_the_controller__"></span><span id="how_do_i_get_the_audio_devices_for_the_controller__"></span><span id="HOW_DO_I_GET_THE_AUDIO_DEVICES_FOR_THE_CONTROLLER__"></span>**Cómo obtener los dispositivos de audio para el controlador?** 
</dt> <dd>

Utilice la función [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/xinput/nf-xinput-xinputgetdsoundaudiodeviceguids) . Vea el ejemplo AudioController para obtener más información.

</dd> <dt>

<span id="What_should_I_do_when_a_controller_is_unplugged__"></span><span id="what_should_i_do_when_a_controller_is_unplugged__"></span><span id="WHAT_SHOULD_I_DO_WHEN_A_CONTROLLER_IS_UNPLUGGED__"></span>**¿Qué debo hacer cuando se desconecta un controlador?** 
</dt> <dd>

Si el controlador estaba en uso por un jugador, debe pausar el juego hasta que el controlador se vuelva a conectar y el reproductor Presione un botón para indicar que está listo para volver a poner en pausa.

</dd> </dl>

 

 