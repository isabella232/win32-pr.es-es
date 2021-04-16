---
title: Cuadro de diálogo Color
description: Muestra un cuadro de diálogo modal que permite al usuario elegir un valor de color específico.
ms.assetid: 248586b5-5068-4021-8407-56eb79243789
keywords:
- entrada de usuario, biblioteca de cuadros de diálogo comunes
- capturar la entrada del usuario, la biblioteca de cuadros de diálogo comunes
- Biblioteca de cuadros de diálogo comunes
- cuadros de diálogo comunes
- Cuadro de diálogo Color
- Color parcial (cuadro de diálogo)
- Color completo (cuadro de diálogo)
- cuadro de diálogo personalizar color
- Modelo de color RGB
- Modelo de color HSL
- matiz saturación luminosidad (HSL)
- HSL (luminosidad de saturación de matiz)
- RGB (rojo verde azul)
- azul verde rojo (RGB)
- enlaces, color (cuadro de diálogo)
- cuadros de diálogo predefinidos
- cuadros de diálogo, color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb90150f49ea7bed4edac53af40ba89e0459946
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/19/2020
ms.locfileid: "104567925"
---
# <a name="color-dialog-box"></a>Cuadro de diálogo Color

Muestra un cuadro de diálogo modal que permite al usuario elegir un valor de color específico. El usuario puede elegir un color de un conjunto de paletas de colores básico o personalizado. Como alternativa, el usuario puede generar un valor de color mediante la modificación de los valores de color RGB o Hue, saturación y luminosidad (HSL) de la interfaz de usuario del cuadro de diálogo. El cuadro de diálogo **color** devuelve el valor RGB del color seleccionado por el usuario.

Puede crear y mostrar un cuadro de diálogo de **color** inicializando una estructura [**las choosecolor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) y pasando la estructura a la función [**las choosecolor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) . Al establecer distintos valores de parámetro para la estructura **las choosecolor.** , puede afectar al modo en que se muestra el cuadro de diálogo color. Por ejemplo, puede mostrar una versión de la interfaz de usuario completa o parcial del cuadro de diálogo. En la ilustración siguiente se muestra la versión completa de la interfaz de usuario del cuadro de diálogo **color** .

![cuadro de diálogo de colores](images/colordialogboxxp.png)

Si el usuario hace clic en el botón **Aceptar** , [**las choosecolor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) devuelve **true**. El miembro **rgbResult** de la estructura [**las choosecolor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) contiene el valor de color RGB del color seleccionado por el usuario. El valor de color RGB especifica las intensidades de los colores rojo, verde y azul individuales que componen el color seleccionado. Los valores individuales van del 0 al 255. Use las macros [**GetRValue**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue)y [**GetBValue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue) para extraer colores individuales de un valor de color RGB.

