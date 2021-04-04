---
title: Acerca de los cursores
description: En este tema se describen los cursores estándar.
ms.assetid: 0ca8e51c-1159-47e9-ba3f-5ced0667cadb
keywords:
- recursos, cursores
- cursores, acerca de
- cursores, estándar
- cursores estándar
- SetSystemCursor función)
- cursores, personalizados
- Cursores personalizados
- cursores, zonas activas
- cursores, crear
- crear cursores
- cursores, ubicación
- cursores, apariencia
- destruir cursores
- duplicar cursores
- cursor de clase
- acotar cursores
- cursores, destruir
- cursores, duplicación
- cursores, clase
- cursores, restringir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2d0b91ba4670d2510413240efd742b2e0ba69b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077707"
---
# <a name="about-cursors"></a>Acerca de los cursores

Windows proporciona un conjunto de cursores estándar que se pueden usar en cualquier aplicación en cualquier momento. Los archivos de encabezado del SDK contienen identificadores para los cursores estándar: los identificadores comienzan con el prefijo **IDC \_** .

Cada cursor estándar tiene asociada una imagen predeterminada correspondiente. El usuario o una aplicación pueden reemplazar la imagen predeterminada asociada con cualquier cursor estándar en cualquier momento. Una aplicación reemplaza una imagen predeterminada mediante la función [**SetSystemCursor**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor) . En la imagen siguiente se muestran varios cursores estándar de Windows Vista:

![cursores estándar, como mano, cuatro flechas signo más, flecha con signo de interrogación, círculo, lápiz](images/cursorsstandard.png)

Una aplicación puede usar la función [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) para recuperar la imagen actual de un cursor y puede dibujar el cursor mediante la función [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) . Para dibujar la imagen predeterminada de un cursor estándar, especifique la marca de la **\_ compatibilidad con di** en la llamada a **DrawIconEx**. Si no especifica la marca de **la \_ compatibilidad con di** , **DrawIconEx** dibuja el cursor estándar mediante la imagen especificada por el usuario.

Los cursores personalizados están diseñados para su uso en una aplicación específica y pueden ser cualquier diseño que defina el desarrollador. En la ilustración siguiente se muestran varios cursores personalizados.

![Cursores personalizados, como Hand, banana, tambor, pulsera a mano, metrónomo](images/cursorscustom.png)

Los cursores pueden ser monocromáticos o de color, y estáticos o animados. El tipo de cursor que se usa en un equipo determinado depende de la pantalla del sistema. Las pantallas antiguas, como VGA, no admiten el color o los cursores animados. Nuevas pantallas, cuyos controladores de pantalla usan el motor de mapa de bits independiente del dispositivo (DIB), las admiten.

Los cursores y los iconos son similares y se pueden usar indistintamente en muchas situaciones. La única diferencia entre ellos es que una imagen especificada como cursor debe estar en el formato admitido por la pantalla. Por ejemplo, un cursor debe ser monocromo para una pantalla VGA.

En esta información general se proporciona información sobre los temas siguientes:

