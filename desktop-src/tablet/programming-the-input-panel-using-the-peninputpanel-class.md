---
description: Descripción del uso del objeto PenInputPanel para programar el panel de entrada de Tablet PC de nivel de sistema.
ms.assetid: f83c7709-86dc-4c64-ad17-2ad660eb57b7
title: Programar el panel de entrada mediante la clase PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d430b002fb967652aea046919ec7341a984f420f756fd936e8c68dbfce8c055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449394"
---
# <a name="programming-the-input-panel-using-the-peninputpanel-class"></a>Programar el panel de entrada mediante la clase PenInputPanel

\[[**PenInputPanel**](peninputpanel-class.md) se ha reemplazado por [Microsoft.Ink.TextInput](/previous-versions/ms581554(v=vs.100)). Consulte Programar el [panel de entrada de texto](programming-the-text-input-panel.md).\]

Descripción del uso del [**objeto PenInputPanel**](peninputpanel-class.md) para programar el panel de entrada de Tablet PC de nivel de sistema.

## <a name="input-panel-vs-the-peninputpanel-object"></a>Panel de entrada frente al objeto PenInputPanel

En la versión 1.0 de Microsoft Windows XP Tablet PC Edition, el panel de entrada de Tablet PC de nivel de sistema proporciona un mecanismo universal para realizar la entrada de texto en la plataforma Windows, pero no proporciona acceso mediante programación. En Windows XP Tablet PC Edition Software Development Kit (SDK) versión 1.5 y posteriores, el objeto [**PenInputPanel**](peninputpanel-class.md) permite integrar las herramientas de entrada de texto directamente en las aplicaciones y proporcionar un nivel de control que no estaba disponible previamente. A partir de Windows XP Tablet PC Edition 2005, el Panel de entrada de nivel de sistema se ha actualizado para incluir la funcionalidad de entrada local proporcionada por el objeto **PenInputPanel** y mucho más.

En el gráfico siguiente se muestra el panel de entrada que se muestra sobre el [ejemplo de ejemplo de formulario de notificaciones](auto-claims-form-sample.md) automáticas.

