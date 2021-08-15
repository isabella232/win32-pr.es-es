---
title: Acerca de los cursores
description: En este tema se de abordan los cursores estándar.
ms.assetid: 0ca8e51c-1159-47e9-ba3f-5ced0667cadb
keywords:
- resources,cursors
- cursores,about
- cursors,standard
- cursores estándar
- Función SetSystemCursor
- cursors,custom
- cursores personalizados
- cursores, zonas de acceso directo
- cursores, crear
- crear cursores
- cursors,location
- cursors,appearance
- destruir cursores
- duplicación de cursores
- cursor de clase
- confining cursors
- cursores, destruir
- cursores, duplicación
- cursors,class
- cursors,confining
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8d987eb12857779ac85d34cb7e4ff7f3f5ce59ed8a750764c433c88abbccea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735409"
---
# <a name="about-cursors"></a>Acerca de los cursores

Windows proporciona un conjunto de cursores estándar que están disponibles para que cualquier aplicación los use en cualquier momento. Los archivos de encabezado del SDK contienen identificadores para los cursores estándar: los identificadores comienzan con el **prefijo IDC. \_**

Cada cursor estándar tiene asociada una imagen predeterminada correspondiente. El usuario o una aplicación pueden reemplazar la imagen predeterminada asociada a cualquier cursor estándar en cualquier momento. Una aplicación reemplaza una imagen predeterminada mediante la [**función SetSystemCursor.**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor) En la imagen siguiente se muestran varios cursores estándar de Windows Vista:

![cursores estándar, incluidos mano, cuatro flechas más signo, flecha con signo de interrogación, círculo, lápiz](images/cursorsstandard.png)

Una aplicación puede usar la [**función GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) para recuperar la imagen actual de un cursor y puede dibujar el cursor mediante la [**función DrawIconEx.**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) Para dibujar la imagen predeterminada de un cursor estándar, especifique la marca **\_ COMPAT de** DI en la llamada a **DrawIconEx**. Si no especifica la marca **\_ COMPAT de DI,** **DrawIconEx** dibuja el cursor estándar con la imagen especificada por el usuario.

Los cursores personalizados están diseñados para su uso en una aplicación específica y pueden ser cualquier diseño que defina el desarrollador. En la ilustración siguiente se muestran varios cursores personalizados.

![cursores personalizados, entre los que se incluyen la mano, el manzana, el cuello, el reloj de mano, el metrónoma.](images/cursorscustom.png)

Los cursores pueden ser monocromáticos o de color, y estáticos o animados. El tipo de cursor utilizado en un sistema de equipo determinado depende de la presentación del sistema. Las pantallas antiguas, como VGA, no admiten cursores animados o de color. Las nuevas pantallas, cuyos controladores de pantalla usan el motor de mapa de bits independiente del dispositivo (DIB), sí las admiten.

Los cursores y los iconos son similares y se pueden usar indistintamente en muchas situaciones. La única diferencia entre ellos es que una imagen especificada como cursor debe estar en el formato que la pantalla puede admitir. Por ejemplo, un cursor debe ser monocromo para una pantalla VGA.

Esta información general proporciona información sobre los temas siguientes:

