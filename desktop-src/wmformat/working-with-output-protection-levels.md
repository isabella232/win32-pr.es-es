---
title: Trabajar con niveles de protección de salida
description: Trabajar con niveles de protección de salida
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- Windows SDK de formato multimedia, niveles de protección de salida (OPL)
- Windows SDK de formato multimedia, niveles de protección
- Formato de sistemas avanzados (ASF), niveles de protección de salida (OPL)
- ASF (formato de sistemas avanzados), niveles de protección de salida (OPL)
- Formato de sistemas avanzados (ASF), niveles de protección
- ASF (formato de sistemas avanzados), niveles de protección
- Formato de sistemas avanzados (ASF), varias licencias
- ASF (formato de sistemas avanzados), varias licencias
- administración de derechos digitales (DRM), niveles de protección de salida (OPL)
- DRM (administración de derechos digitales), niveles de protección de salida (OPL)
- administración de derechos digitales (DRM), niveles de protección
- DRM (administración de derechos digitales), niveles de protección
- administración de derechos digitales (DRM), evaluación de los niveles de protección de salida (OPL)
- DRM (administración de derechos digitales), evaluación de los niveles de protección de salida (OPL)
- administración de derechos digitales (DRM), varias licencias
- DRM (administración de derechos digitales), varias licencias
- niveles de protección de salida (OPL)
- OPL (niveles de protección de salida)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab7023cc8285e5f3993aac69c57deca9675d9dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247166"
---
# <a name="working-with-output-protection-levels"></a>Trabajar con niveles de protección de salida

Las licencias creadas mediante Windows SDK de Media Rights Manager 10 pueden especificar restricciones de acción mediante los niveles de protección de salida (OPL). Las OPIO permiten a un creador de licencias permitir algunas acciones solo en dispositivos con tecnologías específicas. Las ventajas de usar LASL es que obtiene más flexibilidad a la hora de crear restricciones de licencia que las versiones anteriores. Además, las OPL se pueden expandir para dar cabida a tecnologías futuras. Puede admitir dichas licencias en las aplicaciones mediante los métodos de la [**interfaz IWMDRMReader2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)

Para leer los archivos protegidos por una licencia que especifica las OPL, debe comprobar la acción deseada en OPL. La tecnología de salida que usa la aplicación debe estar permitida por OPL en la licencia. Por ejemplo, algunas licencias de audio protegido pueden requerir que use una ruta de acceso de audio segura para reproducirlo.

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a>Configuración del lector para evaluar los niveles de protección de salida

Para poder comprobar las direcciones URL de los archivos cargados en el lector, debe llamar al método [**IWMDRMReader2::SetEvaluateOutputLevelLicenses,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) pasando **TRUE** para el *parámetro fEvaluate.* Si no llama a este método, las licencias que requieren OTO no son visibles para la aplicación.

## <a name="evaluating-copy-output-protection-levels"></a>Evaluación de los niveles de protección de la salida de copia

Para obtener los niveles de protección de salida de la acción de copia, llame al método [**IWMDRMReader2::GetCopyOutputLevels.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) Los datos que recibe de la llamada se almacenan en una [**estructura \_ \_ OPL DE COPIA DE DRM.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) La estructura contiene un nivel de protección de salida base, que especifica el nivel de salida mínimo para la acción de copia en la licencia. Sin embargo, la estructura OPL COPY de DRM también contiene dos listas de identificadores de tecnología: una para las tecnologías permitidas que están clasificadas en un OPL inferior a la base y otra para tecnologías que tienen una clasificación igual o superior a la OPL base pero que están restringidas por la \_ \_ licencia. Debe comprobar las inclusiones y exclusiones para asegurarse de que la licencia permite la tecnología que usa la aplicación.

## <a name="evaluating-play-output-protection-levels"></a>Evaluación de los niveles de protección de salida de Play

Para obtener los niveles de protección de salida de la acción de reproducción, llame al método [**IWMDRMReader2::GetPlayOutputLevels.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) Los datos que recibe de la llamada se almacenan en una [**estructura \_ \_ OPL de DRM PLAY.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) La estructura contiene otras estructuras. Los niveles de protección de salida base para la acción de reproducción se almacenan en una estructura [**DRM MINIMUM OUTPUT PROTECTION \_ \_ \_ \_ LEVELS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) (el **miembro minOPL** de **DRM PLAY \_ \_ OPL),** que define el OPL mínimo necesario para reproducir contenido en una variedad de formatos. Debe comprobar el miembro para el tipo de formatos de salida que ofrece la aplicación.

La **estructura \_ \_ OPL de DRM PLAY** define dos tipos de restricciones: el muestreo de bajada necesario y los identificadores de protección de salida de vídeo permitidos.

El muestreo inferior requerido se define como una lista de identificadores de tecnología de salida (el miembro **oplIdDownsample** de **DRM PLAY \_ \_ OPL)** que, si se usa, solo puede recibir el contenido para la reproducción si el contenido se muestrea primero a una velocidad de bits inferior.

Los identificadores de protección de salida de vídeo permitidos se definen como una lista de tecnologías de salida de vídeo con información de configuración para cada uno.

## <a name="handling-multiple-licenses"></a>Control de varias licencias

Algunos archivos pueden tener varias licencias asociadas a ellos en el almacén de licencias local. Al evaluar las OLL de un archivo que está leyendo, puede buscar licencias adicionales llamando al método [**IWMDRMReader2::TryNextLicense.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) Debe seguir probando licencias hasta que encuentre una que permita la acción que desea realizar o hasta que TryNextLicense devuelva DRM S FALSE, lo que indica que no hay más \_ \_ licencias.

En algunos casos, un archivo podría tener una licencia asociada que requiere un OPL que la aplicación no pueda admitir. En tal caso, es importante comprobar si hay licencias adicionales, ya que puede existir una licencia que no especifique las OPL.

**Nota** DRM no es compatible con la versión basada en x64 de este SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interfaz IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




