---
title: Cuadro de diálogo Color
description: Muestra un cuadro de diálogo modal que permite al usuario elegir un valor de color específico.
ms.assetid: 248586b5-5068-4021-8407-56eb79243789
keywords:
- entrada de usuario, Biblioteca común de cuadros de diálogo
- capturar la entrada del usuario, Biblioteca de cuadros de diálogo común
- Biblioteca común de cuadros de diálogo
- cuadros de diálogo comunes
- Cuadro de diálogo Color
- partial Color (cuadro de diálogo)
- cuadro de diálogo Color completo
- personalizar color (cuadro de diálogo)
- Modelo de color RGB
- Modelo de color HSL
- luminosidad de saturación de hue (HSL)
- HSL (luminosidad de saturación de matiz)
- RGB (azul verde rojo)
- azul verde rojo (RGB)
- hooks,Color (cuadro de diálogo)
- cuadros de diálogo predefinidos
- cuadros de diálogo, Color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb90150f49ea7bed4edac53af40ba89e0459946
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569296"
---
# <a name="color-dialog-box"></a>Cuadro de diálogo Color

Muestra un cuadro de diálogo modal que permite al usuario elegir un valor de color específico. El usuario puede elegir un color de un conjunto de paletas de colores básicas o personalizadas. Como alternativa, el usuario puede generar un valor de color modificando los valores de color RGB o matiz, saturación, luminosidad (HSL) de la interfaz de usuario del cuadro de diálogo. El **cuadro** de diálogo Color devuelve el valor RGB del color seleccionado por el usuario.

Para crear y mostrar un **cuadro de diálogo Color,** inicialice una [**estructura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) y pase la estructura a la [**función ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) Al establecer distintos valores de parámetro para **la estructura CHOOSECOLOR,** puede afectar a cómo aparece el cuadro de diálogo Color. Por ejemplo, puede mostrar una versión completa o parcial de la interfaz de usuario del cuadro de diálogo. En la ilustración siguiente se muestra la versión completa de la interfaz de usuario del **cuadro de diálogo** Color.

![cuadro de diálogo de colores](images/colordialogboxxp.png)

Si el usuario hace clic en el **botón Aceptar,** [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) devuelve **TRUE.** El **miembro rgbResult** de la [**estructura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) contiene el valor de color RGB del color seleccionado por el usuario. El valor de color RGB especifica las intensidades de los colores rojo, verde y azul individuales que son los que lo concidan. Los valores individuales oscilan entre 0 y 255. Use las macros [**GetRValue**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue)y [**GetBValue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue) para extraer colores individuales de un valor de color RGB.

