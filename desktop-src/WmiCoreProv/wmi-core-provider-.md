---
description: El proveedor WMI Core define clases que componen la funcionalidad principal de WMI.
ms.assetid: 6EEA4284-CCFE-4206-9EAA-B4BCF988DE03
title: Proveedor principal wmi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9927be7208d9133d65257292950913972e96483
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465609"
---
# <a name="wmi-core-provider"></a>Proveedor principal wmi

El proveedor WMI Core define clases que componen la funcionalidad principal de WMI.

La mayoría de las clases de proveedor de WMI Core contienen datos proporcionados por el proveedor [de WDM](wdm-provider.md)y describen los monitores de presentación. Las clases se definen en Wmi.mof y se encuentran en el espacio de nombres \\ "WMI raíz".

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                           | Descripción                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSMonitorClass**](msmonitorclass.md)<br/>                                             | es una clase base WMI abstracta. Las clases que describen los monitores de visualización de vídeo heredan de [**este objeto MSMonitorClass.**](msmonitorclass.md)<br/>                                                                         |
| [Clases MSMCA](msmca-classes.md)<br/>                                                   | un conjunto de clases WMI que exponen la arquitectura de comprobación de máquina (MCA). La capa de abstracción del sistema (SAL) proporciona todos los eventos notificados en la clase MSMCA. Intel Corporation desarrolla y posee el MCA.<br/>         |
| [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md)<br/>                         | representa un contenedor para las características de un intervalo de frecuencia admitido.<br/>                                                                                                                                          |
| [**SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)<br/>     | representa las características de visualización admitidas del monitor.<br/>                                                                                                                                                           |
| [**VideoModeDescriptor**](videomodedescriptor.md)<br/>                                   | contiene elementos descriptores de modo **para la matriz MonitorSourceModes** de [**la clase WmiMonitorListedSupportedSourceModes.**](wmimonitorlistedsupportedsourcemodes.md)<br/>                                           |
| [**WMIEvent**](wmievent.md)<br/>                                                         | La [**clase WMIEvent**](wmievent.md) es una clase base de la que se derivan todas las clases de eventos WMI.<br/>                                                                                                                |
| [**WmiMonitorAnalogVideoInputParams**](wmimonitoranalogvideoinputparams.md)<br/>         | representa los parámetros de entrada de vídeo análogos de un monitor de equipo.<br/>                                                                                                                                                 |
| [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md)<br/>                 | representa las características de visualización básicas de un monitor de equipo.<br/>                                                                                                                                                        |
| [**WmiMonitorBrightness**](wmimonitorbrightness.md)<br/>                                 | representa los parámetros de brillo de un monitor de equipo.<br/>                                                                                                                                                         |
| [**WmiMonitorBrightnessEvent**](wmimonitorbrightnessevent.md)<br/>                       | representa un cambio en el brillo de un monitor.<br/>                                                                                                                                                                 |
| [**WmiMonitorBrightnessMethods**](wmimonitorbrightnessmethods.md)<br/>                   | contiene métodos que administran el brillo del monitor.<br/>                                                                                                                                                                    |
| [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md)<br/>             | representa las características de color de la Comisión Internacional de Iluminación (CIE) de un monitor de equipo.<br/>                                                                                                          |
| [**WmiMonitorConnectionParams**](wmimonitorconnectionparams.md)<br/>                     | contiene el tipo de conexión del monitor.<br/>                                                                                                                                                                        |
| [**WmiMonitorDescriptorMethods**](wmimonitordescriptormethods.md)<br/>                   | contiene métodos que obtienen el contenido sin procesar de los bloques de datos de 128 bytes estándar de definición de entrada de vídeo de video electronics standard association (VESA) Enhanced Extended Display Identification Data (E-EDID) v.1.x estándar.<br/> |
| [**WmiMonitorDigitalVideoInputParams**](wmimonitordigitalvideoinputparams.md)<br/>       | representa los parámetros de entrada para el vídeo digital.<br/>                                                                                                                                                                      |
| [**WmiMonitorID**](wmimonitorid.md)<br/>                                                 | representa la información de identificación sobre un monitor de vídeo, como el nombre del fabricante, el año de fabricación o el número de serie.<br/>                                                                                     |
| [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md)<br/>           | enumera los intervalos de frecuencia admitidos por el monitor.<br/>                                                                                                                                                                |
| [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md)<br/> | enumera los modos de origen admitidos para un monitor de vídeo en su descriptor de monitor, si existe alguno.<br/>                                                                                                                       |
| [**WmiMonitorRawEEdidV1Block**](wmimonitorraweedidv1block.md)<br/>                       | representa los datos sin procesar de una estructura de datos mejorados de identificación de pantalla extendida (E-EDID) de Video Electronics Standard Association (VESA).<br/>                                                                      |
| [**XYZinCIE**](xyzincie.md)<br/>                                                         | contiene las coordenadas de la presentación en el espacio de colores XYZ de la Comisión Internacional de Iluminación (CIE).<br/>                                                                                                      |



 

 

 




