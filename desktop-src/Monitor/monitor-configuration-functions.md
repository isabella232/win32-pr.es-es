---
title: Supervisar funciones de configuración
description: Supervisar funciones de configuración
ms.assetid: e9a00792-f471-47a4-93d7-25400e27f13f
keywords:
- supervisión, funciones
- supervisión, funciones de alto nivel
- supervisión, funciones de bajo nivel
- supervisión, funciones de enumeración
- funciones de alto nivel
- funciones de bajo nivel
- funciones de enumeración
- supervisión de la configuración, funciones
- supervisión de la configuración y las funciones de alto nivel
- supervisión de la configuración y las funciones de bajo nivel
- supervisión de la configuración, funciones de enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86925cd25912c17b8fb1bdd339888e5429de135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665725"
---
# <a name="monitor-configuration-functions"></a>Supervisar funciones de configuración

Las funciones siguientes se utilizan para obtener información de un monitor y cambiar la configuración de un monitor. Las funciones de configuración de supervisión se clasifican en funciones de alto nivel, funciones de bajo nivel y funciones de enumeración. Para obtener más información, consulte uso de la [configuración de monitor](using-monitor-configuration.md).

## <a name="high-level-functions"></a>Funciones de High-Level



| Función                                                                         | Descripción                                                                          |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**DegaussMonitor**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-degaussmonitor)                                         | Desmagnetiza un monitor.                                                                 |
| [**GetMonitorBrightness**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorbrightness)                             | Recupera la configuración mínima, máxima y de brillo actual del monitor.             |
| [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities)                         | Recupera las capacidades de configuración de un monitor.                               |
| [**GetMonitorColorTemperature**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcolortemperature)                 | Recupera la temperatura de color actual del monitor.                                     |
| [**GetMonitorContrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcontrast)                                 | Recupera los valores mínimo, máximo y de contraste actual del monitor.               |
| [**GetMonitorDisplayAreaPosition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareaposition)           | Recupera el mínimo, el máximo y la posición horizontal o vertical actual del monitor. |
| [**GetMonitorDisplayAreaSize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareasize)                   | Recupera el valor mínimo, máximo y el ancho o alto actual del monitor.                 |
| [**GetMonitorRedGreenOrBlueDrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluedrive)           | Recupera el valor de la unidad roja, verde o azul del monitor.                               |
| [**GetMonitorRedGreenOrBlueGain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluegain)             | Recupera el valor de ganancia rojo, verde o azul de un monitor.                                |
| [**GetMonitorTechnologyType**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitortechnologytype)                     | Recupera el tipo de tecnología que usa un monitor.                                  |
| [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) | Restaura la configuración de color de un monitor a sus valores predeterminados de fábrica.                       |
| [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults)           | Restaura la configuración de un monitor a sus valores predeterminados de fábrica.                             |
| [**SaveCurrentMonitorSettings**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-savecurrentmonitorsettings)                 | Guarda la configuración del monitor actual en el almacenamiento no volátil de la pantalla.             |
| [**SetMonitorBrightness**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorbrightness)                             | Establece el valor de brillo de un monitor.                                                   |
| [**SetMonitorColorTemperature**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature)                 | Establece la temperatura de color de un monitor.                                                  |
| [**SetMonitorContrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcontrast)                                 | Establece el valor de contraste de un monitor.                                                     |
| [**SetMonitorDisplayAreaPosition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareaposition)           | Establece la posición horizontal o vertical del área de presentación de un monitor.                |
| [**SetMonitorDisplayAreaSize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareasize)                   | Establece el ancho o el alto del área de presentación de un monitor.                                |
| [**SetMonitorRedGreenOrBlueDrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluedrive)           | Establece un valor de unidad rojo, verde o azul del monitor.                                    |
| [**SetMonitorRedGreenOrBlueGain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluegain)             | Establece el valor de ganancia rojo, verde o azul de un monitor.                                     |



 

## <a name="low-level-functions"></a>Funciones de Low-Level



| Función                                                                                   | Descripción                                                                                                    |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) | Recupera una cadena que describe las capacidades de un monitor.                                                        |
| [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength)                         | Recupera la longitud de la cadena de funciones de un monitor.                                                       |
| [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport)                                                 | Recupera las frecuencias de sincronización horizontal y vertical del monitor.                                     |
| [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply)                 | Recupera el valor actual, el valor máximo y el tipo de código de un código del panel de control virtual (VCP) de un monitor. |
| [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings)                                         | Guarda la configuración del monitor actual en el almacenamiento no volátil de la pantalla.                                       |
| [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature)                                                     | Establece el valor de un código del panel de control virtual (VCP) para un monitor.                                            |



 

## <a name="enumeration-functions"></a>Funciones de enumeración



| Función                                                                                                   | Descripción                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)                                                   | Cierra un identificador de un monitor físico.                                                    |
| [**DestroyPhysicalMonitors**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitors)                                                 | Cierra una matriz de identificadores de monitor físicos.                                              |
| [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)                 | Recupera el número de monitores físicos asociados a un identificador de monitor de **HMONITOR** . |
| [**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9) | Recupera el número de monitores físicos asociados a un dispositivo Direct3D.              |
| [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)                                 | Recupera los monitores físicos asociados a un identificador de monitor de **HMONITOR** .           |
| [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)                 | Recupera los monitores físicos asociados a un dispositivo Direct3D.                        |



 

## <a name="internal-functions"></a>Funciones internas

La API de configuración de supervisión utiliza las siguientes funciones para tener acceso a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a estas funciones.

-   [**DDCCIGetCapabilitiesString**](ddccigetcapabilitiesstring.md)
-   [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md)
-   [**DDCCIGetTimingReport**](ddccigettimingreport.md)
-   [**DDCCIGetVCPFeature**](ddccigetvcpfeature.md)
-   [**DDCCISaveCurrentSettings**](ddccisavecurrentsettings.md)
-   [**DDCCISetVCPFeature**](ddccisetvcpfeature.md)
-   [**DestroyPhysicalMonitorInternal**](destroyphysicalmonitorinternal.md)
-   [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md)
-   [**GetPhysicalMonitorDescription**](getphysicalmonitordescription.md)
-   [**GetPhysicalMonitors**](getphysicalmonitors.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de configuración de monitor](monitor-configuration-reference.md)
</dt> </dl>

 

 