Si el usuario cancela el cuadro de diálogo de **color** o se produce un error, [**las choosecolor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) devuelve **false** y no se define el miembro **rgbResult** . Para determinar la causa del error, llame a la función [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar el valor de error extendido.

En esta sección se describen los temas siguientes:

-   [Cuadros de diálogo de color completo y parcial](#full-and-partial-color-dialog-boxes)
-   [Personalización del cuadro de diálogo color](#customizing-the-color-dialog-box)
    -   [Para proporcionar una plantilla personalizada para el cuadro de diálogo color](#to-provide-a-custom-template-for-the-color-dialog-box)
    -   [Para habilitar un procedimiento de enlace para el cuadro de diálogo color](#to-enable-a-hook-procedure-for-the-color-dialog-box)
-   [Modelos de color utilizados por el cuadro de diálogo color](#color-models-used-by-the-color-dialog-box)
    -   [Modelo de color RGB](#rgb-color-model)
    -   [Modelo de color HSL](#hsl-color-model)
    -   [Convertir valores HSL en valores RGB](#converting-hsl-values-to-rgb-values)

## <a name="full-and-partial-color-dialog-boxes"></a>Cuadros de diálogo de color completo y parcial

El cuadro de diálogo color tiene una versión completa y una versión parcial de la interfaz de usuario. La versión completa incluye los controles básicos y tiene controles adicionales que permiten al usuario crear colores personalizados. La versión parcial tiene controles que muestran las paletas de colores básicas y personalizadas desde las que el usuario puede seleccionar un valor de color.

La versión parcial del cuadro de diálogo color incluye un botón **definir colores personalizados** . El usuario puede hacer clic en este botón para mostrar la versión completa. Puede dirigir el cuadro de diálogo color para mostrar siempre la versión completa estableciendo la marca **\_ FULLOPEN de CC** en el miembro **Flags** de la estructura [**las choosecolor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) . Para evitar que el usuario cree colores personalizados, puede establecer la marca **\_ PREVENTFULLOPEN de CC** para deshabilitar el botón **definir colores personalizados** .

Los colores básicos representan una selección de los colores disponibles en el dispositivo especificado. El número real de colores mostrados viene determinado por el controlador de pantalla. Por ejemplo, un controlador VGA muestra 48 colores y un controlador de pantalla monocromo muestra solo 16.

Los colores personalizados son los que se especifican o que el usuario crea. Al crear un cuadro de diálogo de color, debe usar el miembro **lpCustColors** de la estructura [**las choosecolor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) para especificar los valores iniciales de los 16 colores personalizados. Si está abierta la versión completa del cuadro de diálogo color, el usuario puede crear un color personalizado mediante uno de los métodos siguientes:

-   Mover el cursor en el control de espectro de color y el control deslizante de luminosidad
-   Escribir valores RGB en los controles de edición **rojo**, **verde** y **azul**
-   Escribir valores HSL en los controles **Hue**, **SAT** y **Lum** Edit

Para agregar un nuevo color personalizado a la presentación de los colores personalizados, el usuario puede hacer clic en el botón **Agregar a los colores personalizados** . Esto también hace que el cuadro de diálogo copie el valor RGB del nuevo color en el elemento correspondiente de la matriz a la que señala el miembro **lpCustColors** . Para conservar los nuevos colores personalizados entre las llamadas a [**las choosecolor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)), debe asignar la memoria estática para la matriz. Para obtener más información sobre los modelos de color RGB y HSL, vea [modelos de color utilizados por el cuadro de diálogo color](#color-models-used-by-the-color-dialog-box).

## <a name="customizing-the-color-dialog-box"></a>Personalización del cuadro de diálogo color

Para personalizar un cuadro de diálogo de color, puede utilizar cualquiera de los métodos siguientes:

-   Especificar valores en la estructura [**las choosecolor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) al crear el cuadro de diálogo
-   Proporcionar una plantilla personalizada
-   Proporcionar un procedimiento de enlace

Puede modificar la apariencia y el comportamiento del cuadro de diálogo color estableciendo marcas en el miembro **Flags** de la estructura [**las choosecolor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) . Por ejemplo, puede establecer la marca **CC \_ SOLIDCOLOR** para dirigir el cuadro de diálogo para mostrar solo colores sólidos. Para hacer que el cuadro de diálogo Seleccione inicialmente un color que no sea el negro, establezca la marca **\_ RGBINIT de CC** y especifique un color en el miembro **rgbResult** .

Puede proporcionar una plantilla personalizada para el cuadro de diálogo color, por ejemplo, si desea incluir controles adicionales que sean únicos para la aplicación. La función [**las choosecolor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) usa la plantilla personalizada en lugar de la plantilla predeterminada.

### <a name="to-provide-a-custom-template-for-the-color-dialog-box"></a>Para proporcionar una plantilla personalizada para el cuadro de diálogo color

1.  Cree la plantilla personalizada modificando la plantilla predeterminada especificada en el archivo color. Dlg. Los identificadores de control que se usan en la plantilla de cuadro de diálogo color predeterminado se definen en el archivo color. Dlg.
2.  Use la estructura [**las choosecolor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) para habilitar la plantilla de la manera siguiente:
    -   Si la plantilla personalizada es un recurso de una aplicación o una biblioteca de vínculos dinámicos, establezca la marca **\_ ENABLETEMPLATE de CC** en el miembro **Flags** . Use los miembros **hInstance** y **lpTemplateName** de la estructura para identificar el nombre del módulo y del recurso.

        -O bien-

    -   Si la plantilla personalizada ya está en la memoria, establezca la marca **\_ ENABLETEMPLATEHANDLE de CC** . Use el miembro **hInstance** para identificar el objeto de memoria que contiene la plantilla.

Puede proporcionar un procedimiento de enlace [**CCHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc) para el cuadro de diálogo color. El procedimiento de enlace puede procesar los mensajes enviados al cuadro de diálogo. También puede utilizar mensajes registrados para controlar el comportamiento del cuadro de diálogo. Si usa una plantilla personalizada para definir controles adicionales, debe proporcionar un procedimiento de enlace para procesar la entrada para los controles.

### <a name="to-enable-a-hook-procedure-for-the-color-dialog-box"></a>Para habilitar un procedimiento de enlace para el cuadro de diálogo color

1.  Establezca la **marca \_ ENABLEHOOK de CC** en el miembro **Flags** de la estructura [**las choosecolor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) .
2.  Especifique la dirección del procedimiento de enlace en el miembro **lpfnHook** .

Después de procesar el mensaje de [**\_ INITDIALOG de WM**](wm-initdialog.md) , el procedimiento de cuadro de diálogo envía un mensaje de **WM \_ INITDIALOG** al procedimiento de enlace. El parámetro *lParam* de este mensaje es un puntero a la estructura [**las choosecolor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) que se usa para inicializar el cuadro de diálogo.

El cuadro de diálogo envía el mensaje registrado [**COLOROKSTRING**](colorokstring.md) al procedimiento de enlace cuando el usuario hace clic en el botón **Aceptar** . El procedimiento de enlace puede rechazar el color seleccionado y forzar que el cuadro de diálogo permanezca abierto devolviendo cero cuando recibe este mensaje. El procedimiento de enlace puede hacer que el cuadro de diálogo Seleccione un color determinado mediante el envío del mensaje registrado [**SETRGBSTRING**](setrgbstring.md) al cuadro de diálogo. Para usar estos mensajes registrados, debe pasar las constantes **COLOROKSTRING** y **SETRGBSTRING** a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener un identificador de mensaje. A continuación, puede utilizar el identificador para detectar y procesar los mensajes enviados desde el cuadro de diálogo, o para enviar mensajes al cuadro de diálogo.

## <a name="color-models-used-by-the-color-dialog-box"></a>Modelos de color utilizados por el cuadro de diálogo color

La extensión de colores personalizados del cuadro de diálogo color permite al usuario especificar un color con los valores RGB o HSL. Sin embargo, la estructura [**las choosecolor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) solo usa valores RGB para informar de los colores creados o seleccionados por el usuario.

-   [Modelo de color RGB](#rgb-color-model)
-   [Modelo de color HSL](#hsl-color-model)
-   [Convertir valores HSL en valores RGB](#converting-hsl-values-to-rgb-values)

### <a name="rgb-color-model"></a>Modelo de color RGB

El modelo RGB se usa para designar los colores de las pantallas y otros dispositivos que emiten luz. Los valores de rojo, verde y azul válidos van de 0 a 255, donde 0 indica la intensidad mínima y 255 indica la intensidad máxima. En la ilustración siguiente se muestra cómo se pueden combinar los colores primarios rojo, verde y azul para producir cuatro colores adicionales. (En el caso de los dispositivos de visualización, el color negro se produce cuando los valores rojo, verde y azul están establecidos en 0. En la tecnología de pantalla, el color negro es la ausencia de todos los colores.)

![círculos rojo, verde y azul](images/rgbcolormodel.png)

En la tabla siguiente se enumeran ocho colores del modelo RGB y sus valores RGB asociados.



| Color   | Valores RGB    |
|---------|---------------|
| Rojo     | 255, 0, 0     |
| Verde   | 0, 255, 0     |
| Azul    | 0, 0, 255     |
| Cian    | 0, 255, 255   |
| Fucsia | 255, 0, 255   |
| Amarillo  | 255, 255, 0   |
| Blanco   | 255, 255, 255 |
| Negro   | 0, 0, 0       |



 

El sistema almacena los colores internos como valores RGB de 32 bits que tienen el formato hexadecimal siguiente: 0x00bbggrr.

El byte de orden inferior contiene un valor para la intensidad relativa de rojo; el segundo byte contiene un valor para Green; y el tercer byte contiene un valor para Blue. El byte de orden superior debe ser cero.

Puede usar la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) para obtener un valor RGB basado en las intensidades especificadas para los componentes rojo, verde y azul. Use las macros [**GetRValue**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue), [**GetBValue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue)y [**GetGValue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue) para extraer colores individuales de un valor de color RGB.

### <a name="hsl-color-model"></a>Modelo de color HSL

El cuadro de diálogo color proporciona controles para especificar los valores HSL. En la ilustración siguiente se muestra el control de espectro de color y el control de diapositiva de luminosidad que aparecen en el cuadro de diálogo color. La ilustración también muestra los intervalos de valores que el usuario puede especificar con estos controles.

![gama de colores y escala de luminosidad](images/colordialogranges.png)

En el cuadro de diálogo color, los valores de saturación y luminosidad deben estar en el intervalo comprendido entre 0 y 240 y el valor de matiz debe estar en el intervalo comprendido entre 0 y 239.

### <a name="converting-hsl-values-to-rgb-values"></a>Convertir valores HSL en valores RGB

El procedimiento de cuadro de diálogo proporcionado en Comdlg32.dll para el cuadro de diálogo color contiene código que convierte los valores HSL en los valores RGB correspondientes. En la tabla siguiente se enumeran los ocho colores del modelo RGB y sus valores HSL y RGB asociados.



| Color   | HSL (valores)      | Valores RGB      |
|---------|-----------------|-----------------|
| Rojo     | (0, 240, 120)   | (255, 0, 0)     |
| Amarillo  | (40, 240, 120)  | (255, 255, 0)   |
| Verde   | (80, 240, 120)  | (0, 255, 0)     |
| Cian    | (120, 240, 120) | (0, 255, 255)   |
| Azul    | (160, 240, 120) | (0, 0, 255)     |
| Fucsia | (200, 240, 120) | (255, 0, 255)   |
| Blanco   | (0, 0, 240)     | (255, 255, 255) |
| Negro   | (0, 0, 0)       | (0, 0, 0)       |



 

 

 