-   [El punto de acceso](#the-hot-spot)
-   [El mouse y el cursor](#the-mouse-and-the-cursor)
-   [Creación de cursores](#cursor-creation)
-   [Ubicación y apariencia del cursor](#cursor-location-and-appearance)
-   [Contención de cursores](#cursor-confinement)
-   [Destrucción de cursores](#cursor-destruction)
-   [Duplicación de cursores](#cursor-duplication)
-   [Cursor de clase Window](#the-window-class-cursor)

## <a name="the-hot-spot"></a>El punto de acceso

En el cursor, un  píxel denominado zona activa marca la ubicación exacta de la pantalla afectada por un evento del mouse, como hacer clic en un botón del mouse. Normalmente, la zona de acceso es el punto focal del cursor. El sistema realiza un seguimiento de este punto y lo reconoce como la posición del cursor. Por ejemplo, las zonas activas típicas son el píxel situado en la punta de un cursor con forma de flecha y el píxel en medio de un cursor con forma de cruz. En las imágenes siguientes se muestran dos cursores de un programa de dibujo, en los que las zonas de acceso activo se asocian con la punta del pincel y el cruz de laza de pintura.

![zonas de acceso directo en dos cursores](images/cursorhotspot.png)

Cuando se produce un evento de entrada del mouse, el controlador del mouse traduce el evento en un mensaje de mouse adecuado que incluye las coordenadas de la zona de acceso. El sistema envía el mensaje del mouse a la ventana que contiene la zona activa o a la ventana que captura la entrada del mouse. Para obtener más información, vea [Mouse Input](/windows/desktop/inputdev/mouse-input).

## <a name="the-mouse-and-the-cursor"></a>El mouse y el cursor

El sistema refleja el movimiento del mouse moviendo el cursor en la pantalla en consecuencia. A medida que el cursor se mueve sobre diferentes partes de ventanas o en ventanas diferentes, el sistema (o una aplicación) cambia la apariencia del cursor. Por ejemplo, cuando el cursor cruza un hipervínculo, el sistema cambia el cursor de una flecha a una mano.

![cambio de cursor estándar a una mano al sobre un hipervínculo](images/cursorchangingstate.png)

Si el sistema no tiene un mouse, el sistema muestra y mueve el cursor solo cuando el usuario elige determinados comandos del sistema, como los que se usan para cambiar el tamaño o mover una ventana. Para proporcionar al usuario un método para mostrar y mover el cursor cuando un mouse no está disponible, una aplicación puede usar las funciones de cursor para simular el movimiento del mouse. Dada esta funcionalidad de simulación, el usuario puede usar las teclas de dirección para mover el cursor.

## <a name="cursor-creation"></a>Creación de cursores

Dado que los cursores estándar están predefinidos, no es necesario crearlos. Para usar un cursor estándar, una aplicación recupera un identificador de cursor mediante la [**función LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) [**o LoadImage.**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) Un *identificador de* cursor es un valor único del tipo **HCURSOR** que identifica un cursor estándar o personalizado.

Para crear un cursor personalizado para una aplicación, normalmente se usa una aplicación de gráficos e se incluye el cursor como un recurso en el archivo de definición de recursos de la aplicación. En tiempo de ejecución, llame [**a LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) para recuperar el identificador del cursor. Los recursos de cursor contienen datos para varios dispositivos de visualización diferentes. La **función LoadCursor** selecciona automáticamente los datos más adecuados para el dispositivo de visualización actual. Para cargar un cursor directamente desde un . CUR o . Archivo ANI, use la [**función LoadCursorFromFile.**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)

También puede crear un cursor personalizado en tiempo de ejecución mediante la función [**CreateIconIndirect,**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) que crea un cursor basado en el contenido de una [**estructura ICONINFO.**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) La [**función GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) rellena esta estructura con coordenadas de punto de acceso dinámico e información sobre la máscara y el color asociados.

Las aplicaciones deben implementar cursores personalizados como recursos y usar [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)o [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) en lugar de crear el cursor en tiempo de ejecución. El uso de recursos de cursor evita la dependencia del dispositivo, simplifica la localización y permite que las aplicaciones compartan diseños de cursor.

La [**función CreateIconFromResourceEx permite**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) a una aplicación crear iconos y cursores basados en datos de recursos. **CreateIconFromResourceEx crea** un cursor basado en datos de recursos binarios a partir de otros archivos ejecutables (.exe) o DLL. Debe ir precedida de llamadas a la [**función LookupIconIdFromDirectoryEx,**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) así como de varias funciones de recursos. **LookupIconIdFromDirectoryEx** identifica los datos de cursor más adecuados para el dispositivo de visualización actual. Para obtener más información sobre las funciones de recursos, vea [Recursos](resources.md).

## <a name="cursor-location-and-appearance"></a>Ubicación y apariencia del cursor

El sistema muestra automáticamente un cursor para el mouse y actualiza su posición en la pantalla. Puede obtener las coordenadas de pantalla actuales del cursor y mover el cursor a cualquier ubicación de la pantalla mediante las funciones [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) y [**SetCursorPos,**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) respectivamente.

También puede recuperar el identificador del cursor actual mediante la función [**GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor) y puede establecer el cursor mediante la [**función SetCursor.**](/windows/desktop/api/Winuser/nf-winuser-setcursor) Después de llamar a **SetCursor,** la apariencia del cursor no cambia hasta que se mueve el mouse, el cursor se establece explícitamente en otro cursor o se ejecuta un comando del sistema.

Cuando el usuario mueve el mouse, el sistema vuelve a dibujar el cursor en la nueva ubicación. El sistema vuelve a dibujar automáticamente el diseño del cursor asociado a la ventana a la que apunta el cursor.

Puede ocultar y volver a mostrar el cursor, sin cambiar el diseño del cursor, mediante la [**función ShowCursor.**](/windows/desktop/api/Winuser/nf-winuser-showcursor) Esta función usa un contador interno para determinar cuándo ocultar o mostrar el cursor. Un intento de mostrar el cursor incrementa el contador; un intento de ocultar el cursor disminuye el contador. El cursor solo es visible si este contador es mayor o igual que cero.

La [**función GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo) obtiene la siguiente información para el cursor global: si el cursor está oculto o se muestra, el identificador del cursor y las coordenadas del cursor.

## <a name="cursor-confinement"></a>Contención de cursores

Puede limitar el cursor a un área rectangular de la pantalla mediante la [**función ClipCursor.**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) Esto resulta útil cuando el usuario debe responder a un evento determinado dentro del área confinada del rectángulo. Por ejemplo, puede usar **ClipCursor** para limitar el cursor a un cuadro de diálogo modal, lo que impide que el usuario interactúe con otras ventanas hasta que se cierre el cuadro de diálogo.

La [**función GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) recupera las coordenadas de pantalla del área rectangular a la que se limita temporalmente el cursor. Cuando sea necesario limitar el cursor, también puede usar esta función para guardar las coordenadas del área original en la que se puede mover el cursor. A continuación, puede restaurar el cursor en el área original cuando la nueva contención ya no sea necesaria.

## <a name="cursor-destruction"></a>Destrucción de cursores

Puede destruir el identificador del cursor y liberar la memoria que usa el cursor llamando a la [**función DestroyCursor.**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) Sin embargo, esta función no tiene ningún efecto en un cursor compartido. Un cursor compartido es válido siempre y cuando el módulo desde el que se cargó permanezca en la memoria. Las siguientes funciones obtienen un cursor compartido:

-   [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)
-   [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)
-   [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) (si usa la **marca LR \_ SHARED)**
-   [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) (si usa la marca **\_ COPYRETURNORG LR** y *hImage* es un cursor compartido)

Cuando ya no necesite un cursor creado mediante la [**función CreateIconIndirect,**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) debe destruir el cursor. La [**función DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) destruye el identificador del cursor y libera la memoria que usa el cursor. Use esta función solo en cursores creados con **CreateIconIndirect**.

## <a name="cursor-duplication"></a>Duplicación de cursores

La [**función CopyCursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor) copia un identificador de cursor. Esto permite que la aplicación o el código DLL recuperen el identificador de un cursor propiedad de otro módulo. A continuación, si se libera el otro módulo, el módulo que copió el cursor puede seguir utilizando el diseño del cursor.

Para obtener información sobre cómo agregar, quitar o reemplazar recursos de cursor en archivos ejecutables, vea [Recursos](resources.md).

## <a name="the-window-class-cursor"></a>Cursor de clase Window

Al registrar una clase de ventana, mediante la [**función RegisterClass,**](/windows/desktop/api/winuser/nf-winuser-registerclassa) puede asignarle un cursor predeterminado, conocido como cursor *de clase*. Una vez que la aplicación registra la clase de ventana, cada ventana de esa clase tiene el cursor de clase especificado.

Para invalidar el cursor de clase, procese [**el \_ mensaje SETCURSOR de WM.**](wm-setcursor.md) También puede reemplazar un cursor de clase mediante la [**función SetClassLong.**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) Esta función cambia la configuración de ventana predeterminada para todas las ventanas de una clase especificada. Para obtener más información, vea [Cursor de clase](/windows/desktop/winmsg/about-window-classes).

 

 