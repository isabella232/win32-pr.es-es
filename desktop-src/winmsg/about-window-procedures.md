---
description: Cada ventana es miembro de una clase de ventana determinada. La clase Window determina el procedimiento de ventana predeterminado que usa una ventana individual para procesar sus mensajes.
ms.assetid: 3a8e8f4e-910d-4863-a4a7-dd37c2dfa402
title: Acerca de los procedimientos de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f63586b9ca4ac6fe8486ba112316174533b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697806"
---
# <a name="about-window-procedures"></a>Acerca de los procedimientos de ventana

Cada ventana es miembro de una clase de ventana determinada. La clase Window determina el procedimiento de ventana predeterminado que usa una ventana individual para procesar sus mensajes. Todas las ventanas que pertenecen a la misma clase usan el mismo procedimiento de ventana predeterminado. Por ejemplo, el sistema define un procedimiento de ventana para la clase de cuadro combinado (**ComboBox**); todos los cuadros combinados usan ese procedimiento de ventana.

Normalmente, una aplicación registra al menos una nueva clase de ventana y su procedimiento de ventana asociado. Después de registrar una clase, la aplicación puede crear muchas ventanas de esa clase, que utilizan el mismo procedimiento de ventana. Como esto significa que varios orígenes pueden llamar simultáneamente al mismo fragmento de código, debe tener cuidado al modificar los recursos compartidos desde un procedimiento de ventana. Para obtener más información, vea [clases de ventana](window-classes.md).

Los procedimientos de ventana para los cuadros de diálogo (denominados procedimientos de cuadro de diálogo) tienen una estructura similar y una función como procedimientos de ventana normales. Todos los puntos que hacen referencia a los procedimientos de ventana en esta sección también se aplican a los procedimientos del cuadro de diálogo. Para obtener más información, consulte [cuadros de diálogo](/windows/desktop/dlgbox/dialog-boxes).

En esta sección se tratan los temas siguientes.

