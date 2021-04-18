---
description: Más información acerca de cómo establecer el reconocimiento de PPP predeterminado para un proceso
title: Establecer el reconocimiento de PPP predeterminado para un proceso (Windows)
TOCTitle: Setting the default DPI awareness for a process
ms:assetid: C9488338-D863-45DF-B5CB-7ED9B869A5E2
ms:mtpsurl: https://msdn.microsoft.com/library/Mt846517(v=VS.85)
ms:contentKeyID: 74520139
ms.date: 03/30/2018
ms.topic: article
mtps_version: v=VS.85
ms.openlocfilehash: ff869974e6d9aa2eec2b3251832c061d7b6826da
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721388"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a>Establecer el reconocimiento de PPP predeterminado para un proceso

Las aplicaciones de escritorio en Windows se pueden ejecutar en diferentes modos de reconocimiento de PPP. Estos modos permiten un comportamiento de escalado de PPP distinto y pueden usar diferentes espacios de coordenadas. Para obtener más información sobre el reconocimiento de PPP, consulte [desarrollo de aplicaciones de escritorio de PPP alta en Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\)) Es importante que establezca explícitamente el modo de reconocimiento de PPP predeterminado del proceso para evitar un comportamiento inesperado.

Hay dos métodos principales para especificar el reconocimiento de PPP predeterminado de un proceso:

1 \) a través de una configuración de manifiesto de aplicación

2 mediante \) programación a través de una llamada API

Se recomienda especificar el reconocimiento de PPP de proceso predeterminado a través de un valor de manifiesto. Aunque se admite la especificación de la API Via predeterminada, no se recomienda.

## <a name="setting-default-awareness-with-the-application-manifest"></a>Establecer el reconocimiento predeterminado con el manifiesto de aplicación

Hay dos configuraciones de manifiesto que le permiten especificar el modo de reconocimiento de PPP predeterminado del proceso: \<dpiAwareness\> y \<dpiAware\> . \<dpiAware\> se presentó en Windows Vista y solo permite que el proceso predeterminado se establezca en reconocimiento del sistema. \<dpiAwareness\> se presentó en la versión 1607 de Windows 10 y permite especificar una lista ordenada de los modos de reconocimiento de PPP predeterminados del proceso. Esto le permite establecer los modos de reconocimiento de PPP de copia de seguridad, que se usarán si la aplicación se ejecuta en una versión de Windows que no sea compatible con el primer modo de reconocimiento especificado. En versiones anteriores de Windows, se \<dpiAwareness\> omitirá la etiqueta más reciente. Esto significa que puede usar ambos valores del manifiesto para habilitar un escenario en el que el proceso predeterminado podría ser el reconocimiento del sistema en una versión anterior de Windows mientras se Per-Monitor en versiones posteriores a Windows 10, versión 1607. En Windows 10, versión 1607 y en, el \<dpiAware\> valor se omite si el \<dpiAwareness\> elemento está presente.

En la tabla siguiente se muestra cómo especificar los diferentes modos de reconocimiento de PPP predeterminados del proceso mediante los dos valores del manifiesto:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Modo de reconocimiento de PPP predeterminado del proceso</th>
<th>&lt;configuración de dpiAware &gt;</th>
<th>&lt;&gt;configuración de dpiAwareness (Windows 10, versión 1607 y versiones posteriores)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>consciente</td>
<td><p>N/A (no hay ningún valor de dpiAware en el manifiesto)</p>
<p>or</p>
<p>&lt;dpiAware &gt; false &lt; /dpiAware&gt;</p></td>
<td>&lt;dpiAwareness no &gt; compatible &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="even">
<td>Compatible con el sistema</td>
<td>&lt;dpiAware &gt; true &lt; /dpiAware&gt;</td>
<td>&lt;dpiAwareness &gt; del sistema &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="odd">
<td>Por monitor</td>
<td>&lt;dpiAware &gt; true/PM &lt; dpiAware&gt;</td>
<td>&lt;dpiAwareness &gt; permonitor &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="even">
<td>Por monitor V2</td>
<td>No compatible</td>
<td>&lt;dpiAwareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt;</td>
</tr>
</tbody>
</table>

 

En el ejemplo siguiente se muestra el \<dpiAwareness\> y la \<dpiAware\> configuración que se usa en el mismo archivo de manifiesto para configurar el comportamiento de reconocimiento de PPP de proceso predeterminado para diferentes versiones de Windows.

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
  <asmv3:application>
    <asmv3:windowsSettings>
      <dpiAware xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">true</dpiAware>
      <dpiAwareness xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">PerMonitorV2</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

## <a name="setting-default-awareness-programmatically"></a>Establecer el reconocimiento predeterminado mediante programación

Aunque no se recomienda, es posible establecer el reconocimiento de PPP predeterminado mediante programación. Una vez que se ha creado una ventana (HWND) en el proceso, ya no se admite el cambio del modo de reconocimiento de PPP. Si está configurando el modo de reconocimiento de PPP predeterminado del proceso mediante programación, debe llamar a la API correspondiente antes de que se haya creado cualquier HWND.

Hay varias API que permiten especificar el reconocimiento de PPP predeterminado para el proceso. La API recomendada actual es [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), ya que las API anteriores ofrecen menos funcionalidad.

 

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>API</th>
<th>Versión mínima de Windows</th>
<th>PPP no compatible</th>
<th>Reconocimiento de PPP del sistema</th>
<th>Con reconocimiento de PPP por monitor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDpiAware</a></td>
<td>Windows Vista</td>
<td>N/D</td>
<td>SetProcessDpiAware()</td>
<td>N/D</td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></td>
<td>Windows 8.1</td>
<td>SetProcessDpiAwareness (PROCESS_DPI_UNAWARE)</td>
<td>SetProcessDpiAwareness (PROCESS_DPI_SYSTEM_DPI_AWARE)</td>
<td>SetProcessDpiAwareness (PROCESS_DPI_PER_MONITOR_DPI_AWARE)</td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></td>
<td>Windows 10, versión 1607</td>
<td>SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_UNAWARE)</td>
<td>SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</td>
<td><p>SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</p>
<p>SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a>Proceso: predeterminado frente a subproceso predeterminado

Este documento hace referencia a la configuración del reconocimiento de PPP predeterminado para el proceso. Esto se debe a que Windows 10 incorporó compatibilidad para ejecutar más de un modo de reconocimiento de PPP en un único proceso (antes de Windows 10, todo el proceso tuvo que ajustarse a un único modo de reconocimiento de PPP). La compatibilidad con la ejecución de más de un modo de reconocimiento de PPP dentro de un proceso se conoce como "escala de PPP en modo mixto". Al usar el ajuste de PPP en modo mixto dentro del proceso, cada ventana de nivel superior puede ejecutarse en un modo de reconocimiento de PPP que puede ser diferente del valor predeterminado del proceso. A menos que se especifique explícitamente, cada subproceso usará de forma predeterminada el valor predeterminado del proceso cuando se cree. Para obtener más información sobre el escalado de PPP en modo mixto, consulte el artículo sobre el [escalado de PPP en modo mixto](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) .