Si el usuario cancela el cuadro de diálogo **Color** o se produce un error, [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) devuelve **FALSE** y el **miembro rgbResult** no está definido. Para determinar la causa del error, llame a la [**función CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar el valor de error extendido.

En esta sección se tratan los siguientes temas.

-   [Cuadros de diálogo de color completo y parcial](#full-and-partial-color-dialog-boxes)
-   [Personalizar el cuadro de diálogo Color](#customizing-the-color-dialog-box)
    -   [Para proporcionar una plantilla personalizada para el cuadro de diálogo Color](#to-provide-a-custom-template-for-the-color-dialog-box)
    -   [Para habilitar un procedimiento de enlace para el cuadro de diálogo Color](#to-enable-a-hook-procedure-for-the-color-dialog-box)
-   [Modelos de color usados por el cuadro de diálogo Color](#color-models-used-by-the-color-dialog-box)
    -   [Modelo de color RGB](#rgb-color-model)
    -   [Modelo de color HSL](#hsl-color-model)
    -   [Convertir valores HSL en valores RGB](#converting-hsl-values-to-rgb-values)

## <a name="full-and-partial-color-dialog-boxes"></a>Cuadros de diálogo de color completo y parcial

El cuadro de diálogo Color tiene una versión completa y una versión parcial de la interfaz de usuario. La versión completa incluye los controles básicos y tiene controles adicionales que permiten al usuario crear colores personalizados. La versión parcial tiene controles que muestran las paletas de colores básicas y personalizadas desde las que el usuario puede seleccionar un valor de color.

La versión parcial del cuadro de diálogo Color incluye un **botón Definir colores personalizados.** El usuario puede hacer clic en este botón para mostrar la versión completa. Puede dirigir el cuadro de diálogo Color para mostrar siempre la versión completa estableciendo la marca **CC \_ FULLOPEN** en el miembro **Flags** de la [**estructura CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) Para evitar que el usuario cree colores personalizados, puede establecer la marca **\_ CC PREVENTFULLOPEN para** deshabilitar el botón Definir **colores** personalizados.

Los colores básicos representan una selección de los colores disponibles en el dispositivo especificado. El controlador de pantalla determina el número real de colores mostrados. Por ejemplo, un controlador VGA muestra 48 colores y un controlador de pantalla monocromática muestra solo 16.

Los colores personalizados son los que se especifican o que el usuario crea. Al crear un cuadro de diálogo Color, debe usar el miembro **lpCustColors** de la estructura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) para especificar los valores iniciales de los 16 colores personalizados. Si la versión completa del cuadro de diálogo Color está abierta, el usuario puede crear un color personalizado mediante uno de los métodos siguientes:

-   Mover el cursor en el control de espectro de colores y el control de diapositiva de luminosidad
-   Escritura de valores RGB en **los controles de** edición Rojo, Verde **y** Azul 
-   Escribir valores HSL en los controles de edición **Hue,** **Sat** y **Lum**

Para agregar un nuevo color personalizado a la presentación de colores personalizados, el usuario puede hacer clic en **el botón Agregar** a colores personalizados. Esto también hace que el cuadro de diálogo copie el valor RGB del nuevo color en el elemento correspondiente de la matriz a la que apunta el **miembro lpCustColors.** Para conservar nuevos colores personalizados entre llamadas [**a ChooseColor,**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))debe asignar memoria estática para la matriz. Para obtener más información sobre los modelos de color RGB y HSL, vea Modelos de color [usados por el cuadro de diálogo Color](#color-models-used-by-the-color-dialog-box).

## <a name="customizing-the-color-dialog-box"></a>Personalizar el cuadro de diálogo Color

Para personalizar un cuadro de diálogo Color, puede usar cualquiera de los métodos siguientes:

-   Especificar valores en la [**estructura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) al crear el cuadro de diálogo
-   Proporcionar una plantilla personalizada
-   Proporcionar un procedimiento de enlace

Puede modificar la apariencia y el comportamiento del cuadro de diálogo Color estableciendo marcas en el **miembro Flags** de la [**estructura CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) Por ejemplo, puede establecer la marca **CC \_ SOLIDCOLOR** para dirigir el cuadro de diálogo para mostrar solo colores sólidos. Para que el cuadro de diálogo seleccione inicialmente un color distinto del negro, establezca la marca **CC \_ RGBINIT** y especifique un color en el **miembro rgbResult.**

Puede proporcionar una plantilla personalizada para el cuadro de diálogo Color, por ejemplo, si desea incluir controles adicionales que sean únicos para la aplicación. La [**función ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) usa la plantilla personalizada en lugar de la plantilla predeterminada.

### <a name="to-provide-a-custom-template-for-the-color-dialog-box"></a>Para proporcionar una plantilla personalizada para el cuadro de diálogo Color

1.  Cree la plantilla personalizada modificando la plantilla predeterminada especificada en el archivo Color.dlg. Los identificadores de control usados en la plantilla de diálogo Color predeterminada se definen en el archivo Color.dlg.
2.  Use la [**estructura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) para habilitar la plantilla de la siguiente manera:
    -   Si la plantilla personalizada es un recurso de una aplicación o biblioteca de vínculos dinámicos, establezca la marca **CC \_ ENABLETEMPLATE** en el **miembro Flags.** Use los **miembros hInstance** y **lpTemplateName** de la estructura para identificar el módulo y el nombre del recurso.

        -O bien-

    -   Si la plantilla personalizada ya está en memoria, establezca la **\_ marca CC ENABLETEMPLATEHANDLE.** Use el **miembro hInstance** para identificar el objeto de memoria que contiene la plantilla.

Puede proporcionar un procedimiento [**de enlace CCHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc) para el cuadro de diálogo Color . El procedimiento de enlace puede procesar los mensajes enviados al cuadro de diálogo. También puede usar mensajes registrados para controlar el comportamiento del cuadro de diálogo. Si usa una plantilla personalizada para definir controles adicionales, debe proporcionar un procedimiento de enlace para procesar la entrada de los controles.

### <a name="to-enable-a-hook-procedure-for-the-color-dialog-box"></a>Para habilitar un procedimiento de enlace para el cuadro de diálogo Color

1.  Establezca la **marca CC \_ ENABLEHOOK** en el **miembro Flags** de la [**estructura CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
2.  Especifique la dirección del procedimiento de enlace en el **miembro lpfnHook.**

Después de procesar [**su mensaje \_ WM INITDIALOG,**](wm-initdialog.md) el procedimiento del cuadro de diálogo envía un mensaje **WM \_ INITDIALOG** al procedimiento de enlace. El *parámetro lParam* de este mensaje es un puntero a la [**estructura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) utilizada para inicializar el cuadro de diálogo.

El cuadro de diálogo envía el [**mensaje registrado COLOROKSTRING**](colorokstring.md) al procedimiento de enlace cuando el usuario hace clic en el **botón** Aceptar. El procedimiento de enlace puede rechazar el color seleccionado y forzar que el cuadro de diálogo permanezca abierto devolviendo cero cuando recibe este mensaje. El procedimiento de enlace puede forzar al cuadro de diálogo a seleccionar un color determinado mediante el envío del mensaje registrado [**SETRGBSTRING**](setrgbstring.md) al cuadro de diálogo. Para usar estos mensajes registrados, debe pasar las constantes **COLOROKSTRING** y **SETRGBSTRING** a la [**función RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener un identificador de mensaje. A continuación, puede usar el identificador para detectar y procesar los mensajes enviados desde el cuadro de diálogo, o para enviar mensajes al cuadro de diálogo.

## <a name="color-models-used-by-the-color-dialog-box"></a>Modelos de color usados por el cuadro de diálogo Color

La extensión de colores personalizados del cuadro de diálogo Color permite al usuario especificar un color mediante valores RGB o HSL. Sin embargo, [**la estructura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) solo usa valores RGB para notificar los colores creados o seleccionados por el usuario.

-   [Modelo de color RGB](#rgb-color-model)
-   [Modelo de color HSL](#hsl-color-model)
-   [Convertir valores HSL en valores RGB](#converting-hsl-values-to-rgb-values)

### <a name="rgb-color-model"></a>Modelo de color RGB

El modelo RGB se usa para designar colores para las pantallas y otros dispositivos que emiten luz. Los valores válidos de rojo, verde y azul oscilan entre 0 y 255, con 0 que indica la intensidad mínima y 255 indica la intensidad máxima. En la ilustración siguiente se muestra cómo se pueden combinar los colores primarios rojo, verde y azul para generar cuatro colores adicionales. (En el caso de los dispositivos de visualización, el color negro se produce cuando los valores rojo, verde y azul están establecidos en 0. En la tecnología de visualización, el negro es la ausencia de todos los colores).

![círculos rojos, verdes y azules superpuestos](images/rgbcolormodel.png)

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



 

El sistema almacena los colores internos como valores RGB de 32 bits que tienen la siguiente forma hexadecimal: 0x00bbggrr.

El byte de orden bajo contiene un valor para la intensidad relativa de rojo; el segundo byte contiene un valor para verde; y el tercer byte contiene un valor para azul. El byte de orden superior debe ser cero.

Puede usar la [**macro RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) para obtener un valor RGB basado en las intensidades especificadas para los componentes rojo, verde y azul. Use las macros [**GetRValue,**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue) [**GetBValue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue)y [**GetGValue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue) para extraer colores individuales de un valor de color RGB.

### <a name="hsl-color-model"></a>Modelo de color HSL

El cuadro de diálogo Color proporciona controles para especificar valores HSL. En la ilustración siguiente se muestra el control de espectro de color y el control de diapositiva de luminosidad que aparecen en el cuadro de diálogo Color. En la ilustración también se muestran los intervalos de valores que el usuario puede especificar con estos controles.

![espectro de colores y escala de luminosidad](images/colordialogranges.png)

En el cuadro de diálogo Color, los valores de saturación y luminosidad deben estar en el intervalo de 0 a 240 y el valor de matiz debe estar en el intervalo de 0 a 239.

### <a name="converting-hsl-values-to-rgb-values"></a>Convertir valores HSL en valores RGB

El procedimiento de cuadro de diálogo Comdlg32.dll para el cuadro de diálogo Color contiene código que convierte los valores HSL en los valores RGB correspondientes. En la tabla siguiente se enumeran ocho colores del modelo RGB y sus valores HSL y RGB asociados.



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



 

 

 