-   [La zona activa](#the-hot-spot)
-   [El mouse y el cursor](#the-mouse-and-the-cursor)
-   [Creación de cursores](#cursor-creation)
-   [Ubicación y apariencia del cursor](#cursor-location-and-appearance)
-   [Confinamiento de cursor](#cursor-confinement)
-   [Destrucción de cursor](#cursor-destruction)
-   [Duplicación de cursores](#cursor-duplication)
-   [Cursor de clase de ventana](#the-window-class-cursor)

## <a name="the-hot-spot"></a>La zona activa

En el cursor, un píxel denominado *zona activa* marca la ubicación de pantalla exacta afectada por un evento del mouse, como hacer clic en un botón del mouse. Normalmente, la zona activa es el punto focal del cursor. El sistema realiza un seguimiento y reconoce este punto como la posición del cursor. Por ejemplo, las zonas activas típicas son el píxel en la punta de un cursor en forma de flecha y el píxel en medio de un cursor en forma de Cruz. En las siguientes imágenes se muestran dos cursores de un programa de dibujo, en los que las zonas activas están asociadas a la punta del pincel y la Cruz de la pintura puede.

![zonas activas en dos cursores](images/cursorhotspot.png)

Cuando se produce un evento de entrada del mouse, el controlador de mouse convierte el evento en un mensaje de mouse adecuado que incluye las coordenadas de la zona activa. El sistema envía el mensaje del mouse a la ventana que contiene la zona activa o a la ventana que está capturando la entrada del mouse. Para obtener más información, vea [entrada del mouse](/windows/desktop/inputdev/mouse-input).

## <a name="the-mouse-and-the-cursor"></a>El mouse y el cursor

El sistema refleja el movimiento del mouse moviendo el cursor en la pantalla en consecuencia. Cuando el cursor se mueve sobre distintas partes de Windows o en diferentes ventanas, el sistema (o una aplicación) cambia la apariencia del cursor. Por ejemplo, cuando el cursor cruza sobre un hipervínculo, el sistema cambia el cursor de una flecha a una mano.

![cambio de cursor estándar a mano cuando se encuentra sobre un hipervínculo](images/cursorchangingstate.png)

Si el sistema no tiene un mouse, el sistema muestra y mueve el cursor solo cuando el usuario elige determinados comandos del sistema, como los que se usan para cambiar el tamaño o mover una ventana. Para proporcionar al usuario un método para mostrar y mover el cursor cuando no está disponible un mouse, una aplicación puede usar las funciones de cursor para simular el movimiento del mouse. Dada esta capacidad de simulación, el usuario puede utilizar las teclas de dirección para desplace el cursor.

## <a name="cursor-creation"></a>Creación de cursores

Dado que los cursores estándar están predefinidos, no es necesario crearlos. Para usar un cursor estándar, una aplicación recupera un identificador de cursor mediante la función [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) o [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) . Un *identificador de cursor* es un valor único del tipo **HCURSOR** que identifica un cursor estándar o personalizado.

Para crear un cursor personalizado para una aplicación, normalmente se usa una aplicación de gráficos e incluye el cursor como un recurso en el archivo de definición de recursos de la aplicación. En tiempo de ejecución, llame a [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) para recuperar el identificador de cursor. Los recursos de cursor contienen datos para varios dispositivos de pantalla diferentes. La función **LoadCursor** selecciona automáticamente los datos más apropiados para el dispositivo de pantalla actual. Para cargar un cursor directamente desde un. CUR o. ANI, utilice la función [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea) .

También puede crear un cursor personalizado en tiempo de ejecución mediante la función [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , que crea un cursor basado en el contenido de una estructura [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) . La función [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) llena esta estructura con coordenadas de zona activa e información relativa a la máscara y el color asociados.

Las aplicaciones deben implementar cursores personalizados como recursos y usar [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)o [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) en lugar de crear el cursor en tiempo de ejecución. El uso de recursos de cursor evita la dependencia del dispositivo, simplifica la localización y permite que las aplicaciones compartan diseños de cursores.

La función [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) permite a una aplicación crear iconos y cursores basados en los datos de recursos. **CreateIconFromResourceEx** crea un cursor basado en datos de recursos binarios de otros archivos ejecutables (. exe) o dll. Debe ir precedida de llamadas a la función [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) , así como de varias funciones de recursos. **LookupIconIdFromDirectoryEx** identifica los datos de cursor más adecuados para el dispositivo de pantalla actual. Para obtener más información sobre las funciones de recursos, vea [recursos](resources.md).

## <a name="cursor-location-and-appearance"></a>Ubicación y apariencia del cursor

El sistema muestra automáticamente un cursor para el mouse y actualiza su posición en la pantalla. Puede obtener las coordenadas de pantalla actuales del cursor y desplace el cursor a cualquier ubicación de la pantalla mediante las funciones [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) y [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) , respectivamente.

También puede recuperar el identificador del cursor actual mediante la función [**GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor) , y puede establecer el cursor mediante la función [**setCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) . Después de llamar a **setCursor**, la apariencia del cursor no cambia hasta que se mueve el mouse, el cursor se establece explícitamente en un cursor diferente o se ejecuta un comando del sistema.

Cuando el usuario mueve el mouse, el sistema vuelve a dibujar el cursor en la nueva ubicación. El sistema vuelve a dibujar automáticamente el diseño del cursor asociado a la ventana a la que apunta el cursor.

Puede ocultar y volver a mostrar el cursor sin cambiar el diseño del cursor mediante la función [**ShowCursor**](/windows/desktop/api/Winuser/nf-winuser-showcursor) . Esta función usa un contador interno para determinar cuándo se debe ocultar o mostrar el cursor. Un intento de mostrar el cursor incrementa el contador. un intento de ocultar el cursor disminuye el contador. El cursor solo es visible si este contador es mayor o igual que cero.

La función [**GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo) obtiene la información siguiente para el cursor global: Si el cursor está oculto o se muestra, el identificador del cursor y las coordenadas del cursor.

## <a name="cursor-confinement"></a>Confinamiento de cursor

Puede limitar el cursor a un área rectangular en la pantalla mediante la función [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) . Esto resulta útil cuando el usuario debe responder a un evento determinado dentro del área confinada del rectángulo. Por ejemplo, puede usar **ClipCursor** para limitar el cursor a un cuadro de diálogo modal, lo que impide que el usuario interactúe con otras ventanas hasta que se cierre el cuadro de diálogo.

La función [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) recupera las coordenadas de pantalla del área rectangular en la que el cursor se ha limitado temporalmente. Cuando sea necesario limitar el cursor, también puede usar esta función para guardar las coordenadas del área original en la que se puede desplace el cursor. Después, puede restaurar el cursor en el área original cuando el nuevo confinador ya no es necesario.

## <a name="cursor-destruction"></a>Destrucción de cursor

Puede destruir el identificador de cursor y liberar la memoria que usa el cursor llamando a la función [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) . Sin embargo, esta función no tiene ningún efecto en un cursor compartido. Un cursor compartido es válido siempre y cuando el módulo desde el que se cargó permanezca en la memoria. Las siguientes funciones obtienen un cursor compartido:

-   [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)
-   [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)
-   [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) (si se usa la marca de **\_ recurso compartido LR** )
-   [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) (si usa la marca **LR \_ COPYRETURNORG** y *hImage* es un cursor compartido)

Cuando ya no necesite un cursor que haya creado con la función [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , debe destruir el cursor. La función [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) destruye el identificador de cursor y libera cualquier memoria que use el cursor. Use esta función solo en cursores creados con **CreateIconIndirect**.

## <a name="cursor-duplication"></a>Duplicación de cursores

La función [**CopyCursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor) copia un identificador de cursor. Esto permite que el código de aplicación o DLL recupere el identificador de un cursor propiedad de otro módulo. Después, si se libera el otro módulo, el módulo que copió el cursor todavía puede usar el diseño del cursor.

Para obtener información sobre cómo agregar, quitar o reemplazar recursos de cursor en archivos ejecutables, vea [recursos](resources.md).

## <a name="the-window-class-cursor"></a>Cursor de clase de ventana

Al registrar una clase de ventana, mediante la función [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) , puede asignarle un cursor predeterminado, conocido como el *cursor de clase*. Una vez que la aplicación registra la clase de ventana, cada ventana de esa clase tiene el cursor de clase especificado.

Para invalidar el cursor de clase, procese el mensaje de [**\_ SETCURSOR de WM**](wm-setcursor.md) . También puede reemplazar un cursor de clase mediante la función [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) . Esta función cambia la configuración de ventana predeterminada para todas las ventanas de una clase especificada. Para obtener más información, vea [cursor de clase](/windows/desktop/winmsg/about-window-classes).

 

 