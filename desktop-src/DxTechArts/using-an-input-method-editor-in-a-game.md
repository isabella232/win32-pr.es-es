---
title: Usar un editor de métodos de entrada en un juego
description: En este artículo se explica cómo implementar un control de edición de IME básico en una aplicación de Microsoft DirectX de pantalla completa.
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119c5933aae14e2d3e45085dafa241a4dcb11e1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118680"
---
# <a name="using-an-input-method-editor-in-a-game"></a>Usar un editor de métodos de entrada en un juego

> [!Note]  
> En este artículo se detalla cómo trabajar con el Editor de métodos de entrada (IME) de Windows XP. Se realizaron cambios en el IME para Windows Vista que no se detallan completamente en este artículo. Para obtener más información sobre los cambios en el IME para Windows Vista, vea Editores de métodos de entrada [(IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) en [Windows Vista:](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) una vista Ever-Expanding de internacionalización en el Portal de desarrollo e informática global de Microsoft.

 

Un editor de métodos de entrada (IME) es un programa que permite una entrada de texto sencilla mediante un teclado estándar para idiomas de Asia Oriental, como chino, japonés, coreano y otros idiomas con caracteres complejos. Por ejemplo, con imes, un usuario puede escribir caracteres complejos en un procesador de palabras o un jugador de un juego en línea multijugador masivo puede chatear con amigos en caracteres complejos.

En este artículo se explica cómo implementar un control de edición de IME básico en una aplicación de Microsoft DirectX de pantalla completa. Las aplicaciones que aprovechan DXUT obtienen automáticamente la funcionalidad IME. En el caso de las aplicaciones que no usan el marco de trabajo, en este artículo se describe cómo agregar compatibilidad con IME a un control de edición.

Contenido:

-   [Comportamiento predeterminado de IME](#default-ime-behavior)
-   [Uso de IME con DXUT](#using-imes-with-dxut)
-   [Invalidar el comportamiento predeterminado de IME](#overriding-the-default-ime-behavior)
-   [Funciones](#functions)
-   [Mensajes](#ime-messages)
-   [Ejemplos](#examples)
    -   [CHT IME versión 4.2, 4.3 y 4.4](#cht-ime-version-42-43-and-44)
    -   [CHT IME versión 5.0](#cht-ime-version-50)
    -   [CHT IME versión 5.1, 5.2 y CHS IME versión 5.3](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [CHS IME versión 4.1](#chs-ime-version-41)
    -   [CHS IME versión 4.2](#chs-ime-version-42)
-   [Mensajes IME](#ime-messages)
    -   [WM \_ INPUTLANGCHANGE](#wm_inputlangchange)
    -   [WM \_ IME \_ STARTCOMPOSITION](/windows)
    -   [WM \_ IME \_ COMPOSITION](/windows)
    -   [WM \_ IME \_ ENDCOMPOSITION](/windows)
    -   [WM \_ IME \_ NOTIFY](/windows)
-   [Representación](#rendering)
    -   [Indicador de configuración regional de entrada](#input-locale-indicator)
    -   [Ventana Composición](#composition-window)
    -   [Ventanas de lectura y candidatas](#reading-and-candidate-windows)
-   [Limitaciones](#limitations)
-   [Información del Registro](#registry-information)
-   [Apéndice A: Versiones de CHT por sistema operativo](#appendix-a-cht-versions-per-operating-system)
-   [Información adicional](#further-information)
-   [GetReadingString](#getreadingstring)
-   [ShowReadingWindow](#showreadingwindow)

## <a name="default-ime-behavior"></a>Comportamiento predeterminado de IME

Los IME asignan la entrada de teclado a componentes fonéticos u otros elementos de lenguaje específicos de un idioma seleccionado. En un escenario típico, el usuario tipos claves que representan la pronunciación de un carácter complejo. Si el IME reconoce la pronunciación como válida, presenta al usuario una lista de candidatos de palabras o frases entre las que el usuario puede seleccionar una opción final. A continuación, la palabra elegida se envía a la aplicación a través de una serie de mensajes [**WM \_ CHAR de**](/windows/desktop/inputdev/wm-char) Microsoft Windows. Dado que el IME funciona en un nivel por debajo de la aplicación mediante la interceptación de la entrada de teclado, la presencia de un IME es transparente para la aplicación. Casi todas las aplicaciones de Windows pueden aprovechar fácilmente las ventajas de los EME sin tener en cuenta su existencia y sin necesidad de codificación especial.

Un IME típico muestra varias ventanas para guiar al usuario a través de la entrada de caracteres, como se muestra en los ejemplos siguientes.

![ime muestra varias ventanas](images/ime-elements.png)

| Tipo de ventana                                       | Descripción                                                                                                                                                                                                                                                                                                                 | Salida de IME                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| A. Ventana de lectura                                 | Contiene pulsaciones de tecla del teclado; normalmente cambia después de cada pulsación de tecla.                                                                                                                                                                                                                                              | cadena de lectura                               |
| B. Ventana Composición                             | Contiene la colección de caracteres que el usuario ha compuesto con el IME. El IME dibuja estos caracteres en la parte superior de la aplicación. Cuando el usuario notifica al IME que la cadena de composición es satisfactoria, el IME envía la cadena de composición a la aplicación a través de una serie de mensajes \_ WM CHAR. | cadena de composición                           |
| C. Ventana Candidata                               | Cuando el usuario ha escrito una pronunciación válida, el IME muestra una lista de caracteres candidatos que coinciden con la pronunciación dada. A continuación, el usuario selecciona el carácter deseado de esta lista y el IME agrega este carácter a la pantalla Ventana de composición.                                                    | el siguiente carácter de la cadena de composición |
| D. [Indicador de configuración regional de](/windows/desktop/Intl/nls-terminology) entrada | Muestra el idioma que el usuario ha seleccionado para la entrada de teclado. Este indicador se inserta en la barra de tareas de Windows. Para seleccionar el idioma de entrada, abra el cuadro de diálogo Opciones regionales Panel de control idioma y, a continuación, haga clic en Detalles en la pestaña Idiomas.                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a>Uso de IME con DXUT

En DXUT, la clase CD DXTIMEEditBox implementa la funcionalidad IME. Esta clase se deriva de la clase CDXUTEditBox, el control de edición básico proporcionado por el marco. CDMUTTIMEEditBox amplía ese control de edición para admitir los IME mediante la invalidación de los métodos CDMUTTIMEEditBox. Las clases están diseñadas de esta manera para ayudar a los desarrolladores a aprender lo que necesitan tomar del marco para implementar la compatibilidad con IME en sus propios controles de edición. En el resto de este tema se explica cómo el marco de trabajo, y CDTEXTTIMEEditBox en particular, invalida un control de edición básico para implementar la funcionalidad de IME.

La mayoría de las variables específicas de IME de CDEDITTIMEEditBox se declaran como estáticas, ya que muchos búferes y estados de IME son específicos del proceso. Por ejemplo, un proceso tiene solo un búfer para la cadena de composición. Incluso si el proceso tiene diez controles de edición, todos compartirán el mismo búfer de cadena de composición. Por lo tanto, el búfer de cadenas de composición para CD COMPOSTIMEEditBox es estático, lo que impide que la aplicación tome espacio de memoria innecesario.

CD DXTIMEEditBox se implementa en el siguiente código DXUT:

(raíz del SDK) \\ Ejemplos \\ de D \\ \\ MALWARETgui.cpp comunes de C++

## <a name="overriding-the-default-ime-behavior"></a>Invalidar el comportamiento predeterminado de IME

Normalmente, un IME usa procedimientos estándar de Windows para crear una ventana (consulte [Uso de Windows).](/windows/desktop/winmsg/using-windows) En circunstancias normales, esto produce resultados satisfactorios. Sin embargo, cuando la aplicación se presenta en modo de pantalla completa, como es habitual para los juegos, las ventanas estándar ya no funcionan y es posible que no se muestren encima de la aplicación. Para solucionar este problema, la aplicación debe dibujar las propias ventanas de IME en lugar de depender de Windows para realizar esta tarea.

Cuando el comportamiento predeterminado de creación de ventanas de IME no proporciona lo que requiere una aplicación, la aplicación puede invalidar el control de ventanas de IME. Una aplicación puede lograrlo procesando mensajes relacionados con IME y llamando a [la](/windows/desktop/Intl/input-method-manager) API del Administrador de métodos de entrada (IMM).

Cuando un usuario interactúa con un IME para introducir caracteres complejos, IMM envía mensajes a la aplicación para notificarle eventos importantes, como iniciar una composición o mostrar la ventana candidata. Normalmente, una aplicación omite estos mensajes y los pasa al controlador de mensajes predeterminado, lo que hace que el IME los controle. Cuando la aplicación, en lugar del controlador predeterminado, controla los mensajes, controla exactamente lo que sucede en cada uno de los eventos de IME. A menudo, el controlador de mensajes recupera el contenido de las distintas ventanas de IME mediante una llamada a la API de IMM. Una vez que la aplicación tiene esta información, puede dibujar correctamente las propias ventanas de IME cuando necesite representarse en la pantalla.

## <a name="functions"></a>Functions

Un IME debe obtener la cadena de lectura, ocultar la ventana de lectura y obtener la orientación de la ventana de lectura. En esta tabla se muestran las funcionalidades por versión de IME:



|                    | Obtención de la cadena de lectura                                                | Ocultar la ventana de lectura                       | Orientación de la ventana de lectura                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| **Antes de la versión 6.0** | A. Lectura de datos privados de IME de acceso a la ventana directamente. Vea "4 Structure" (Estructura 4). | Captura de mensajes privados de IME. Vea "3 mensajes" | Examine la información del Registro. Vea "5 Información del Registro" |
| **Después de la versión 6.0**  | [GetReadingString](#getreadingstring)                                 | [ShowReadingWindow](#showreadingwindow)     | [GetReadingString](#getreadingstring)                      |



 

## <a name="messages"></a>error de Hadoop

Los mensajes siguientes no tienen que procesarse para un IME más reciente que implemente [ShowReadingWindow](#showreadingwindow)().

El controlador de mensajes de la aplicación (es decir, no se pasa a DefWindowProc) para evitar que se muestre la ventana de lectura.

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra cómo obtener información de cadena de lectura del IME anterior que no tiene GetReadingString(). El código genera las siguientes salidas:



| Output              | Descripción                                                                                      |
|--------------|---------------------------------------------------------------------------------------|
| DWORD dwlen  | Longitud de la cadena de lectura.                                                          |
| DWORD dwerr  | Índice del carácter de error.                                                                   |
| LPWSTR wstr  | Puntero a la cadena de lectura.                                                         |
| UNICODE BOOL | Si es true, la cadena de lectura está en formato Unicode. De lo contrario, está en formato multibyte. |



 

### <a name="cht-ime-version-42-43-and-44"></a>CHT IME versión 4.2, 4.3 y 4.4

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a>CHT IME versión 5.0

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

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a>CHT IME versión 5.1, 5.2 y CHS IME versión 5.3

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

### <a name="chs-ime-version-41"></a>IME de CHS, versión 4.1

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

### <a name="chs-ime-version-42"></a>IME de CHS, versión 4.2

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

Una aplicación de pantalla completa debe controlar correctamente los siguientes mensajes relacionados con IME:

### <a name="wm_inputlangchange"></a>WM \_ INPUTLANGCHANGE

IMM envía un mensaje DE WM INPUTLANGCHANGE a la ventana activa de una aplicación después de que el usuario haya cambiado la configuración regional de entrada con una combinación de teclas (normalmente ALT+MAYÚS) o con el indicador de configuración regional de entrada en la barra de tareas o la barra de \_ idioma. La barra de idioma es un control en pantalla con el que el usuario puede configurar un servicio de texto. (Vea [Cómo mostrar la barra de idioma).](/windows/desktop/TSF/how-to-set-up-tsf) La siguiente captura de pantalla muestra una lista de selección de idioma que se muestra cuando el usuario hace clic en el indicador de configuración regional.

![lista de selección de idioma que se muestra cuando el usuario hace clic en el indicador de configuración regional](images/ime-langselection.png)

Cuando IMM envía un mensaje DE WM \_ INPUTLANGCHANGE, CDALTERTIMEEditBox debe realizar varias tareas importantes:

1.  Se llama al método GetKeyboardLayout para devolver el identificador de configuración regional (ID) de entrada para el subproceso de aplicación. La clase CDCOLATIMEEditBox guarda este identificador en su variable miembro estática \_ hklCurrent para su uso posterior. Es importante que la aplicación conozca la configuración regional de entrada actual, ya que el IME de cada idioma tiene su propio comportamiento distinto. Es posible que el desarrollador tenga que proporcionar código diferente para distintas configuraciones regionales de entrada.
2.  CDEDITTIMEEditBox inicializa una cadena para mostrarla en el indicador de idioma del cuadro de edición. Este indicador puede mostrar el idioma de entrada activo cuando la aplicación se ejecuta en modo de pantalla completa y ni la barra de tareas ni la barra de idioma están visibles.
3.  Se llama al método ImmGetConversionStatus para indicar si la configuración regional de entrada está en modo de conversión nativo o no nativo. El modo de conversión nativa permite al usuario escribir texto en el idioma elegido. El modo de conversión no nativo hace que el teclado actúe como un teclado en inglés estándar. Es importante proporcionar al usuario una indicación visual sobre en qué tipo de modo de conversión se encuentra el IME, para que el usuario pueda saber fácilmente qué caracteres esperar al pulsar una tecla. CDEDITTIMEEditBox proporciona esta indicación visual con un color de indicador de idioma. Cuando la configuración regional de entrada usa un IME con el modo de conversión nativo, la clase CDANDERTIMEEditBox dibuja el texto del indicador con el color definido por el parámetro m \_ IndicatorImeColor. Cuando el IME está en modo de conversión no nativo o no se usa ningún IME, la clase dibuja el texto del indicador con el color definido por el parámetro m \_ IndicatorEngColor.
4.  CDCORETIMEEditBox comprueba la configuración regional de entrada y establece la variable miembro estática s bInsertOnType en TRUE para coreano y FALSE para todos los \_ demás idiomas. Esta marca es necesaria debido a los distintos comportamientos de los IME coreanos y de todos los demás IME. Al escribir caracteres en idiomas distintos del coreano, el texto escrito por el usuario se muestra en la ventana de composición y el usuario puede cambiar libremente el contenido de la cadena de composición. El usuario presiona la tecla ENTRAR cuando se satisface con la cadena de composición y la cadena de composición se envía a la aplicación como una serie de mensajes \_ WM CHAR. Sin embargo, en los IME coreanos, cuando un usuario presiona una tecla para escribir texto, se envía inmediatamente un carácter a la aplicación. Cuando el usuario presiona posteriormente más teclas para modificar ese carácter inicial, el carácter del cuadro de edición cambia para reflejar la entrada adicional del usuario. Básicamente, el usuario está escribiendo caracteres en el cuadro de edición. Estos dos comportamientos son lo suficientemente diferentes como para que CD QRTIMEEditBox deba codificar para cada uno de ellos específicamente.
5.  Se llama al método de miembro estático SetupImeApi para recuperar direcciones de dos funciones del módulo IME: GetReadingString y ShowReadingWindow. Si existen estas funciones, se llama a ShowReadingWindow para ocultar la ventana de lectura predeterminada para este IME. Dado que la aplicación representa la propia ventana de lectura, notifica al IME que deshabilite el dibujo de la ventana de lectura predeterminada para que no interfiera con la representación a pantalla completa.

IMM envía un mensaje \_ SETCONTEXT de WM IME cuando se activa una \_ ventana de la aplicación. El parámetro lParam de este mensaje contiene una marca que indica al IME qué ventanas se deben dibujar y cuáles no. Dado que la aplicación está controlando todo el dibujo, no necesita el IME para dibujar ninguna de las ventanas de IME. Por lo tanto, el controlador de mensajes de la aplicación simplemente establece lParam en 0 y devuelve .

Para que las aplicaciones admitan IME, se necesita un procesamiento especial para el mensaje WM IME SETCONTEXT relacionado con \_ \_ IME. Puesto que Windows normalmente envía este mensaje a la aplicación antes de llamar al método PanoramaInitialize(), Panorama no tiene la oportunidad de procesar la interfaz de usuario para mostrar las ventanas de lista candidatas.

El siguiente fragmento de código especifica a las aplicaciones de Windows que no muestren ninguna interfaz de usuario asociada a la ventana de lista de candidatos, lo que permite a Panorama controlar específicamente esta interfaz de usuario.

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a>WM \_ IME \_ STARTCOMPOSITION

IMM envía un mensaje STARTCOMPOSITION de WM IME a la aplicación cuando una composición de IME está a punto de comenzar como resultado de pulsaciones de teclas \_ \_ por parte del usuario. Si el IME usa la ventana de composición, muestra la cadena de composición actual en una ventana de composición. CDDORESTIMEEditBox controla este mensaje mediante la realización de dos tareas:

1.  CDEDITTIMEEditBox borra el búfer de cadenas de composición y el búfer de atributos. Estos búferes son miembros estáticos de CDEDITTIMEEditBox.
2.  CD CURSORTIMEEditBox establece la variable miembro \_ estática bHideCaret de s en TRUE. Este miembro, definido en la clase base CDXUTEditBox, controla si el cursor del cuadro de edición debe dibujarse cuando se represente el cuadro de edición. La ventana de composición funciona de forma similar a un cuadro de edición con texto y cursor. Para evitar confusiones cuando la ventana de composición está visible, el cuadro de edición oculta su cursor para que solo esté visible un cursor a la vez.

### <a name="wm_ime_composition"></a>WM \_ IME \_ COMPOSITION

IMM envía un mensaje WM IME COMPOSITION a la aplicación cuando el usuario escribe una pulsación de \_ tecla para cambiar la cadena de \_ composición. El valor de lParam indica qué tipo de información puede recuperar la aplicación del Administrador de métodos de entrada (IMM). La aplicación debe recuperar la información disponible llamando a [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) y, a continuación, debe guardar la información en su búfer privado para que pueda representar los elementos IME más adelante.

CDEDITTIMEEditBox busca y recupera los siguientes datos de cadena de composición:



| [**WM \_ Valor de \_ marca iME COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) lParam | data                           | Descripción                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GCS \_ COMPATTR                                                         | Atributo Composition          | Este atributo contiene información como el estado de cada carácter de la cadena de composición (por ejemplo, convertido o no convertido). Esta información es necesaria porque CD BYTETIMEEditBox colore los caracteres de cadena de composición de forma diferente en función de sus atributos.                                                                                   |
| GCS \_ COMPCLAUSE                                                       | Información de la cláusula composition | Esta información de cláusula se usa cuando el IME japonés está activo. Cuando se convierte una cadena de composición japonesa, los caracteres se pueden agrupar como una cláusula que se convierte en una sola entidad. Cuando el usuario mueve el cursor, CD CURSORTIMEEditBox usa esta información para resaltar toda la cláusula, en lugar de un solo carácter dentro de la cláusula . |
| GCS \_ COMPSTR                                                          | Cadena de composición             | Esta cadena es la cadena actualizada que está compuesta por el usuario. También es la cadena que se muestra en la ventana de composición.                                                                                                                                                                                                                                        |
| CURSORPOS \_ de GCS                                                        | Posición del cursor de composición    | La ventana de composición implementa un cursor, similar al cursor de un cuadro de edición. La aplicación puede recuperar la posición del cursor al procesar el mensaje COMPOSITION de WM \_ IME \_ para dibujar el cursor correctamente.                                                                                                                                            |
| GCS \_ RESULTSTR                                                        | Cadena de resultado                  | La cadena de resultado está disponible cuando el usuario está a punto de completar el proceso de composición. Esta cadena se debe recuperar y los caracteres se deben enviar al cuadro de edición.                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a>WM \_ IME \_ ENDCOMPOSITION

IMM envía un mensaje ENDCOMPOSITION de WM IME a la aplicación cuando finaliza la operación de composición \_ \_ de IME. Esto puede ocurrir cuando el usuario presiona la tecla ENTRAR para aprobar la cadena de composición o la tecla ESC para cancelar la composición. CD COMPOSTIMEEditBox controla este mensaje estableciendo el búfer de cadena de composición en vacío. A continuación, establece bHideCaret en FALSE porque la ventana de composición está cerrada y el cursor del cuadro de edición \_ debe volver a estar visible.

El controlador de mensajes CDEDITTIMEEditBox también establece \_ bShowReadingWindow en FALSE. Esta marca controla si la clase dibuja la ventana de lectura cuando el cuadro de edición se representa a sí mismo, por lo que debe establecerse en FALSE cuando finaliza una composición.

### <a name="wm_ime_notify"></a>WM \_ IME \_ NOTIFY

IMM envía un mensaje WM IME NOTIFY a la aplicación cada \_ vez que cambia una ventana de \_ IME. Una aplicación que controla el dibujo de las ventanas de IME debe procesar este mensaje para que sea consciente de cualquier actualización del contenido de la ventana. wParam indica el comando o el cambio que se está llevando a cabo. CDEDITTIMEEditBox controla los siguientes comandos:



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
<td>Este atributo contiene información como el estado de cada carácter de la cadena de composición (por ejemplo, convertido o no convertido). Esta información es necesaria porque CD BYTETIMEEditBox colore los caracteres de cadena de composición de forma diferente en función de sus atributos.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  /  <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></td>
<td>Se envía a la aplicación cuando la ventana candidata está a punto de abrirse o actualizarse, respectivamente. La ventana candidata se abre cuando un usuario desea cambiar la opción de texto convertido. La ventana se actualiza cuando un usuario mueve el indicador de selección o cambia la página. CDEDITTIMEEditBox usa un controlador de mensajes para ambos comandos porque las tareas necesarias son exactamente las mismas:<br/>
<ol>
<li>CDSHOWTIMEEditBox establece el miembro bShowWindow de la estructura de lista de candidatos s_CandList en TRUE para indicar que la ventana candidata debe dibujarse durante la representación del marco.</li>
<li>CDDHTIMEEditBox recupera la lista de candidatos mediante una llamada a <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList,</strong></a>primero para obtener el tamaño de búfer necesario y, después, para obtener los datos reales.</li>
<li>La estructura de lista de candidatos s_CandList se inicializa con los datos candidatos recuperados.</li>
<li>Las cadenas candidatas se almacenan como una matriz de cadenas.</li>
<li>Se guarda el índice de la entrada seleccionada, así como el índice de página.</li>
<li>CDEDITTIMEEditBox comprueba si el estilo de la ventana candidata es vertical u horizontal. Si el estilo de ventana es horizontal, se debe inicializar un búfer de cadena adicional, el miembro HoriCand de s_CandList, con todas las cadenas candidatas, con caracteres de espacio insertados entre todas las cadenas adyacentes. Al representar una ventana candidata vertical, las cadenas candidatas individuales se dibujan de una en una, con las coordenadas y incrementadas para cada cadena. Sin embargo, esta cadena HoriCand debe usarse al representar una ventana candidata horizontal, ya que el carácter de espacio es la mejor manera de separar dos cadenas adyacentes en la misma línea.</li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></td>
<td>Se envía a la aplicación cuando una ventana candidata está a punto de cerrarse. Esto sucede cuando un usuario ha realizado una selección de la lista de candidatos. CDANDERTIMEEditBox controla este comando estableciendo la marca visible de la ventana candidata en FALSE y, a continuación, borrando el búfer de cadenas candidatas.</td>
</tr>
<tr class="even">
<td>IMN_PRIVATE</td>
<td>Se envía a la aplicación cuando el IME ha actualizado su cadena de lectura como resultado de que el usuario escriba o quite caracteres. La aplicación debe recuperar la cadena de lectura y guardarla para su representación. CDEDITTIMEEditBox tiene dos métodos para recuperar la cadena de lectura, en función de cómo se admiten las cadenas de lectura en el IME: <br/>
<ul>
<li>Si el IME admite la función GetReadingString, se llama a GetReadingString para recuperar la cadena de lectura.</li>
<li>Si el IME no implementa GetReadingString, CDSTRINGTIMEEditBox recupera la cadena de lectura del contenido del contexto de entrada.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="rendering"></a>Representación

La representación de los elementos y ventanas de IME es sencilla. CDEDITTIMEEditBox permite que la clase base se represente primero porque las ventanas IME deben aparecer en la parte superior del control de edición. Después de representar el cuadro de edición base, CDANDERTIMEEditBox comprueba la marca de visibilidad de cada ventana de IME (indicador, composición, candidato y ventana de lectura) y dibuja la ventana si debe estar visible. Consulte Comportamiento predeterminado de IME para obtener descripciones de los diferentes tipos de ventana de IME.

### <a name="input-locale-indicator"></a>Indicador de configuración regional de entrada

El indicador de configuración regional de entrada se representa antes que cualquier otra ventana IME porque es un elemento que siempre se muestra. Por lo tanto, debería aparecer debajo de otras ventanas de IME. CDINTEGRATIMEEditBox representa el indicador mediante una llamada al método RenderIndicator, en el que el color de fuente del indicador se determina mediante el examen de la variable estática S ImeState, que refleja el modo de conversión \_ de IME actual. Cuando el IME está habilitado y la conversión nativa está activa, el método usa m \_ IndicatorImeColor como color del indicador. Si el IME está deshabilitado o está en modo de conversión no nativo, se usa m \_ IndicatorImeColor para dibujar el texto del indicador. De forma predeterminada, la propia ventana del indicador se dibuja a la derecha del cuadro de edición. Las aplicaciones pueden cambiar este comportamiento invalidando el método RenderIndicator.

En la ilustración siguiente se muestran las distintas apariencias de un indicador de configuración regional de entrada para inglés, japonés en modo de conversión alfanumérica y japonés en modo de conversión nativa:

![diferentes apariencias de un indicador de configuración regional de entrada para inglés y japonés](images/ime-indicator.png)

### <a name="composition-window"></a>Ventana Composición

El dibujo de la ventana de composición se controla en el método RenderComposition de CDCOMPOSICIÓNTIMEEditBox. La ventana de composición flota sobre el cuadro de edición. Debe dibujarse en la posición del cursor del control de edición subyacente. CDEDITTIMEEditBox controla la representación de la manera siguiente:

1.  Toda la cadena de composición se dibuja con los colores predeterminados de la cadena de composición.
2.  Los caracteres con determinados atributos especiales se deben dibujar en colores diferentes, por lo que CD BYTETIMEEditBox revisa los caracteres de la cadena de composición e inspecciona el atributo de cadena. Si el atributo llama a colores diferentes, el carácter se dibuja de nuevo con los colores adecuados.
3.  El cursor de la ventana de composición se dibuja para completar la representación.

El cursor debe parpadear para los IME coreanos, pero no para otros IME. RenderComposition determina si el cursor debe estar visible en función de los valores de temporizador cuando se usa el IME coreano.

### <a name="reading-and-candidate-windows"></a>Ventanas de lectura y candidatas

Las ventanas de lectura y candidatas se representan mediante el mismo método CDOIDTIMEEditBox, RenderCandidateReadingWindow. Ambas ventanas contienen una matriz de cadenas para el diseño vertical o una sola cadena en el caso del diseño horizontal. La mayor parte del código de RenderCandidateReadingWindow se usa para colocar la ventana de modo que ninguna parte de la ventana esté fuera de la ventana de la aplicación y se recorte.

## <a name="limitations"></a>Limitaciones

A veces, los IME contienen características avanzadas para mejorar la facilidad de entrada de texto. Algunas de las características que se encuentran en los IME más recientes se muestran en las cifras siguientes. Estas características avanzadas no están presentes en DXUT. Implementar la compatibilidad con estas características avanzadas puede ser complicado porque no hay ninguna interfaz definida para obtener la información necesaria de los IME.

IME chino tradicional avanzado con lista de candidatos expandida:

![ime chino tradicional avanzado con lista de candidatos expandida](images/ime-advanced1.png)

IME japonés avanzado con algunas entradas candidatas que contienen texto adicional para describir sus significados:

![ime japonés avanzado con algunas entradas candidatas que contienen texto adicional para describir sus significados](images/ime-advanced2.png)

IME coreano avanzado que incluye un sistema de reconocimiento de escritura a mano:

![ime coreano avanzado que incluye un sistema de reconocimiento de escritura a mano](images/ime-advanced3.png)

## <a name="registry-information"></a>Información del Registro

La siguiente información del Registro se comprueba para determinar la orientación de la ventana de lectura, cuando el IME actual es un nuevo fonético CHT anterior que no implementa GetReadingString().



| Key                                                           | Valor            |
|---------------------------------------------------------------|------------------|
| HKCU \\ software \\ microsoft \\ windows \\ currentversion \\ IME \_ Name | asignación de teclado |



 

Dónde: El nombre de IME es MSTCIPH si la versión del archivo IME es 5.1 o posterior; de lo contrario, el nombre \_ de IME \_ es TINTLGNT.

La orientación de la ventana de lectura es horizontal si:

-   El IME es la versión 5.0 y el valor de asignación de teclado es 0x22 o 0x23
-   El IME es la versión 5.1 o 5.2 y el valor de asignación de teclado es 0x22, 0x23 o 0x24.

Si no se cumple ninguna condición, la ventana de lectura es vertical.

## <a name="appendix-a-cht-versions-per-operating-system"></a>Apéndice A: Versiones de CHT por sistema operativo



| Sistema operativo           | Versión de IME de CHT |
|----------------------------|-----------------|
| Windows 98                 | 4,2             |
| Windows 2000               | 4.3             |
| unknown                    | 4.4.             |
| Windows ME                 | 5.0             |
| Office XP                  | 5,1             |
| Windows XP                 | 5.2             |
| Descarga web independiente | 6.0             |



 

## <a name="further-information"></a>Información adicional

Para obtener información adicional, vea lo siguiente:

-   [Instalación y uso de editores de métodos de entrada](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [Presentación de texto internacional](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [El consorcio Unicode](https://www.unicode.org/)
-   Desarrollo de software internacional. Dr. International. Segundo ed. Redmond, WA: Microsoft Press, 2003.

## <a name="getreadingstring"></a>GetReadingString

Obtiene información de cadena de lectura.

**Parámetros**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[en \] contexto de entrada.

</dd> <dt>

<span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*
</dt> <dd>

\[en \] Longitud de lpwReadingBuf, en WCHAR. Si es cero, significa que la longitud del búfer de lectura de consultas.

</dd> <dt>

<span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf* 
</dt> <dd>

\[out \] Devuelve la cadena de lectura (no el extremo cero).

</dd> <dt>

<span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex* 
</dt> <dd>

\[out \] Devuelve el índice del carácter de error en la cadena de lectura si lo hay.

</dd> <dt>

<span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical* 
</dt> <dd>

\[out \] Si es TRUE, la lectura de la interfaz de usuario es vertical. De lo contrario, puMaxReadingLen horizontal.

</dd> <dt>

<span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen* 
</dt> <dd>

\[out \] Longitud de la interfaz de usuario de lectura. La longitud máxima de lectura no es fija; depende no solo del diseño del teclado, sino también del modo de entrada (por ejemplo, código interno o entrada suplente).

</dd> </dl>

**Valores devueltos**

Longitud de la cadena de lectura.

**Comentarios:**

Si el valor devuelto es mayor que el valor de uReadingBufLen, todos los parámetros de salida no están definidos.

Esta función se implementa en CHT IME 6.0 o posterior y GetProcAddress puede adquirirla en un identificador de módulo IME; ImmGetIMEFileName y LoadLibrary pueden adquirir el identificador del módulo IME.

**Requisitos**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Rúbrica**
</dt> <dd>

Declarado en Imm.h.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Biblioteca de importación**
</dt> <dd>

Use Imm.lib.

</dd> </dl>

## <a name="showreadingwindow"></a>ShowReadingWindow

Mostrar (u ocultar) la ventana de lectura.

**Parámetros**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[en \] contexto de entrada.

</dd> <dt>

<span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow* 
</dt> <dd>

\[en \] Establecer en TRUE para mostrar la ventana de lectura (o FALSE para ocultarla).

</dd> </dl>

**Valores devueltos**

**Comentarios:**

Devuelve TRUE si se realiza correctamente o FALSE si no es así.

**Requisitos**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Rúbrica**
</dt> <dd>

Declarado en Imm.h.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Biblioteca de importación**
</dt> <dd>

Use Imm.lib.

</dd> </dl>