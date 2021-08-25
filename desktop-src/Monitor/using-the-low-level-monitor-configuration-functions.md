---
title: Uso de las funciones de configuración Low-Level Monitor
description: Uso de las funciones de configuración Low-Level Monitor
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- monitor,functions
- monitor, funciones de configuración de bajo nivel
- monitor,DDC/CI
- monitor,Display Data Channel Command Interface
- supervisar la configuración, funciones de configuración de bajo nivel
- monitor configuration,functions
- monitor configuration,DDC/CI
- monitor configuration,Display Data Channel Command Interface
- funciones de configuración de bajo nivel
- Mostrar la interfaz de comandos del canal de datos
- DDC/CI
- Conjunto de comandos de control de VESA Monitor (MCCS)
- Supervisar conjunto de comandos de control (MCCS)
- MCCS (Supervisar conjunto de comandos de control)
- Virtual Panel de control (VCP)
- VCP (virtual Panel de control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ffd21f0b232db71bb6023f968122271ce70f03b0a632dc33d9df1e7ee993bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927395"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a>Uso de las funciones de configuración Low-Level Monitor

Antes de usar las funciones de configuración de monitor de bajo nivel, debe estar familiarizado con estos estándares:

-   Mostrar la interfaz de comandos del canal de datos (DDC/CI)
-   Conjunto de comandos de control de VESA Monitor (MCCS)

Las funciones de bajo nivel funcionan obteniendo y estableciendo los valores de los códigos Panel de control virtual (VCP). Un código VCP puede *ser continuo* o *no continuo.* Los códigos continuos pueden suponer cualquier valor entre cero y un valor máximo específico del proveedor. Los códigos no pertinentes admiten un conjunto definido de valores, que también es específico del proveedor.

Para usar las funciones de configuración de monitor de bajo nivel, realice los pasos siguientes:

1.  Obtenga un **identificador HMONITOR** mediante una llamada [**a EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) o [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).
2.  Llame [**a GetNumberOfPhysicalMonitorsFromHMONITOR para**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) obtener el número de monitores físicos asociados al identificador **HMONITOR.**
3.  Llame [**a GetPhysicalMonitorsFromHMONITOR para**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) obtener una lista de identificadores para los monitores físicos.
4.  Llame [**a GetCapabilitiesStringLength para**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) obtener la longitud de la cadena de funcionalidades de DDC/CI de un monitor. La cadena capabilities es una cadena ASCII que contiene información estática sobre el monitor. Una parte de la cadena enumera los códigos VCP que admite el monitor. La cadena también enumera los valores admitidos de los códigos VCP no comunes.
5.  Asigne un búfer para contener la cadena de funcionalidades y llame a [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) para obtener la cadena.
6.  Analice la cadena de funcionalidades para determinar qué códigos de VCP admite el monitor.
7.  Para obtener un código VCP continuo, llame a [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) para obtener los valores actual y máximo del código. Para un código VCP no constante, analice la cadena de funcionalidades para obtener los valores admitidos.
8.  Llame [**a SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) para establecer un nuevo valor para un código VCP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de la configuración de Monitor**](using-monitor-configuration.md)
</dt> </dl>

 

 