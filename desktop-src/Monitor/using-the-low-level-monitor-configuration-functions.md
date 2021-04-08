---
title: Uso de las funciones de configuración del monitor de Low-Level
description: Uso de las funciones de configuración del monitor de Low-Level
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- supervisión, funciones
- supervisión, funciones de configuración de bajo nivel
- monitor, DDC/CI
- supervisar, Mostrar la interfaz de comandos del canal de datos
- supervisión de la configuración y las funciones de configuración de bajo nivel
- supervisión de la configuración, funciones
- configuración de monitor, DDC/CI
- configuración de monitor, Mostrar interfaz de comandos de canal de datos
- funciones de configuración de bajo nivel
- Mostrar interfaz de comandos del canal de datos
- DDC/CI
- Conjunto de comandos de control de monitor VESA (MCCS)
- Conjunto de comandos de control de supervisión (MCCS)
- MCCS (conjunto de comandos de control de monitor)
- Panel de control virtual (VCP)
- VCP (panel de control virtual)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d98e2cd4d85cb972b6a13896e9c497e51e16f8d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995199"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a>Uso de las funciones de configuración del monitor de Low-Level

Antes de usar las funciones de configuración del monitor de bajo nivel, debe estar familiarizado con estos estándares:

-   Mostrar la interfaz de comandos del canal de datos (DDC/CI)
-   Conjunto de comandos de control de monitor VESA (MCCS)

Las funciones de bajo nivel funcionan al obtener y establecer los valores de los códigos del panel de control virtual (VCP). Un código VCP puede ser *continuo* o no *continuo*. Los códigos continuos pueden suponer cualquier valor entre cero y un valor máximo específico del proveedor. Los códigos no continuos admiten un conjunto definido de valores, que también es específico del proveedor.

Para usar las funciones de configuración del monitor de bajo nivel, realice los pasos siguientes:

1.  Obtenga un identificador **HMONITOR** llamando a [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) o [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).
2.  Llame a [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) para obtener el número de monitores físicos asociados al identificador de **HMONITOR** .
3.  Llame a [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) para obtener una lista de identificadores para los monitores físicos.
4.  Llame a [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) para obtener la longitud de la cadena de funcionalidades DDC/CI de un monitor. La cadena Capabilities es una cadena ASCII que contiene información estática sobre el monitor. Una parte de la cadena muestra los códigos VCP que admite el monitor. La cadena también muestra los valores admitidos de los códigos VCP no continuos.
5.  Asigne un búfer para que contenga la cadena de funcionalidades y llame a [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) para obtener la cadena.
6.  Analice la cadena de funciones para determinar qué códigos VCP admite el monitor.
7.  Para un código VCP continuo, llame a [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) para obtener los valores actuales y máximos del código. En el caso de un código VCP no continuo, analice la cadena de funcionalidades para obtener los valores admitidos.
8.  Llame a [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) para establecer un nuevo valor para un código VCP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de la configuración de monitor**](using-monitor-configuration.md)
</dt> </dl>

 

 