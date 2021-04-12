---
description: El proveedor principal de WMI define las clases que componen la funcionalidad básica de WMI.
ms.assetid: 6EEA4284-CCFE-4206-9EAA-B4BCF988DE03
title: Proveedor principal de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9927be7208d9133d65257292950913972e96483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278416"
---
# <a name="wmi-core-provider"></a>Proveedor principal de WMI

El proveedor principal de WMI define las clases que componen la funcionalidad básica de WMI.

La mayoría de las clases de proveedor de WMI Core contienen los datos proporcionados por el [proveedor de WDM](wdm-provider.md)y describen los monitores de pantalla. Las clases se definen en WMI. mof y se encuentran en el espacio de \\ nombres "WMI raíz".

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                           | Descripción                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSMonitorClass**](msmonitorclass.md)<br/>                                             | es una clase base abstracta de WMI. Las clases que describen monitores de pantalla de vídeo heredan de este [**MSMonitorClass**](msmonitorclass.md).<br/>                                                                         |
| [Clases MSMCA](msmca-classes.md)<br/>                                                   | un conjunto de clases WMI que exponen la arquitectura de comprobación automática (MCA). La capa de abstracción del sistema (SAL) proporciona todos los eventos que se indican en la clase MSMCA. Intel Corporation desarrolla y posee la MCA.<br/>         |
| [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md)<br/>                         | representa un contenedor para las características de un intervalo de frecuencias admitido.<br/>                                                                                                                                          |
| [**SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)<br/>     | representa las características de presentación admitidas del monitor.<br/>                                                                                                                                                           |
| [**VideoModeDescriptor**](videomodedescriptor.md)<br/>                                   | contiene los elementos de descriptor de modo de la matriz **MonitorSourceModes** en la clase [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) .<br/>                                           |
| [**WMIEvent**](wmievent.md)<br/>                                                         | La clase [**WMIEvent**](wmievent.md) es una clase base de la que se derivan todas las clases de eventos WMI.<br/>                                                                                                                |
| [**WmiMonitorAnalogVideoInputParams**](wmimonitoranalogvideoinputparams.md)<br/>         | representa los parámetros de entrada de vídeo analógico de un monitor de equipo.<br/>                                                                                                                                                 |
| [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md)<br/>                 | representa las características básicas de pantalla de un monitor de equipo.<br/>                                                                                                                                                        |
| [**WmiMonitorBrightness**](wmimonitorbrightness.md)<br/>                                 | representa los parámetros de brillo de un monitor de equipo.<br/>                                                                                                                                                         |
| [**WmiMonitorBrightnessEvent**](wmimonitorbrightnessevent.md)<br/>                       | representa un cambio en el brillo de un monitor.<br/>                                                                                                                                                                 |
| [**WmiMonitorBrightnessMethods**](wmimonitorbrightnessmethods.md)<br/>                   | contiene métodos que administran el brillo del monitor.<br/>                                                                                                                                                                    |
| [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md)<br/>             | representa las características de color de la Comisión Internacional de iluminación (CIE) de un monitor del equipo.<br/>                                                                                                          |
| [**WmiMonitorConnectionParams**](wmimonitorconnectionparams.md)<br/>                     | contiene el tipo de conexión del monitor.<br/>                                                                                                                                                                        |
| [**WmiMonitorDescriptorMethods**](wmimonitordescriptormethods.md)<br/>                   | contiene métodos que obtienen el contenido sin procesar de la definición de entrada de vídeo de Video Electronics estándar Association (VESA) datos de identificación mejorada de la visualización extendida (E-EDID) v. 1. x 128 bits bloques de datos de bytes.<br/> |
| [**WmiMonitorDigitalVideoInputParams**](wmimonitordigitalvideoinputparams.md)<br/>       | representa los parámetros de entrada para el vídeo digital.<br/>                                                                                                                                                                      |
| [**WmiMonitorID**](wmimonitorid.md)<br/>                                                 | representa la información de identificación de un monitor de vídeo, como el nombre del fabricante, el año de fabricación o el número de serie.<br/>                                                                                     |
| [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md)<br/>           | muestra los intervalos de frecuencia que admite el monitor.<br/>                                                                                                                                                                |
| [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md)<br/> | enumera los modos de origen admitidos para un monitor de vídeo en su descriptor de monitor, si existe alguno.<br/>                                                                                                                       |
| [**WmiMonitorRawEEdidV1Block**](wmimonitorraweedidv1block.md)<br/>                       | representa los datos sin procesar de una estructura de datos de identificación mejorada de la presentación extendida (E-EDID) de la Asociación estándar de vídeo electrónica (VESA).<br/>                                                                      |
| [**XYZinCIE**](xyzincie.md)<br/>                                                         | contiene las coordenadas de la presentación en el espacio de color de la Comisión Internacional de iluminación (CIE) XYZ.<br/>                                                                                                      |



 

 

 