-   [Estructura de un procedimiento de ventana](#structure-of-a-window-procedure)
-   [Procedimiento de ventana predeterminado](#default-window-procedure)
-   [Subclases de procedimientos de ventana](#window-procedure-subclassing)
    -   [Subclases de instancia](#instance-subclassing)
    -   [Subclase global](#global-subclassing)
-   [Superclase de procedimientos de ventana](#window-procedure-superclassing)

## <a name="structure-of-a-window-procedure"></a>Estructura de un procedimiento de ventana

Un procedimiento de ventana es una función que tiene cuatro parámetros y devuelve un valor con signo. Los parámetros se componen de un identificador de ventana, un identificador de mensaje **uint** y dos parámetros de mensaje declarados con los tipos de datos **wParam** e **lParam** . Para obtener más información, vea [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).

Los parámetros de mensaje suelen contener información en sus palabras de orden inferior y de orden superior. Hay varias macros que una aplicación puede usar para extraer información de los parámetros del mensaje. Por ejemplo, la macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) extrae la palabra de orden inferior (de bits 0 a 15) de un parámetro de mensaje. Otras macros son [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85))y [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)).

La interpretación del valor devuelto depende del mensaje determinado. Consulte la descripción de cada mensaje para determinar el valor devuelto adecuado.

Dado que es posible llamar a un procedimiento de ventana de forma recursiva, es importante minimizar el número de variables locales que usa. Al procesar mensajes individuales, una aplicación debe llamar a funciones fuera del procedimiento de ventana para evitar el uso excesivo de variables locales, lo que podría provocar un desbordamiento de la pila durante la recursividad profunda.

## <a name="default-window-procedure"></a>Procedimiento de ventana predeterminado

La función de procedimiento de ventana predeterminada, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) define cierto comportamiento fundamental compartido por todas las ventanas. El procedimiento de ventana predeterminado proporciona la funcionalidad mínima para una ventana. Un procedimiento de ventana definido por la aplicación debe pasar cualquier mensaje que no procese a la función **DefWindowProc** para el procesamiento predeterminado.

## <a name="window-procedure-subclassing"></a>Subclases de procedimientos de ventana

Cuando una aplicación crea una ventana, el sistema asigna un bloque de memoria para almacenar información específica de la ventana, incluida la dirección del procedimiento de ventana que procesa los mensajes para la ventana. Cuando el sistema necesita pasar un mensaje a la ventana, busca en la información específica de la ventana la dirección del procedimiento de ventana y pasa el mensaje a ese procedimiento.

La *subclase* es una técnica que permite a una aplicación interceptar y procesar los mensajes enviados o publicados en una ventana determinada antes de que la ventana tenga la oportunidad de procesarlos. Mediante la subclase de una ventana, una aplicación puede aumentar, modificar o supervisar el comportamiento de la ventana. Una aplicación puede subclaser una ventana que pertenece a una clase global del sistema, como un control de edición o un cuadro de lista. Por ejemplo, una aplicación podría subclaser un control de edición para evitar que el control acepte determinados caracteres. Sin embargo, no puede subclaser una ventana o clase que pertenezca a otra aplicación. Todas las subclases deben realizarse dentro del mismo proceso.

Una aplicación subclase una ventana reemplazando la dirección del procedimiento de ventana original de la ventana por la dirección de un nuevo procedimiento de ventana, denominado *procedimiento de subclase*. A partir de ese momento, el procedimiento de subclase recibe los mensajes enviados o publicados en la ventana.

El procedimiento de subclase puede tomar tres acciones al recibir un mensaje: puede pasar el mensaje al procedimiento de ventana original, modificar el mensaje y pasarlo al procedimiento de ventana original, o procesar el mensaje y no pasarlo al procedimiento de ventana original. Si el procedimiento de subclase procesa un mensaje, puede hacerlo antes, después o antes y después de pasar el mensaje al procedimiento de ventana original.

El sistema proporciona dos tipos de subclases: [Instance](#instance-subclassing) y [global](#global-subclassing). En las *subclases de instancia*, una aplicación reemplaza la dirección del procedimiento de ventana de una única instancia de una ventana. Una aplicación debe usar la subclase de instancia para subclase de una ventana existente. En la *subclase global*, una aplicación reemplaza la dirección del procedimiento de ventana en la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) de una clase de ventana. Todas las ventanas posteriores creadas con la clase tienen la dirección del procedimiento de subclase, pero las ventanas existentes de la clase no se ven afectadas.

### <a name="instance-subclassing"></a>Subclases de instancia

Una aplicación subclase una instancia de una ventana mediante la función [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) . La aplicación pasa la marca **GWL \_ WndProc** , el identificador a la ventana a la subclase y la dirección del procedimiento de la subclase a **SetWindowLong**. El procedimiento de subclase puede residir en el ejecutable de la aplicación o en un archivo DLL.

[**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) devuelve la dirección del procedimiento de ventana original de la ventana. La aplicación debe guardar la dirección y utilizarla en las llamadas subsiguientes a la función [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) para pasar los mensajes interceptados al procedimiento de ventana original. La aplicación también debe tener la dirección del procedimiento de ventana original para quitar la subclase de la ventana. Para quitar la subclase, la aplicación llama de nuevo a **SetWindowLong** , pasando la dirección del procedimiento de ventana original con la marca **GWL \_ WndProc** y el identificador a la ventana.

El sistema posee las clases globales del sistema y los aspectos de los controles pueden cambiar de una versión del sistema a la siguiente. Si la aplicación debe subclaser una ventana que pertenece a una clase global del sistema, es posible que el desarrollador tenga que actualizar la aplicación cuando se lance una nueva versión del sistema.

Dado que la creación de subclases de instancia se produce después de crear una ventana, no se pueden agregar bytes adicionales a la ventana. Las aplicaciones que subclasen una ventana deben usar la lista de propiedades de la ventana para almacenar los datos necesarios para una instancia de la ventana de la subclase. Para obtener más información, vea propiedades de la [ventana](window-properties.md).

Cuando una aplicación subclase una ventana subclase, debe quitar las subclases en el orden inverso en el que se realizaron. Si no se revierte el orden de eliminación, puede producirse un error irrecuperable en el sistema.

### <a name="global-subclassing"></a>Subclase global

Para subclases globales de una clase de ventana, la aplicación debe tener un identificador a una ventana de la clase. La aplicación también necesita el identificador para quitar la subclase. Para obtener el identificador, una aplicación normalmente crea una ventana oculta de la clase para la que se van a crear subclases. Después de obtener el identificador, la aplicación llama a la función [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) , especificando el identificador, la marca **GCL \_ WndProc** y la dirección del procedimiento de la subclase. **SetClassLong** devuelve la dirección del procedimiento de ventana original para la clase.

La dirección del procedimiento de ventana original se usa en la subclase global de la misma manera que se usa en la subclase de instancia. El procedimiento de subclase pasa los mensajes al procedimiento de ventana original mediante una llamada a [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca). La aplicación quita la subclase de la clase de ventana llamando a [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) de nuevo, especificando la dirección del procedimiento de ventana original, la marca **GCL \_ WndProc** y el identificador de una ventana de la clase que se va a subclase. Una aplicación que subclase globalmente una clase de control debe quitar la subclase cuando la aplicación finaliza; de lo contrario, puede producirse un error irrecuperable en el sistema.

La subclase global tiene las mismas limitaciones que las subclases de instancia, además de algunas restricciones adicionales. Una aplicación no debe utilizar los bytes adicionales para la clase o la instancia de la ventana sin saber exactamente cómo las utiliza el procedimiento de ventana original. Si la aplicación debe asociar datos a una ventana, debe utilizar las propiedades de la ventana.

## <a name="window-procedure-superclassing"></a>Superclase de procedimientos de ventana

La *superclase* es una técnica que permite a una aplicación crear una nueva clase de ventana con la funcionalidad básica de la clase existente, además de mejoras proporcionadas por la aplicación. Una superclase se basa en una clase de ventana existente denominada *clase base*. Con frecuencia, la clase base es una clase de ventana global del sistema, como un control de edición, pero puede ser cualquier clase de ventana.

Una superclase tiene su propio procedimiento de ventana, denominado procedimiento de superclase. El *procedimiento* de la superclase puede llevar a cabo tres acciones al recibir un mensaje: puede pasar el mensaje al procedimiento de ventana original, modificar el mensaje y pasarlo al procedimiento de ventana original, o procesar el mensaje y no pasarlo al procedimiento de ventana original. Si el procedimiento de la superclase procesa un mensaje, puede hacerlo antes, después o antes y después de pasar el mensaje al procedimiento de ventana original.

A diferencia de un procedimiento de subclase, un procedimiento de superclase puede procesar los mensajes de creación de ventanas ([**WM \_ NCCREATE**](wm-nccreate.md), la [**\_ creación de WM**](wm-create.md), etc.), pero también debe pasarlos al procedimiento de ventana de clase base original para que el procedimiento de ventana de clase base pueda realizar su procedimiento de inicialización.

Para repartir una clase de ventana, una aplicación llama primero a la función [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) para recuperar información sobre la clase base. **GetClassInfo** rellena una estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) con los valores de la estructura **WNDCLASS** de la clase base. A continuación, la aplicación copia su propio identificador de instancia en el miembro **hInstance** de la estructura **WNDCLASS** y copia el nombre de la superclase en el miembro **lpszClassName** . Si la clase base tiene un menú, la aplicación debe proporcionar un nuevo menú con los mismos identificadores de menú y copiar el nombre del menú en el miembro **lpszMenuName** . Si el procedimiento de la superclase procesa el mensaje del [**\_ comando de WM**](/windows/desktop/menurc/wm-command) y no lo pasa al procedimiento de ventana de la clase base, el menú no necesita tener identificadores correspondientes. **GetClassInfo** no devuelve el miembro **lpszMenuName**, **lpszClassName** o **hInstance** de la estructura **WNDCLASS** .

Una aplicación también debe establecer el miembro **lpfnWndProc** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) . La función [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) rellena este miembro con la dirección del procedimiento de ventana original para la clase. La aplicación debe guardar esta dirección para pasar mensajes al procedimiento de ventana original y, a continuación, copiar la dirección del procedimiento de la superclase en el miembro **lpfnWndProc** . La aplicación puede, si es necesario, modificar cualquier otro miembro de la estructura **WNDCLASS** . Después de rellenar la estructura **WNDCLASS** , la aplicación registra la superclase pasando la dirección de la estructura a la función [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . La superclase se puede usar para crear ventanas.

Dado que la superclase registra una nueva clase de ventana, una aplicación puede Agregar a los bytes de clase adicionales y a los bytes de ventana adicionales. La superclase no debe utilizar los bytes adicionales originales para la clase base o la ventana por las mismas razones por las que una subclase de instancia o una subclase global no deben utilizarlos. Además, si la aplicación agrega bytes adicionales para su uso en la clase o en la instancia de la ventana, debe hacer referencia a los bytes adicionales en relación con el número de bytes adicionales utilizados por la clase base original. Dado que el número de bytes utilizados por la clase base puede variar de una versión de la clase base a la siguiente, el desplazamiento inicial para los bytes adicionales de la superclase también puede variar de una versión de la clase base a la siguiente.

 

 
