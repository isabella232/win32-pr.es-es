---
title: Compatibilidad y confiabilidad
description: Windows 7 está diseñado para ejecutarse en el mismo hardware que Windows Vista y para ser compatible con aplicaciones y controladores de dispositivo que funcionan con Windows Vista.
ms.assetid: d7a0c335-93d1-49d3-ae40-c59ff9163f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e42dbf564fc524fbfb620746cea84e387fbe9f76484ce9e0d87803f55dae4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706305"
---
# <a name="compatibility-and-reliability"></a>Compatibilidad y confiabilidad

Windows 7 está diseñado para ejecutarse en el mismo hardware que Windows Vista y para ser compatible con aplicaciones y controladores de dispositivo que funcionan con Windows Vista.

Windows 7 es la versión más confiable de Windows todavía. Diseñado sobre una base tecnológica mejorada, Windows 7 permite a los usuarios iniciar, apagar o hibernar sus equipos de forma confiable sin tener que preocuparse por perder un trabajo valioso. Además, Windows 7 facilita más que nunca la copia de seguridad y restauración de datos en unidades de red o discos de vídeo digital (DVD). Windows 7 también mejora la confiabilidad y el rendimiento de la impresión. (Consulte Windows guía de calidad de la [aplicación 7).](../win7appqual/windows-7-application-quality-cookbook.md)

## <a name="applications"></a>Aplicaciones

Para ayudar a garantizar la compatibilidad, Windows 7 se ha diseñado en estrecha colaboración con proveedores de software y fabricantes de equipos. La interacción temprana ha permitido a Microsoft crear una lista completa de las aplicaciones más usadas. Los ciclos de prueba automatizados garantizan que los problemas de compatibilidad se detectan y se solucionan al principio del ciclo de desarrollo. (Vea [Windows compatibilidad de aplicaciones).](/windows/apps/desktop/)

## <a name="drivers"></a>Controladores

La versión 7.0.0 de Windows Driver Kit (WDK) proporciona el entorno de compilación, las herramientas, la documentación y los ejemplos que los desarrolladores necesitan para crear controladores de calidad para Windows. WDK 7.0.0 admite el análisis de código fuente estático, mediante PREfast para detectar determinadas clases de errores de codificación de C y C++. PREfast incluye un componente de controlador especializado, conocido como PREfast for Drivers (PFD), que detecta errores en el código del controlador en modo kernel. Además, wdk se ha mejorado mediante la anotación de todos los archivos de encabezado de kernel para la compatibilidad con PFD. Se han agregado nuevos controladores de ejemplo que muestran nuevas tecnologías y se ha ampliado la documentación.

Windows 7 admite una gran variedad de productos de software y hardware diseñados para integrarse sin problemas con la plataforma. Los controladores creados para Windows Vista no deben requerir que la actualización se ejecute correctamente en Windows 7. (Consulte [Windows Driver Kit](/windows-hardware/drivers/)).

## <a name="devices"></a>Dispositivos

Windows 7 proporciona compatibilidad flexible y sólida para una amplia variedad de aplicaciones y dispositivos, incluidos reproductores de música, dispositivos de almacenamiento, teléfonos móviles y otros tipos de dispositivos conectados. Las pruebas automáticas de estos dispositivos se usan para garantizar que los problemas de compatibilidad se corrigirán al principio del ciclo de desarrollo. (Vea [Windows aspectos básicos de la clase de dispositivo).](https://www.microsoft.com/whdc/device/default.mspx)

## <a name="reliability-analysis-component"></a>Componente de análisis de confiabilidad

Componente Análisis de confiabilidad es un agente incluido que proporciona información de experiencia del cliente detallada sobre el uso y la confiabilidad del sistema. Esta información se expone a través de una interfaz de WMI (Instrumental de administración de Windows), estando disponible para ser utilizada por lectores PRS (Portable Readers System). Mediante la exposición del componente Análisis de confiabilidad a través de una interfaz WMI, los desarrolladores pueden supervisar y analizar sus aplicaciones, aumentando la confiabilidad y el rendimiento.

Windows 7 usa el componente de análisis de confiabilidad integrado para calcular un índice de confiabilidad que proporciona información sobre el uso general del sistema y la estabilidad a lo largo del tiempo. El componente Análisis de confiabilidad también realiza el seguimiento de los cambios importantes producidos en el sistema que probablemente tengan un impacto en la estabilidad, como las actualizaciones de Windows y las instalaciones de aplicaciones. Puede usar el complemento Monitor de confiabilidad para ver tendencias en el índice de confiabilidad del sistema correlacionadas con estos eventos potencialmente desestabilizadores, lo que facilita el seguimiento de un cambio de confiabilidad directamente a un evento determinado. (Vea [Función MountVHD).](/previous-versions/windows/desktop/msvs/mountvhd)

 

 