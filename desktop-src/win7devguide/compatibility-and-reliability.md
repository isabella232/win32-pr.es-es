---
title: Compatibilidad y confiabilidad
description: Windows 7 está diseñado para ejecutarse en el mismo hardware que Windows Vista y para ser compatible con aplicaciones y controladores de dispositivos que funcionan con Windows Vista.
ms.assetid: d7a0c335-93d1-49d3-ae40-c59ff9163f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e9686c732c94b4b99408d0fd6e24f84079ee9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105705009"
---
# <a name="compatibility-and-reliability"></a>Compatibilidad y confiabilidad

Windows 7 está diseñado para ejecutarse en el mismo hardware que Windows Vista y para ser compatible con aplicaciones y controladores de dispositivos que funcionan con Windows Vista.

Windows 7 es la versión más confiable de Windows todavía. Diseñado con una base de tecnología mejorada, Windows 7 permite a los usuarios iniciar, apagar o hibernar sus equipos de forma confiable sin tener que preocuparse por perder trabajo valioso. Además, Windows 7 facilita más que nunca la copia de seguridad y la restauración de datos en unidades de red o discos de vídeo digital (DVDs). Windows 7 también mejora en cuanto a confiabilidad y rendimiento de impresión. (Consulte la guía de calidad de las [aplicaciones de Windows 7](../win7appqual/windows-7-application-quality-cookbook.md)).

## <a name="applications"></a>APLICACIONES

Para ayudar a garantizar la compatibilidad, Windows 7 se ha diseñado en estrecha colaboración con los proveedores de software y los fabricantes de PC. Early Engagement ha habilitado a Microsoft para crear una lista completa de las aplicaciones más usadas. Los ciclos de pruebas automatizadas garantizan que los problemas de compatibilidad se detectan y corrigen al principio del ciclo de desarrollo. (Consulte [compatibilidad de aplicaciones de Windows](/windows/apps/desktop/)).

## <a name="drivers"></a>Controladores

Windows Driver Kit (WDK) versión 7.0.0 proporciona el entorno de compilación, las herramientas, la documentación y los ejemplos que los desarrolladores necesitan para crear controladores de calidad para Windows. El WDK 7.0.0 es compatible con el análisis de código fuente estático, usando la PREfast para detectar ciertas clases de errores de codificación de C y C++. PREfast incluye un componente de controlador especializado, conocido como PREfast para controladores (PFD), que detecta errores en el código de controlador en modo kernel. Además, el WDK se ha mejorado anotando todos los archivos de encabezado del kernel para la compatibilidad con PFD. Se han agregado nuevos controladores de ejemplo que muestran nuevas tecnologías y la documentación se ha expandido.

Windows 7 es compatible con una gran variedad de productos de software y hardware diseñados para integrarse sin problemas con la plataforma. Los controladores creados para Windows Vista no deben requerir la actualización para ejecutarse correctamente en Windows 7. (Consulte [Kit de controladores de Windows](/windows-hardware/drivers/)).

## <a name="devices"></a>Dispositivos

Windows 7 proporciona compatibilidad flexible y robusta para una amplia variedad de aplicaciones y dispositivos, como reproductores de música, dispositivos de almacenamiento, teléfonos móviles y otros tipos de dispositivos conectados. Las pruebas automáticas de estos dispositivos se usan para garantizar que los problemas de compatibilidad se corrigen en el ciclo de desarrollo. (Consulte [aspectos básicos de las clases de dispositivos Windows](https://www.microsoft.com/whdc/device/default.mspx)).

## <a name="reliability-analysis-component"></a>Componente de análisis de confiabilidad

Componente Análisis de confiabilidad es un agente incluido que proporciona información de experiencia del cliente detallada sobre el uso y la confiabilidad del sistema. Esta información se expone a través de una interfaz de WMI (Instrumental de administración de Windows), estando disponible para ser utilizada por lectores PRS (Portable Readers System). Mediante la exposición del componente Análisis de confiabilidad a través de una interfaz WMI, los desarrolladores pueden supervisar y analizar sus aplicaciones, aumentando la confiabilidad y el rendimiento.

Windows 7 usa el componente de análisis de confiabilidad integrado para calcular un índice de confiabilidad que proporciona información sobre el uso y la estabilidad generales del sistema a lo largo del tiempo. El componente Análisis de confiabilidad también realiza el seguimiento de los cambios importantes producidos en el sistema que probablemente tengan un impacto en la estabilidad, como las actualizaciones de Windows y las instalaciones de aplicaciones. Puede usar el complemento monitor de confiabilidad para ver las tendencias en el índice de confiabilidad del sistema correlacionado con estos eventos potencialmente desestabilizadores, lo que facilita el seguimiento de un cambio de confiabilidad directamente en un evento determinado. (Consulte la [función MountVHD](/previous-versions/windows/desktop/msvs/mountvhd)).

 

 