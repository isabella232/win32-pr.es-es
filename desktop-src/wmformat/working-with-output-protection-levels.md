---
title: Trabajar con niveles de protección de salida
description: Trabajar con niveles de protección de salida
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- Windows Media Format SDK, niveles de protección de salida (OPL)
- Windows Media Format SDK, niveles de protección
- Advanced Systems Format (ASF), niveles de protección de salida (OPL)
- ASF (formato de sistemas avanzados), niveles de protección de salida (OPL)
- Advanced Systems Format (ASF), niveles de protección
- ASF (formato de sistemas avanzados), niveles de protección
- Advanced Systems Format (ASF), varias licencias
- ASF (formato de sistemas avanzados), varias licencias
- Administración de derechos digitales (DRM), niveles de protección de salida (OPL)
- DRM (administración de derechos digitales), niveles de protección de salida (OPL)
- Administración de derechos digitales (DRM), niveles de protección
- DRM (administración de derechos digitales), niveles de protección
- Administración de derechos digitales (DRM), evaluación de los niveles de protección de salida (OPL)
- DRM (administración de derechos digitales), evaluación de los niveles de protección de salida (OPL)
- Administración de derechos digitales (DRM), varias licencias
- DRM (administración de derechos digitales), varias licencias
- niveles de protección de salida (OPL)
- OPL (niveles de protección de salida)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab7023cc8285e5f3993aac69c57deca9675d9dd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358668"
---
# <a name="working-with-output-protection-levels"></a>Trabajar con niveles de protección de salida

Las licencias creadas con el SDK de Windows Media Rights Manager 10 pueden especificar restricciones de acción mediante los niveles de protección de salida (OPLs). OPLs permite a un creador de licencias permitir algunas acciones solo en dispositivos con tecnologías específicas. Las ventajas de usar OPLs es que obtiene más flexibilidad a la hora de crear restricciones de licencia que las versiones anteriores. Además, los OPLs se pueden expandir para adaptarse a las tecnologías futuras. Puede admitir tales licencias en sus aplicaciones mediante los métodos de la interfaz [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) .

Para leer los archivos que están protegidos por una licencia que especifica OPLs, debe comprobar el OPL para la acción deseada. La tecnología de salida que usa la aplicación debe ser permitida por el OPL de la licencia. Por ejemplo, algunas licencias de audio protegido pueden requerir que use la ruta de acceso de audio segura para reproducirla.

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a>Configuración del lector para evaluar los niveles de protección de los resultados

Antes de poder comprobar OPLs para los archivos cargados en el lector, debe llamar al método [**IWMDRMReader2:: SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) , pasando **true** para el parámetro *fEvaluate* . Si no llama a este método, las licencias que requieren OPLs no son visibles para la aplicación.

## <a name="evaluating-copy-output-protection-levels"></a>Evaluación de los niveles de protección de la salida de copia

Para obtener los niveles de protección de salida de la acción de copia, llame al método [**IWMDRMReader2:: GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) . Los datos que recibe de la llamada se almacenan en una estructura del [**\_ \_ OPL de copia de DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) . La estructura contiene un nivel de protección de salida base, que especifica el nivel de salida mínimo para la acción de copia en la licencia. Sin embargo, la \_ estructura del OPL de copia \_ de DRM también contiene dos listas de identificadores de tecnología: una para las tecnologías permitidas que se clasifican en un OPL inferior al de la base, y otra para las tecnologías cuya clasificación es igual o superior al OPL base, pero que están restringidas por la licencia. Debe comprobar las inclusiones y exclusiones para asegurarse de que la tecnología que está usando la aplicación está permitida por la licencia.

## <a name="evaluating-play-output-protection-levels"></a>Evaluación de los niveles de protección de la salida de reproducción

Para obtener los niveles de protección de salida de la acción Play, llame al método [**IWMDRMReader2:: GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) . Los datos que recibe de la llamada se almacenan en una estructura de receptor de [**\_ \_ reproducción DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) . La estructura contiene otras estructuras. Los niveles de protección de salida base para la acción de reproducción se almacenan en una estructura de niveles de  [**\_ \_ \_ protección \_ de salida mínima de DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) (el miembro minOPL de un **\_ \_ OPL de reproducción de DRM**), que define el valor de OPL mínimo necesario para reproducir contenido en diversos formatos. Debe comprobar el miembro para el tipo de formato de salida que proporciona la aplicación.

La estructura del **\_ \_ OPL de reproducción de DRM** define dos tipos de restricciones: el muestreo necesario y los identificadores de protección de salida de vídeo permitidos.

Required: el muestreo se define como una lista de identificadores de tecnología de salida (el miembro **oplIdDownsample** de **DRM Play de DRM \_ \_**) que, si se usa, puede recibir el contenido de la reproducción solo si el contenido se muestra por primera vez en una velocidad de bits inferior.

Los identificadores de protección de salida de vídeo permitidos se definen como una lista de tecnologías de salida de vídeo con información de configuración para cada uno.

## <a name="handling-multiple-licenses"></a>Control de varias licencias

Algunos archivos pueden tener varias licencias asociadas a ellos en el almacén de licencias local. Al evaluar OPLs para un archivo que está leyendo, puede comprobar si hay más licencias llamando al método [**IWMDRMReader2:: TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) . Debe seguir probando licencias hasta que encuentre una que permita la acción que desea realizar o hasta que TryNextLicense devuelva DRM \_ S \_ false, lo que indica que no hay más licencias.

En algunos casos, un archivo puede tener una licencia asociada que requiere un OPL que la aplicación no admite. En tal caso, es importante comprobar si hay licencias adicionales, ya que puede existir una licencia que no especifique OPLs.

**Nota:** DRM no es compatible con la versión basada en x64 de este SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interfaz IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




