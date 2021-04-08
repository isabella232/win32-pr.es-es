---
title: Usar un editor de métodos de entrada en un juego
description: En este artículo se explica cómo se puede implementar un control básico de edición de IME en una aplicación Microsoft DirectX de pantalla completa.
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1519f07a4e105ae822bd13fd7acd8b29e5ad8a0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104003744"
---
# <a name="using-an-input-method-editor-in-a-game"></a>Usar un editor de métodos de entrada en un juego

> [!Note]  
> En este artículo se describe cómo trabajar con el editor de métodos de entrada (IME) de Windows XP. Se realizaron cambios en el IME para Windows Vista que no están totalmente detallados en este artículo. Para obtener más información acerca de los cambios en el IME para Windows Vista, consulte [editores de métodos de entrada (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) en [Windows Vista: una Ever-Expanding vista de internacionalización](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) en el portal de desarrollo y informática global de Microsoft.

 

Un editor de métodos de entrada (IME) es un programa que permite una entrada de texto sencilla mediante un teclado estándar para idiomas asiáticos orientales, como el chino, el japonés, el coreano y otros idiomas con caracteres complejos. Por ejemplo, con los IME, un usuario puede escribir caracteres complejos en un procesador de textos o un jugador de un juego en línea multijugador masivo puede conversar con amigos en caracteres complejos.

En este artículo se explica cómo se puede implementar un control básico de edición de IME en una aplicación Microsoft DirectX de pantalla completa. Las aplicaciones que aprovechan DXUT obtienen automáticamente la funcionalidad IME. En el caso de las aplicaciones que no usan el marco de trabajo, en este artículo se describe cómo agregar compatibilidad con IME a un control de edición.

Contenido:

-   [Comportamiento predeterminado de IME](#default-ime-behavior)
-   [Uso de IME con DXUT](#using-imes-with-dxut)
-   [Invalidar el comportamiento predeterminado de IME](#overriding-the-default-ime-behavior)
-   [Funciones](#functions)
-   [Mensajes](#ime-messages)
-   [Ejemplos](#examples)
    -   [CHT IME versión 4,2, 4,3 y 4,4](#cht-ime-version-42-43-and-44)
    -   [CHT IME versión 5,0](#cht-ime-version-50)
    -   [Chino tradicional versión 5,1, 5,2 y CHS IME versión 5,3](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [CHS IME versión 4,1](#chs-ime-version-41)
    -   [CHS IME versión 4,2](#chs-ime-version-42)
-   [Mensajes IME](#ime-messages)
    -   [INPUTLANGCHANGE de WM \_](#wm_inputlangchange)
    -   [\_STARTCOMPOSITION de IME de WM \_](/windows)
    -   [\_composición del IME de WM \_](/windows)
    -   [\_ENDCOMPOSITION de IME de WM \_](/windows)
    -   [\_notificación de IME de WM \_](/windows)
-   [Representación](#rendering)
    -   [Indicador de configuración regional de entrada](#input-locale-indicator)
    -   [Ventana composición](#composition-window)
    -   [Lecturas y ventanas candidatas](#reading-and-candidate-windows)
-   [Limitaciones](#limitations)
-   [Información del registro](#registry-information)
-   [Apéndice A: versiones CHT por sistema operativo](#appendix-a-cht-versions-per-operating-system)
-   [Información adicional](#further-information)
-   [GetReadingString](#getreadingstring)
-   [ShowReadingWindow](#showreadingwindow)

## <a name="default-ime-behavior"></a>Comportamiento predeterminado de IME

Los IME asignan entradas de teclado a componentes fonéticos u otros elementos de lenguaje específicos de un idioma seleccionado. En un escenario típico, el usuario escribe claves que representan la Pronunciación de un carácter complejo. Si el IME reconoce la pronunciación como válida, presenta al usuario una lista de candidatos de palabra o frase desde los que el usuario puede seleccionar una opción final. La palabra elegida se envía a la aplicación a través de una serie de mensajes de tipo [**\_ Char**](/windows/desktop/inputdev/wm-char) de Microsoft Windows WM. Dado que el IME funciona en un nivel por debajo de la aplicación mediante la interceptación de la entrada del teclado, la presencia de un IME es transparente para la aplicación. Casi todas las aplicaciones de Windows pueden aprovechar fácilmente los IME sin tener en cuenta su existencia y sin necesidad de codificación especial.

Un IME típico muestra varias ventanas para guiar al usuario a través de la entrada de caracteres, tal y como se muestra en los ejemplos siguientes.

![IME muestra varias ventanas](images/ime-elements.png)

| Tipo de ventana                                       | Descripción                                                                                                                                                                                                                                                                                                                 | Salida de IME                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| A. Ventana de lectura                                 | Contiene pulsaciones de teclas del teclado; Normalmente, los cambios después de cada pulsación de tecla.                                                                                                                                                                                                                                              | cadena de lectura                               |
| B. Ventana composición                             | Contiene la colección de caracteres que el usuario ha compuesto con el IME. El IME dibuja estos caracteres en la parte superior de la aplicación. Cuando el usuario notifica al IME que la cadena de composición es satisfactoria, el IME envía la cadena de composición a la aplicación a través de una serie de mensajes de tipo char de WM \_ . | cadena de composición                           |
| C. Ventana candidata                               | Cuando el usuario ha escrito una pronunciación válida, el IME muestra una lista de caracteres candidatos que coinciden con la pronunciación indicada. A continuación, el usuario selecciona el carácter previsto en esta lista y el IME agrega este carácter a la ventana de composición.                                                    | carácter siguiente de la cadena de composición. |
| D. Indicador de [configuración regional de entrada](/windows/desktop/Intl/nls-terminology) | Muestra el idioma seleccionado por el usuario para la entrada de teclado. Este indicador está incrustado en la barra de tareas de Windows. Para seleccionar el idioma de entrada, abra el panel de control configuración regional y de idioma y, a continuación, haga clic en detalles en la pestaña idiomas.                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a>Uso de IME con DXUT

En DXUT, la clase CDXUTIMEEditBox implementa la funcionalidad del IME. Esta clase se deriva de la clase CDXUTEditBox, el control básico de edición proporcionado por el marco de trabajo. CDXUTIMEEditBox extiende ese control de edición para admitir los IME mediante la invalidación de los métodos CDXUTIMEEditBox. Las clases están diseñadas de esta manera para ayudar a los desarrolladores a saber lo que necesitan tomar de la plataforma para implementar la compatibilidad con el IME en sus propios controles de edición. En el resto de este tema se explica cómo el marco de trabajo y CDXUTIMEEditBox en concreto reemplazan a un control de edición básico para implementar la funcionalidad de IME.

La mayoría de las variables específicas del IME en CDXUTIMEEditBox se declaran como estáticas, ya que muchos de los búferes y Estados IME son específicos del proceso. Por ejemplo, un proceso solo tiene un búfer para la cadena de composición. Aunque el proceso tenga diez controles de edición, todos ellos compartirán el mismo búfer de cadena de composición. Por lo tanto, el búfer de cadena de composición para CDXUTIMEEditBox es estático, lo que impide que la aplicación ocupe espacio de memoria innecesario.

CDXUTIMEEditBox se implementa en el siguiente código de DXUT:

(Raíz del SDK) \\ Ejemplos \\ C++ \\ común \\ DXUTgui. cpp

## <a name="overriding-the-default-ime-behavior"></a>Invalidar el comportamiento predeterminado de IME

Normalmente, un IME usa los procedimientos estándar de Windows para crear una ventana (consulte [uso de Windows](/windows/desktop/winmsg/using-windows)). En circunstancias normales, esto produce resultados satisfactorios. Sin embargo, cuando la aplicación presenta el modo de pantalla completa, como es habitual para los juegos, las ventanas estándar ya no funcionan y es posible que no se muestren en la parte superior de la aplicación. Para solucionar este problema, la aplicación debe dibujar las ventanas del IME en lugar de basarse en Windows para realizar esta tarea.

Cuando el comportamiento de creación de la ventana del IME predeterminado no proporciona lo que una aplicación requiere, la aplicación puede invalidar el control de ventanas del IME. Una aplicación puede lograr esto mediante el procesamiento de mensajes relacionados con el IME y la llamada a la API del [Administrador de métodos de entrada](/windows/desktop/Intl/input-method-manager) (IMM).

Cuando un usuario interactúa con un IME para escribir caracteres complejos, el IMM envía mensajes a la aplicación para notificarle eventos importantes, como iniciar una composición o Mostrar la ventana candidata. Normalmente, una aplicación omite estos mensajes y los pasa al controlador de mensajes predeterminado, lo que hace que el IME los controle. Cuando la aplicación, en lugar del controlador predeterminado, controla los mensajes, controla exactamente lo que sucede en cada uno de los eventos del IME. A menudo, el controlador de mensajes recupera el contenido de las distintas ventanas del IME mediante una llamada a la API de IMM. Una vez que la aplicación tenga esta información, puede dibujar correctamente las propias ventanas del IME cuando sea necesario representarlas en la pantalla.

## <a name="functions"></a>Functions

Un IME debe obtener la cadena de lectura, ocultar la ventana de lectura y obtener la orientación de la ventana de lectura. En esta tabla se muestran las funcionalidades por versión de IME:



|                    | Obteniendo cadena de lectura                                                | Ocultar la ventana de lectura                       | Orientación de la ventana de lectura                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| Antes de la versión 6,0 | A. Leer datos privados del IME de acceso a la ventana directamente. Vea "4 Structure" | Interceptar mensajes privados del IME. Vea "3 mensajes" | Examine la información del registro. Consulte "5 información del registro" |
| Después de la versión 6,0  | [GetReadingString](#getreadingstring)                                 | [ShowReadingWindow](#showreadingwindow)     | [GetReadingString](#getreadingstring)                      |



 

## <a name="messages"></a>error de Hadoop

No es necesario procesar los siguientes mensajes para el IME más reciente que implementa [ShowReadingWindow](#showreadingwindow)().

Los mensajes siguientes se capturan mediante el controlador de mensajes de la aplicación (es decir, no se pasan a DefWindowProc) para impedir que se muestre la ventana de lectura.

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos se muestra cómo obtener información de cadena de lectura de IME anterior que no tiene GetReadingString (). El código genera las siguientes salidas:



|              |                                                                                       |
|--------------|---------------------------------------------------------------------------------------|
| DWORD dwlen  | Longitud de la cadena de lectura                                                          |
| DWORD dwerr  | Índice de carácter de error                                                                   |
| LPWSTR wstr  | Puntero a la cadena de lectura                                                         |
| BOOL Unicode | Si es true, la cadena de lectura está en formato Unicode. En caso contrario, tiene el formato multibyte. |



 

### <a name="cht-ime-version-42-43-and-44"></a>CHT IME versión 4,2, 4,3 y 4,4

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a>CHT IME versión 5,0

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 3*4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4 + 4*2 );
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 + 1*4);
wstr = (WCHAR *)(p + 1*4 + (16*2+2*4) + 5*4);
unicode = FALSE;
```

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a>Chino tradicional versión 5,1, 5,2 y CHS IME versión 5,3

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4); 
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2 + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = TRUE;
```

### <a name="chs-ime-version-41"></a>CHS IME versión 4,1

``` syntax
// GetImeId(1) returns VS_FIXEDFILEINFO:: dwProductVersionLS of IME file
int offset = ( GetImeId( 1 ) >= 0x00000002 ) ? 8 : 7;
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + offset * 4);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 16*2*4);
dwerr = *(DWORD *)(p + 8*4 + 16*2*4);
dwerr = min(dwerr, dwlen);
wstr = (WCHAR *)(p + 6*4 + 16*2*1);
unicode = TRUE;
```

### <a name="chs-ime-version-42"></a>CHS IME versión 4,2

``` syntax
int nTcharSize = IsNT() ? sizeof(WCHAR) : sizeof(char);
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 1*4 + 1*4 + 6*4);
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = IsNT() ? TRUE : FALSE;
```

## <a name="ime-messages"></a>Mensajes IME

Una aplicación de pantalla completa debe administrar correctamente los siguientes mensajes relacionados con el IME:

### <a name="wm_inputlangchange"></a>INPUTLANGCHANGE de WM \_

El IMM envía un \_ mensaje de WM INPUTLANGCHANGE a la ventana activa de una aplicación después de que el usuario haya cambiado la configuración regional de entrada con una combinación de teclas (normalmente Alt + Mayús) o con el indicador de configuración regional de entrada en la barra de tareas o en la barra de idioma. La barra de idioma es un control en pantalla con el que el usuario puede configurar un servicio de texto. (Vea [Cómo mostrar la barra de idioma](/windows/desktop/TSF/how-to-set-up-tsf)). En la captura de pantalla siguiente se muestra una lista de selección de idioma que se muestra cuando el usuario hace clic en el indicador de configuración regional.

![lista de selección de idioma que se muestra cuando el usuario hace clic en el indicador de configuración regional](images/ime-langselection.png)

Cuando el IMM envía un mensaje de WM \_ INPUTLANGCHANGE, CDXUTIMEEditBox debe realizar varias tareas importantes:

1.  Se llama al método GetKeyboardLayout para devolver el identificador de configuración regional (ID.) de entrada para el subproceso de la aplicación. La clase CDXUTIMEEditBox guarda este identificador en su variable miembro estática s \_ hklCurrent para su uso posterior. Es importante que la aplicación Conozca la configuración regional de entrada actual, ya que el IME para cada idioma tiene su propio comportamiento distinto. El desarrollador puede tener que proporcionar un código diferente para las diferentes configuraciones regionales de entrada.
2.  CDXUTIMEEditBox Inicializa una cadena para mostrarla en el indicador de idioma del cuadro de edición. Este indicador puede mostrar el idioma de entrada activo cuando la aplicación se ejecuta en modo de pantalla completa y no está visible la barra de tareas ni la barra de idioma.
3.  Se llama al método ImmGetConversionStatus para indicar si la configuración regional de entrada está en modo de conversión nativo o no nativo. El modo de conversión nativo permite al usuario escribir texto en el idioma elegido. El modo de conversión no nativo hace que el teclado actúe como un teclado estándar en inglés. Es importante proporcionar una indicación visual al usuario sobre el tipo de modo de conversión en el que se encuentra el IME, de modo que el usuario pueda saber fácilmente qué caracteres se deben esperar al golpear una tecla. CDXUTIMEEditBox proporciona esta indicación visual con un color de indicador de lenguaje. Cuando la configuración regional de entrada usa un IME con el modo de conversión nativo, la clase CDXUTIMEEditBox dibuja el texto del indicador con el color definido por el \_ parámetro m IndicatorImeColor. Cuando el IME está en modo de conversión no nativo, o no se usa ningún IME, la clase dibuja el texto del indicador con el color definido por el \_ parámetro m IndicatorEngColor.
4.  CDXUTIMEEditBox comprueba la configuración regional de entrada y establece el valor de la variable miembro estática s \_ bInsertOnType en true para coreano y false para todos los demás idiomas. Esta marca es necesaria debido a los distintos comportamientos de los IME de Coreano y de todos los demás IME. Al escribir caracteres en idiomas distintos del coreano, el texto escrito por el usuario se muestra en la ventana de composición y el usuario puede cambiar libremente el contenido de la cadena de composición. El usuario presiona la tecla entrar cuando está satisfecho con la cadena de composición y la cadena de composición se envía a la aplicación como una serie de mensajes de tipo char de WM \_ . Sin embargo, en los IME de Coreano, cuando un usuario presiona una tecla para escribir texto, se envía inmediatamente un carácter a la aplicación. Cuando el usuario presiona más teclas para modificar el carácter inicial, el carácter del cuadro de edición cambia para reflejar entradas adicionales del usuario. Esencialmente, el usuario está creando caracteres en el cuadro de edición. Estos dos comportamientos son lo suficientemente diferentes como para que CDXUTIMEEditBox deba codificar cada uno de ellos de forma específica.
5.  Se llama al método miembro estático SetupImeApi para recuperar direcciones de dos funciones del módulo IME: GetReadingString y ShowReadingWindow. Si estas funciones existen, se llama a ShowReadingWindow para ocultar la ventana de lectura predeterminada para este IME. Dado que la aplicación representa la propia ventana de lectura, notifica al IME que deshabilite el dibujo de la ventana de lectura predeterminada para que no interfiera con la representación a pantalla completa.

El IMM envía un \_ mensaje de de WM IME en el que \_ se activa una ventana de la aplicación. El parámetro lParam de este mensaje contiene una marca que indica al IME Qué ventanas se deben dibujar y cuáles no. Dado que la aplicación controla todo el dibujo, no es necesario que el IME dibuje ninguna de las ventanas del IME. Por lo tanto, el controlador de mensajes de la aplicación simplemente establece lParam en 0 y devuelve.

Para que las aplicaciones admitan el IME, se necesita un procesamiento especial para el mensaje relacionado con el IME de WM \_ IME \_ . Puesto que Windows normalmente envía este mensaje a la aplicación antes de llamar al método PanoramaInitialize (), panorama no tiene la oportunidad de procesar la interfaz de usuario para mostrar las ventanas de lista de candidatos.

El siguiente fragmento de código especifica a las aplicaciones de Windows que no muestren ninguna interfaz de usuario asociada a la ventana de lista de candidatos, lo que permite que panorama controle específicamente esta interfaz de usuario.

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a>\_STARTCOMPOSITION de IME de WM \_

El IMM envía un \_ \_ mensaje STARTCOMPOSITION del IME de WM a la aplicación cuando la composición del IME está a punto de comenzar como resultado de las pulsaciones de tecla del usuario. Si el IME usa la ventana de composición, muestra la cadena de composición actual en una ventana de composición. CDXUTIMEEditBox controla este mensaje mediante la realización de dos tareas:

1.  CDXUTIMEEditBox borra el búfer de la cadena de composición y el búfer de atributo. Estos búferes son miembros estáticos de CDXUTIMEEditBox.
2.  CDXUTIMEEditBox establece la \_ variable de miembro estático s bHideCaret en true. Este miembro, definido en la clase base CDXUTEditBox, controla si se debe dibujar el cursor en el cuadro de edición cuando se represente el cuadro de edición. La ventana composición funciona de forma similar a un cuadro de edición con texto y cursor. Para evitar confusiones cuando la ventana de composición está visible, el cuadro de edición oculta su cursor para que solo un cursor esté visible a la vez.

### <a name="wm_ime_composition"></a>\_composición del IME de WM \_

El IMM envía un \_ mensaje de \_ composición del IME de WM a la aplicación cuando el usuario escribe una pulsación de tecla para cambiar la cadena de composición. El valor de lParam indica qué tipo de información puede recuperar la aplicación del administrador de métodos de entrada (IMM). La aplicación debe recuperar la información disponible mediante una llamada a [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) y, a continuación, debe guardar la información en su búfer privado para que pueda representar los elementos IME más adelante.

CDXUTIMEEditBox comprueba y recupera los datos de la cadena de composición siguientes:



| [**WM \_ Valor \_**](/windows/desktop/Intl/wm-ime-composition) de marca lParam de composición de IME | data                           | Descripción                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GC \_ COMPATTR                                                         | Atributo de composición          | Este atributo contiene información como el estado de cada carácter de la cadena de composición (por ejemplo, convertido o no convertido). Esta información es necesaria porque CDXUTIMEEditBox colorea los caracteres de cadena de composición de manera diferente en función de sus atributos.                                                                                   |
| GC \_ COMPCLAUSE                                                       | Información de la cláusula de composición | Esta información de la cláusula se utiliza cuando el IME japonés está activo. Cuando se convierte una cadena de composición en japonés, los caracteres se pueden agrupar como una cláusula que se convierte en una sola entidad. Cuando el usuario mueve el cursor, CDXUTIMEEditBox usa esta información para resaltar la cláusula completa, en lugar de simplemente un carácter único dentro de la cláusula. |
| GC \_ COMPSTR                                                          | Cadena de composición             | Esta cadena es la cadena actualizada que está compuesta por el usuario. Esta es también la cadena mostrada en la ventana de composición.                                                                                                                                                                                                                                        |
| GC \_ CURSORPOS                                                        | Posición del cursor de composición    | La ventana composición implementa un cursor, similar al cursor en un cuadro de edición. La aplicación puede recuperar la posición del cursor al procesar el \_ \_ mensaje de composición del IME de WM para dibujar el cursor correctamente.                                                                                                                                            |
| RESULTSTR de GC \_                                                        | Cadena de resultado                  | La cadena de resultado está disponible cuando el usuario está a punto de completar el proceso de composición. Esta cadena debe recuperarse y los caracteres deben enviarse al cuadro de edición.                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a>\_ENDCOMPOSITION de IME de WM \_

El IMM envía un \_ \_ mensaje ENDCOMPOSITION del IME de WM a la aplicación cuando finaliza la operación de composición del IME. Esto puede ocurrir cuando el usuario presiona la tecla entrar para aprobar la cadena de composición o la tecla ESC para cancelar la composición. CDXUTIMEEditBox controla este mensaje estableciendo el búfer de cadena de composición en blanco. A continuación, establece s \_ bHideCaret en false porque la ventana de composición está cerrada y el cursor en el cuadro de edición debe estar visible de nuevo.

El controlador de mensajes CDXUTIMEEditBox también establece s \_ bShowReadingWindow en false. Esta marca controla si la clase dibuja la ventana de lectura cuando el cuadro de edición se representa a sí mismo, por lo que debe establecerse en FALSE cuando finaliza una composición.

### <a name="wm_ime_notify"></a>\_notificación de IME de WM \_

El IMM envía un \_ mensaje de notificación del IME de WM \_ a la aplicación cada vez que cambia una ventana del IME. Una aplicación que controla el dibujo de las ventanas del IME debe procesar este mensaje para que sea consciente de cualquier actualización del contenido de la ventana. WParam indica el comando o el cambio que se está llevando a cabo. CDXUTIMEEditBox controla los siguientes comandos:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Comando IME</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></td>
<td>Este atributo contiene información como el estado de cada carácter de la cadena de composición (por ejemplo, convertido o no convertido). Esta información es necesaria porque CDXUTIMEEditBox colorea los caracteres de cadena de composición de manera diferente en función de sus atributos.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  /  <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></td>
<td>Se envía a la aplicación cuando la ventana candidata está a punto de abrirse o actualizarse, respectivamente. La ventana candidata se abre cuando un usuario desea cambiar la opción de texto convertido. La ventana se actualiza cuando un usuario mueve el indicador de selección o cambia la página. CDXUTIMEEditBox usa un controlador de mensajes para ambos comandos, ya que las tareas necesarias son exactamente iguales:<br/>
<ol>
<li>CDXUTIMEEditBox establece el miembro bShowWindow de la estructura de la lista de candidatos s_CandList en TRUE para indicar que la ventana candidata debe dibujarse durante la representación del marco.</li>
<li>CDXUTIMEEditBox recupera la lista de candidatos llamando a <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, primero para obtener el tamaño de búfer necesario y, después, de nuevo para obtener los datos reales.</li>
<li>La estructura de la lista de candidatos privados s_CandList se inicializa con los datos candidatos recuperados.</li>
<li>Las cadenas candidatas se almacenan como una matriz de cadenas.</li>
<li>Se guarda el índice de la entrada seleccionada, así como el índice de la página.</li>
<li>CDXUTIMEEditBox comprueba si el estilo de ventana candidata es vertical u horizontal. Si el estilo de ventana es horizontal, se debe inicializar un búfer de cadena adicional, el miembro HoriCand de s_CandList, con todas las cadenas candidatas, con caracteres de espacio insertados entre todas las cadenas adyacentes. Al representar una ventana de candidato vertical, las cadenas candidatas individuales se dibujan de una en una, con las coordenadas y incrementadas para cada cadena. Sin embargo, esta cadena HoriCand se debe usar al representar una ventana candidata horizontal, porque el carácter de espacio es la mejor manera de separar dos cadenas adyacentes en la misma línea.</li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></td>
<td>Se envía a la aplicación cuando una ventana candidata está a punto de cerrarse. Esto sucede cuando un usuario ha realizado una selección de la lista de candidatos. CDXUTIMEEditBox controla este comando estableciendo la marca visible de la ventana candidata en FALSE y, a continuación, borrando el búfer de la cadena candidata.</td>
</tr>
<tr class="even">
<td>IMN_PRIVATE</td>
<td>Se envía a la aplicación cuando el IME ha actualizado su cadena de lectura como resultado de que el usuario escriba o quite caracteres. La aplicación debe recuperar la cadena de lectura y guardarla para su representación. CDXUTIMEEditBox tiene dos métodos para recuperar la cadena de lectura, en función de cómo se admiten las cadenas de lectura en el IME: <br/>
<ul>
<li>Si el IME admite la función GetReadingString, se llama a GetReadingString para recuperar la cadena de lectura.</li>
<li>Si el IME no implementa GetReadingString, CDXUTIMEEditBox recupera la cadena de lectura del contenido del contexto de entrada.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="rendering"></a>Representación

La representación de los elementos y ventanas del IME es sencilla. CDXUTIMEEditBox permite que la clase base se represente primero porque las ventanas de IME deben aparecer encima del control de edición. Una vez representado el cuadro de edición base, CDXUTIMEEditBox comprueba la marca de visibilidad de cada ventana del IME (indicador, composición, candidato y ventana de lectura) y dibuja la ventana si debe estar visible. Consulte comportamiento predeterminado del IME para obtener descripciones de los distintos tipos de ventana del IME.

### <a name="input-locale-indicator"></a>Indicador de configuración regional de entrada

El indicador de configuración regional de entrada se representa antes que cualquier otra ventana de IME porque es un elemento que siempre se muestra. Por lo tanto, debe aparecer debajo de otras ventanas IME. CDXUTIMEEditBox representa el indicador llamando al método RenderIndicator, en el que el color de la fuente del indicador se determina examinando la \_ variable estática de s, que refleja el modo de conversión del IME actual. Cuando el IME está habilitado y la conversión nativa está activa, el método usa m \_ IndicatorImeColor como el color del indicador. Si el IME está deshabilitado o está en modo de conversión no nativo, \_ se usa m IndicatorImeColor para dibujar el texto del indicador. De forma predeterminada, la ventana de indicador en sí se dibuja a la derecha del cuadro de edición. Las aplicaciones pueden cambiar este comportamiento invalidando el método RenderIndicator.

En la siguiente ilustración se muestran las distintas apariencias de un indicador de configuración regional de entrada para inglés, Japonés en modo de conversión alfanumérica y japonés en modo de conversión nativo:

![diferentes aspectos de un indicador de configuración regional de entrada para inglés y japonés](images/ime-indicator.png)

### <a name="composition-window"></a>Ventana composición

El dibujo de la ventana de composición se controla en el método RenderComposition de CDXUTIMEEditBox. La ventana de composición flota sobre el cuadro de edición. Debe dibujarse en la posición del cursor del control de edición subyacente. CDXUTIMEEditBox controla la representación de la siguiente manera:

1.  Toda la cadena de composición se dibuja utilizando los colores de la cadena de composición predeterminados.
2.  Los caracteres con ciertos atributos especiales deben dibujarse en colores diferentes, por lo que CDXUTIMEEditBox revisa los caracteres de la cadena de composición e inspecciona el atributo de cadena. Si el atributo llama a para distintos colores, el carácter se dibuja de nuevo con los colores adecuados.
3.  Se dibuja el cursor de la ventana de composición para completar la representación.

El cursor debe parpadear en los IME de Coreano, pero no en otros IME. RenderComposition determina si el cursor debe ser visible en función de los valores de temporizador cuando se usa el IME Coreano.

### <a name="reading-and-candidate-windows"></a>Lecturas y ventanas candidatas

Las ventanas de lectura y de candidatos se representan mediante el mismo método CDXUTIMEEditBox, RenderCandidateReadingWindow. Ambas ventanas contienen una matriz de cadenas para el diseño vertical o una sola cadena en el caso del diseño horizontal. La mayor parte del código de RenderCandidateReadingWindow se usa para colocar la ventana de forma que ninguna parte de la ventana esté fuera de la ventana de la aplicación y se recorte.

## <a name="limitations"></a>Limitaciones

A veces, los IME contienen características avanzadas para mejorar la facilidad de entrada de texto. Algunas de las características que se encuentran en los IME más recientes se muestran en las siguientes figuras. Estas características avanzadas no están presentes en DXUT. La implementación de la compatibilidad con estas características avanzadas puede ser complicada, ya que no hay ninguna interfaz definida para obtener la información necesaria de los IME.

IME de chino tradicional avanzado con lista de candidatos ampliada:

![IME de chino tradicional avanzado con lista de candidatos ampliada](images/ime-advanced1.png)

IME japonés avanzado con algunas entradas candidatas que contienen texto adicional para describir su significado:

![IME japonés avanzado con algunas entradas candidatas que contienen texto adicional para describir su significado](images/ime-advanced2.png)

IME Coreano avanzado que incluye un sistema de reconocimiento de escritura a mano:

![IME Coreano avanzado que incluye un sistema de reconocimiento de escritura a mano](images/ime-advanced3.png)

## <a name="registry-information"></a>Información del registro

La siguiente información del registro se comprueba para determinar la orientación de la ventana de lectura, cuando el IME actual es anterior CHT nuevo Phonetic que no implementa GetReadingString ().



| Clave                                                           | Value            |
|---------------------------------------------------------------|------------------|
| HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ IME \_ Name | asignación de teclado |



 

Donde: \_ el nombre del IME es MSTCIPH si la versión del archivo IME es 5,1 o posterior; en caso contrario, el nombre del IME \_ es TINTLGNT.

La orientación de la ventana de lectura es horizontal si:

-   El IME tiene la versión 5,0 y el valor de asignación de teclado es 0x22 o 0x23
-   El IME es la versión 5,1 o la versión 5,2 y el valor de asignación de teclado es 0x22, 0x23 o 0x24.

Si no se cumple ninguna de las condiciones, la ventana de lectura es vertical.

## <a name="appendix-a-cht-versions-per-operating-system"></a>Apéndice A: versiones CHT por sistema operativo



| Sistema operativo           | Versión de IME de CHT |
|----------------------------|-----------------|
| Windows 98                 | 4,2             |
| Windows 2000               | 4.3             |
| unknown                    | 4.4.             |
| Windows ME                 | 5.0             |
| Office XP                  | 5,1             |
| Windows XP                 | 5.2             |
| Downloadble web independiente | 6.0             |



 

## <a name="further-information"></a>Información adicional

Para obtener más información, vea lo siguiente:

-   [Instalación y uso de editores de métodos de entrada](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [Presentación de texto internacional](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [El consorcio Unicode](https://www.unicode.org/)
-   Desarrollo de software internacional. Dr. International. 2a ed. Redmond, WA: Microsoft Press, 2003.

## <a name="getreadingstring"></a>GetReadingString

Obtiene la información de la cadena de lectura.

**Parámetros**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[en el \] contexto de entrada.

</dd> <dt>

<span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*
</dt> <dd>

\[en la \] longitud de lpwReadingBuf, en WCHAR. Si es cero, significa que la longitud del búfer de lectura de consulta es.

</dd> <dt>

<span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf* 
</dt> <dd>

\[out \] devuelve una cadena de lectura (no un extremo cero).

</dd> <dt>

<span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex* 
</dt> <dd>

\[out \] devuelve el índice del carácter de error en la cadena de lectura si existe.

</dd> <dt>

<span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical* 
</dt> <dd>

\[\]si es true, la lectura de la interfaz de usuario es vertical. De lo contrario, puMaxReadingLen horizontal.

</dd> <dt>

<span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen* 
</dt> <dd>

\[\]la longitud de la interfaz de usuario de lectura. La longitud de lectura máxima no es fija. no depende solo de la distribución del teclado, sino también en el modo de entrada (por ejemplo, código interno, entrada suplente).

</dd> </dl>

**Valores devueltos**

La longitud de la cadena de lectura.

**Comentarios:**

Si el valor devuelto es mayor que el valor de uReadingBufLen, todos los parámetros de salida no están definidos.

Esta función se implementa en la versión CHT de IME 6,0 o posterior, y la puede adquirir GetProcAddress en un identificador de módulo IME; ImmGetIMEFileName y LoadLibrary pueden adquirir el identificador del módulo IME.

**Requisitos**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Encabezado**
</dt> <dd>

Declarado en IMM. h.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Biblioteca de importación**
</dt> <dd>

Use IMM. lib.

</dd> </dl>

## <a name="showreadingwindow"></a>ShowReadingWindow

Mostrar u ocultar la ventana de lectura.

**Parámetros**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[en el \] contexto de entrada.

</dd> <dt>

<span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow* 
</dt> <dd>

\[en \] establecido en true para mostrar la ventana de lectura (o false para ocultarla).

</dd> </dl>

**Valores devueltos**

**Comentarios:**

Devuelve TRUE si es correcto o FALSE si no lo está.

**Requisitos**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Encabezado**
</dt> <dd>

Declarado en IMM. h.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Biblioteca de importación**
</dt> <dd>

Use IMM. lib.

</dd> </dl>