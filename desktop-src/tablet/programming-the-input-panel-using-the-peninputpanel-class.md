---
description: Descripción del uso del objeto PenInputPanel para programar el panel de entrada de Tablet PC en el nivel del sistema.
ms.assetid: f83c7709-86dc-4c64-ad17-2ad660eb57b7
title: Programar el panel de entrada mediante la clase PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e00d1cb10983255ab2e532aa08de6e9e6a0fb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361477"
---
# <a name="programming-the-input-panel-using-the-peninputpanel-class"></a>Programar el panel de entrada mediante la clase PenInputPanel

\[[**PenInputPanel**](peninputpanel-class.md) ha sido reemplazado por [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100)). Consulte [programar el panel de entrada de texto](programming-the-text-input-panel.md).\]

Descripción del uso del objeto [**PenInputPanel**](peninputpanel-class.md) para programar el panel de entrada de Tablet PC en el nivel del sistema.

## <a name="input-panel-vs-the-peninputpanel-object"></a>Panel de entrada frente al objeto PenInputPanel

En la versión 1,0 de Microsoft Windows XP Tablet PC Edition, el panel de entrada de Tablet PC de nivel de sistema proporciona un mecanismo universal para realizar la entrada de texto en la plataforma Windows, pero no proporciona acceso mediante programación. En el kit de desarrollo de software (SDK) de Windows XP Tablet PC Edition, versión 1,5 y versiones posteriores, el objeto [**PenInputPanel**](peninputpanel-class.md) permite integrar herramientas de entrada de texto directamente en las aplicaciones y proporcionar un nivel de control no disponible previamente. A partir de Windows XP Tablet PC Edition 2005, el panel de entrada de nivel de sistema se ha actualizado para incluir la funcionalidad de entrada en contexto proporcionada por el objeto **PenInputPanel** y mucho más.

En el gráfico siguiente se muestra el panel de entrada que se muestra en el ejemplo de [formulario de notificaciones automáticas](auto-claims-form-sample.md) .