![Panel de entrada mostrado sobre un formulario usado para notificaciones de automóviles](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

El Panel de entrada reemplaza a [**PenInputPanel**](peninputpanel-class.md) al proporcionar la misma funcionalidad de entrada local a cualquier aplicación que se ejecute en Windows XP Tablet PC Edition 2005 o posterior sin necesidad de código adicional. Este artículo sobre el uso del **objeto PenInputPanel** se proporciona por compatibilidad con versiones anteriores. Las aplicaciones que ya usan el objeto **PenInputPanel** funcionarán igual, salvo que se mostrará el Panel de entrada en lugar de **PenInputPanel** cuando la aplicación se ejecute en Windows XP Tablet PC Edition 2005 o posterior.

Si va a desarrollar una nueva aplicación para tablet PC y desea tener una solución de entrada de usuario local, el Panel de entrada lo proporciona automáticamente en Windows XP Tablet PC Edition 2005 o posterior. No es necesario crear una instancia del [**objeto PenInputPanel.**](peninputpanel-class.md)

## <a name="disabling-the-input-panel"></a>Deshabilitar el panel de entrada

Puede haber casos en los que quiera deshabilitar el Panel de entrada. Hay dos maneras de lograrlo. Puede hacerlo mediante programación o estableciendo una entrada del Registro que deshabilite el Panel de entrada para toda la aplicación.

### <a name="disabling-input-panel-programmatically"></a>Deshabilitar el panel de entrada mediante programación

Para deshabilitar el Panel de entrada mediante programación, cree una instancia de [**PenInputPanel**](peninputpanel-class.md) y establezca su [**propiedad AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) en **False.**


```C++
using Microsoft.Ink;

// ...

private PenInputPanel theInputPanel;

// ...

private void Form1_Load(object sender, System.EventArgs e)
{
// Attach the Input Panel to a specific TextBox control.
theInputPanel = new PenInputPanel(textBox1);

// Disable the Input Panel for the TextBox.
theInputPanel.AutoShow = false;
}
```



Para deshabilitar el Panel de entrada para varios controles en una sola aplicación, cree una instancia de un objeto [**PenInputPanel**](peninputpanel-class.md) para cada control y establezca la propiedad [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)en **False** para cada uno o cree una instancia de un único **PenInputPanel** y muévolo del control al control a medida que cambia el foco de entrada. Para obtener más información sobre estas dos técnicas, vea el [tema Ejemplo PenInputPanel.](peninputpanel-sample.md)

### <a name="disabling-input-panel-through-the-registry"></a>Deshabilitar el panel de entrada a través del Registro

Puede establecer una entrada del Registro para deshabilitar el Panel de entrada para toda la aplicación. Sin embargo, esto también lo deshabilitará  para cuadros de  diálogo comunes, como el cuadro de diálogo Abrir archivo, el cuadro de diálogo Imprimir y el **cuadro** de diálogo Guardar archivo . Esto puede hacer que la experiencia del usuario en la aplicación sea incoherente con otras aplicaciones de Tablet PC.

Establecer la clave del Registro en cero impide que la interfaz de usuario (UI) del Panel de entrada `DisableInPlace` aparezca en una aplicación. Debe colocar la clave `DisableInPlace` del Registro en `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\` . A continuación, agregue un nuevo valor del Registro mediante la ruta de acceso completa de la aplicación en la que desea deshabilitar el Panel de entrada. La entrada del Registro de ejemplo siguiente deshabilita el Panel de entrada en una aplicación denominada MyApp:

`[HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\WindowsNT\TabletTIP\DisableInPlace]``"C:\Program Files\My App\MyApp.exe"=dword:00000000`

Si sigue teniendo un problema en la aplicación después de deshabilitar la interfaz de usuario del Panel de entrada, puede que sea necesario deshabilitar el marco subyacente, que consulta la aplicación para la ubicación del caret. Por ejemplo, el Panel de entrada puede exponer un error en el código de seguimiento del carácter de referencia de la aplicación. Al desactivar la consulta de seguimiento del carácter de diálogo, también se impide que aparezca la interfaz de usuario del Panel de entrada. Para deshabilitar el marco de trabajo, establezca la `EnableCaretTracking` clave del Registro en cero. Busque esta clave en `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\` .

> [!Note]  
> Las herramientas de accesibilidad y la tecnología de voz de Windows XP también usan este marco, por lo que deshabilitar la consulta también deshabilita estas características en la aplicación.

 

## <a name="the-input-panel-and-web-pages"></a>El panel de entrada y las páginas web

Para usar una API en una página web, debe funcionar en un entorno de confianza parcial. Todos los miembros de la clase [**PenInputPanel**](peninputpanel-class.md) requieren plena confianza, excepto lo siguiente:

-   [Constructores PenInputPanel](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90)) (solo código administrado)
-   [Método Dispose](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (solo código administrado)
-   [Propiedad AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (solo código administrado)
-   [**Propiedad AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)

Estas API funcionan en un entorno de confianza parcial, como una página web, lo que permite crear instancias de un objeto [**PenInputPanel,**](peninputpanel-class.md) adjuntarlo a un control y deshabilitar el Panel de entrada para ese control. Para obtener más información, vea Programming the Input Panel Using the PenInputPanel Class and Ink on the Web (Programación del panel de entrada mediante la clase PenInputPanel [y Ink en la web).](ink-on-the-web.md)

## <a name="the-peninputpanel-object"></a>El objeto PenInputPanel

En el resto de este tema se describe cómo usar el [**objeto PenInputPanel**](peninputpanel-class.md) en las aplicaciones habilitadas para Tablet PC. Más concretamente, este tema hace referencia al objeto **PenInputPanel** al analizar el objeto de programación, el panel de entrada del lápiz al hacer referencia al elemento de la interfaz de usuario y el panel de entrada de PC (o panel de entrada) cuando se hace referencia al panel de entrada global que se encuentra normalmente en el lado de la pantalla tablet PC.

En las secciones siguientes se describen el [**objeto PenInputPanel**](peninputpanel-class.md) y la interfaz de usuario.

-   [Acerca del panel de entrada](about-the-input-panel.md)
-   [Creación de instancias de la clase PenInputPanel](instantiating-the-peninputpanel-class.md)
-   [Compatibilidad con Factoid](factoid-support.md)
-   [Text Services Framework (TSF)](text-services-framework.md)
-   [Procedimientos recomendados](best-practices.md)

 

 
