---
description: 'Más información sobre: Establecimiento del reconocimiento de PPP predeterminado para un proceso'
title: Establecimiento del reconocimiento de PPP predeterminado para un proceso (Windows)
TOCTitle: Setting the default DPI awareness for a process
ms:assetid: C9488338-D863-45DF-B5CB-7ED9B869A5E2
ms:mtpsurl: https://msdn.microsoft.com/library/Mt846517(v=VS.85)
ms:contentKeyID: 74520139
ms.date: 03/30/2018
ms.topic: article
mtps_version: v=VS.85
ms.openlocfilehash: c9192bf650588b7c21f17afb45149fe460f91bea
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481870"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a>Establecimiento del reconocimiento de PPP predeterminado para un proceso

Las aplicaciones de escritorio Windows pueden ejecutarse en diferentes modos de reconocimiento de PPP. Estos modos permiten un comportamiento de escalado de PPP diferente y pueden usar distintos espacios de coordenadas. Para obtener más información sobre el reconocimiento de PPP, consulte [High PPP Desktop Application Development on Windows(Desarrollo de](https://msdn.microsoft.com/library/mt843498\(v=vs.85\)) aplicaciones de escritorio con valores altos de PPP en Windows). Es importante que establezca explícitamente el modo de reconocimiento de PPP predeterminado del proceso para evitar un comportamiento inesperado.

Hay dos métodos principales para especificar el reconocimiento de PPP predeterminado de un proceso:

1 a \) través de una configuración de manifiesto de aplicación

2 \) mediante programación a través de una llamada API

Se recomienda especificar el reconocimiento de PPP del proceso predeterminado a través de una configuración de manifiesto. Aunque se admite la especificación del valor predeterminado a través de la API, no se recomienda.

## <a name="setting-default-awareness-with-the-application-manifest"></a>Establecimiento del reconocimiento predeterminado con el manifiesto de aplicación

Hay dos configuraciones de manifiesto que permiten especificar el modo de reconocimiento de PPP predeterminado del proceso: \<dpiAwareness\> y \<dpiAware\> . \<dpiAware\>se introdujo en Windows Vista y solo permite que el proceso predeterminado se establezca en el reconocimiento del sistema. \<dpiAwareness\>se introdujo en Windows 10 versión 1607 y permite especificar una lista ordenada de modos de reconocimiento de PPP predeterminados del proceso. Esto le permite establecer modos de reconocimiento de PPP de copia de seguridad, que se usarán si la aplicación se ejecuta en una versión de Windows no puede admitir el primer modo de reconocimiento especificado. En versiones anteriores de Windows, se omitirá la \<dpiAwareness\> etiqueta más reciente. Esto significa que puede usar ambas opciones de configuración de manifiesto para habilitar un escenario en el que el proceso predeterminado podría ser el reconocimiento del sistema en la versión anterior de Windows mientras se usa Per-Monitor en versiones superiores a Windows 10, versión 1607. En Windows 10, versión 1607 y en, la configuración se omite \<dpiAware\> si el elemento está \<dpiAwareness\> presente.

En la tabla siguiente se muestra cómo especificar diferentes modos de reconocimiento de PPP predeterminados del proceso mediante las dos configuraciones de manifiesto:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Modo de reconocimiento de PPP predeterminado del proceso</th>
<th>&lt;configuración de &gt; pppAware</th>
<th>&lt;configuración de pppAwareness &gt; (Windows 10 versión 1607 y posteriores)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Conscientes</td>
<td><p>N/A (sin configuración de pppAware en el manifiesto)</p>
<p>o</p>
<p>&lt;dpiAware &gt; false &lt; /dpiAware&gt;</p></td>
<td>&lt;pppAwareness &gt; unware &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="even">
<td>Con constancia del sistema</td>
<td>&lt;dpiAware &gt; true &lt; /dpiAware&gt;</td>
<td>&lt;dpiAwareness &gt; system &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="odd">
<td>Por monitor</td>
<td>&lt;pppAware &gt; true/pm &lt; pppAware&gt;</td>
<td>&lt;pppAwareness &gt; PerMonitor &lt; /pppAwareness&gt;</td>
</tr>
<tr class="even">
<td>Por monitor V2</td>
<td>No compatible</td>
<td>&lt;pppAwareness &gt; PerMonitorV2 &lt; /pppAwareness&gt;</td>
</tr>
</tbody>
</table>

 

En el ejemplo siguiente se muestra y la configuración que se usa en el mismo archivo de manifiesto para configurar el comportamiento de reconocimiento de PPP predeterminado del proceso para las distintas \<dpiAwareness\> \<dpiAware\> versiones de Windows.

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

## <a name="setting-default-awareness-programmatically"></a>Establecimiento del reconocimiento predeterminado mediante programación

Aunque no se recomienda, es posible establecer el reconocimiento de PPP predeterminado mediante programación. Una vez que se ha creado una ventana (un HWND) en el proceso, ya no se admite el cambio del modo de reconocimiento de PPP. Si está estableciendo el modo de reconocimiento de PPP predeterminado del proceso mediante programación, debe llamar a la API correspondiente antes de que se hayan creado los HWND.

Hay varias API que permiten especificar el reconocimiento de PPP predeterminado para el proceso. La API recomendada actual [**es SetProcessDpiAwarenessContext,**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\))ya que las API anteriores ofrecen menos funcionalidad.

 

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
<th>PPP sin reconocimiento</th>
<th>Reconocimiento de PPP del sistema</th>
<th>Reconocimiento de PPP por monitor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a></td>
<td>Windows Vista</td>
<td>N/D</td>
<td>SetProcessDPIAware()</td>
<td>N/D</td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></td>
<td>Windows 8.1</td>
<td>SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</td>
<td>SetProcessDpiAwareness(PROCESS_SYSTEM_DPI_AWARE)</td>
<td>SetProcessDpiAwareness(PROCESS_PER_MONITOR_DPI_AWARE)</td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></td>
<td>Windows 10, versión 1607</td>
<td>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</td>
<td>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</td>
<td><p>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</p>
<p>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a>Process-default frente a Thread default

Este documento hace referencia a la configuración del reconocimiento de PPP predeterminado para el proceso. Esto se debe a Windows 10 se introdujo compatibilidad para ejecutar más de un modo de reconocimiento de PPP dentro de un único proceso (antes de Windows 10, todo el proceso tenía que ajustarse a un único modo de reconocimiento de PPP). La compatibilidad con la ejecución de más de un modo de reconocimiento de PPP dentro de un proceso se conoce como "escalado de PPP en modo mixto". Cuando se usa el escalado de PPP en modo mixto dentro del proceso, cada ventana de nivel superior se puede ejecutar en un modo de reconocimiento de PPP que puede ser diferente del valor predeterminado del proceso. A menos que se especifique explícitamente, cada subproceso tendrá como valor predeterminado el proceso predeterminado cuando se cree. Para obtener más información sobre el escalado de PPP en modo mixto, consulte el artículo Escalado de [PPP](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) en modo mixto.