![panel de entrada que se muestra en un formulario usado para las notificaciones de automóviles](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

El panel de entrada reemplaza el [**PenInputPanel**](peninputpanel-class.md) proporcionando la misma funcionalidad de entrada en contexto a cualquier aplicación que se ejecute en Windows XP Tablet PC Edition 2005 o posterior sin necesidad de código adicional. Este artículo sobre el uso del objeto **PenInputPanel** se proporciona por motivos de compatibilidad con versiones anteriores. Las aplicaciones que ya usan el objeto **PenInputPanel** funcionarán de la misma forma, salvo que se mostrará el panel de entrada en lugar de **PenInputPanel** cuando la aplicación se ejecute en Windows XP Tablet PC Edition 2005 o posterior.

Si está desarrollando una nueva aplicación para Tablet PC y desea tener una solución de entrada de usuario en contexto, el panel de entrada lo proporciona automáticamente en Windows XP Tablet PC Edition 2005 o posterior. No es necesario crear una instancia del objeto [**PenInputPanel**](peninputpanel-class.md) .

## <a name="disabling-the-input-panel"></a>Deshabilitar el panel de entrada

Puede haber casos en los que desee deshabilitar el panel de entrada. Hay dos maneras de lograrlo. Puede hacerlo mediante programación o mediante el establecimiento de una entrada del registro que deshabilite el panel de entrada para toda la aplicación.

### <a name="disabling-input-panel-programmatically"></a>Deshabilitar el panel de entrada mediante programación

Para deshabilitar el panel de entrada mediante programación, cree una instancia de [**PenInputPanel**](peninputpanel-class.md) y establezca su propiedad [**Autoshow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) en **false**.


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



Para deshabilitar el panel de entrada de varios controles en una sola aplicación, cree una instancia de un objeto [**PenInputPanel**](peninputpanel-class.md) para cada control y establezca la propiedad [**Autoshow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)en **false** para cada una de ellas o cree una instancia de un **PenInputPanel** único y muévala del control al control cuando cambie el foco de entrada. Para obtener más información sobre estas dos técnicas, vea el tema de [ejemplo PenInputPanel](peninputpanel-sample.md) .

### <a name="disabling-input-panel-through-the-registry"></a>Deshabilitar el panel de entrada a través del registro

Puede establecer una entrada del registro para deshabilitar el panel de entrada de toda la aplicación. Sin embargo, esto también lo deshabilitará en los cuadros de diálogo comunes, como el cuadro de diálogo **Abrir archivo** , el cuadro de diálogo **Imprimir** y el cuadro de diálogo **Guardar archivo** . Esto puede hacer que la experiencia del usuario en la aplicación sea incoherente con otras aplicaciones de Tablet PC.

Si se establece la `DisableInPlace` clave del registro en cero, se evita que la interfaz de usuario (UI) del panel de entrada aparezca en una aplicación. Debe colocar la `DisableInPlace` clave del registro en `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\` . A continuación, agregue un nuevo valor del registro mediante la ruta de acceso completa de la aplicación en la que desea deshabilitar el panel de entrada. La siguiente entrada del registro de ejemplo deshabilita el panel de entrada en una aplicación denominada MyApp:

`[HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\WindowsNT\TabletTIP\DisableInPlace]``"C:\Program Files\My App\MyApp.exe"=dword:00000000`

Si sigue viendo un problema en la aplicación después de deshabilitar la interfaz de usuario del panel de entrada, puede que sea necesario deshabilitar el marco subyacente, que consulta la ubicación del símbolo de intercalación en la aplicación. Por ejemplo, el panel de entrada puede exponer un error en el código de seguimiento del símbolo de intercalación de la aplicación. Desactivar la consulta de seguimiento de símbolo de intercalación también evita que aparezca la interfaz de usuario del panel de entrada. Para deshabilitar el marco de trabajo, establezca la `EnableCaretTracking` clave del registro en cero. Busque esta clave en `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\` .

> [!Note]  
> Las herramientas de accesibilidad y la tecnología de voz de Windows XP también usan este marco de trabajo, por lo que al deshabilitar la consulta también se deshabilitan estas características en la aplicación.

 

## <a name="the-input-panel-and-web-pages"></a>Panel de entrada y páginas web

Para usar una API en una página web, debe funcionar en un entorno de confianza parcial. Todos los miembros de clase [**PenInputPanel**](peninputpanel-class.md) requieren plena confianza, excepto los siguientes:

-   [Constructores PenInputPanel](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90)) (solo código administrado)
-   [Método Dispose](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (solo código administrado)
-   [Propiedad AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (solo código administrado)
-   [**Automostrar (propiedad)**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)

Estas API funcionan en un entorno de confianza parcial, como una página web, lo que permite crear una instancia de un objeto [**PenInputPanel**](peninputpanel-class.md) , adjuntarlo a un control y deshabilitar el panel de entrada para ese control. Para obtener más información, vea programar el panel de entrada con la clase PenInputPanel y la [entrada manuscrita en la web](ink-on-the-web.md).

## <a name="the-peninputpanel-object"></a>El objeto PenInputPanel

En el resto de este tema se describe cómo usar el objeto [**PenInputPanel**](peninputpanel-class.md) en las aplicaciones habilitadas para Tablet PC. Más concretamente, en este tema se hace referencia al objeto **PenInputPanel** cuando se analiza el objeto de programación, el panel de entrada del lápiz al hacer referencia al elemento de la interfaz de usuario y el panel de entrada de PC (o panel de entrada) al hacer referencia al panel de entrada global que se encuentra normalmente en el lateral de la pantalla de Tablet PC.

En las secciones siguientes se describe el objeto y la interfaz de usuario de [**PenInputPanel**](peninputpanel-class.md) .

-   [Acerca del panel de entrada](about-the-input-panel.md)
-   [Crear instancias de la clase PenInputPanel](instantiating-the-peninputpanel-class.md)
-   [Compatibilidad con Factoid](factoid-support.md)
-   [Text Services Framework (TSF)](text-services-framework.md)
-   [Procedimientos recomendados](best-practices.md)

 

 
