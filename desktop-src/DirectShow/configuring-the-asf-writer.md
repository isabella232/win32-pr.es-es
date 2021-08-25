---
description: Configuración de ASF Writer
ms.assetid: 5708c4a0-6197-4a42-adfd-01c6dfe86302
title: Configuración de ASF Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e3d28b3b6178a383909f53a98fef98a5c3e69297f71615010f505d28b77375a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871705"
---
# <a name="configuring-the-asf-writer"></a>Configuración de ASF Writer

Cuando se crea el filtro [WM ASF Writer,](wm-asf-writer-filter.md) se configura automáticamente con el perfil WMProfile \_ V80 \_ 256Video. Este perfil usa los códecs Windows Media Audio y Windows Media Video versión 8, que no son tan recientes como los códecs de la serie Windows Media 9. Se recomienda crear un perfil personalizado que use los códecs de la serie Windows Media 9 y configurar WM ASF Writer con el perfil personalizado, como se describe en [Configuring Profiles and Other ASF File Properties](configuring-profiles-and-other-asf-file-properties.md). Debe agregar el filtro WM ASF Writer al gráfico de filtros antes de configurar el filtro y configurarlo antes de conectarlo a cualquier otro filtro.

Todos los datos de entrada deben tener marca de tiempo y todos los pines de entrada deben estar conectados antes de que el filtro se pueda ejecutar o pausar. Por lo tanto, si configura el filtro con un perfil que tiene una secuencia de audio y una secuencia de vídeo, el filtro creará un pin de entrada de audio y vídeo, y ambos pins deben estar conectados antes de que se pueda ejecutar el filtro. Dado que el SDK de formato multimedia de Windows requiere que una secuencia de audio funcione, WM ASF Writer siempre debe tener un pin de audio de entrada, incluso si es para una secuencia ficticia, es decir, una secuencia de audio muted y de baja velocidad de bits.

Agregar extensiones de unidad de datos

Puede configurar un flujo de perfil para extensiones de unidad de datos, como códigos de tiempo SMPTE, antes o después de conectar el filtro, siempre que siga este orden de operaciones:

1.  Agregue una o varias extensiones de unidad de datos a la secuencia **mediante IWMStreamConfig2::AddDataUnitExtension**.
2.  Llame **a IWMProfile::ReconfigStream** para actualizar el perfil.
3.  Llame [**a IConfigAsfWriter::ConfigureFilterUsingProfile con**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) el objeto de perfil actualizado.
4.  Busque el pin de entrada de vídeo y llame a su [**método IAMWMBufferPass::SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) para registrar la interfaz [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) definida por la aplicación.

Cuando se ejecuta el gráfico, se llamará al método [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) para cada fotograma y podrá obtener y establecer propiedades en el ejemplo mediante sus métodos de interfaz **INSSBuffer3.**

> [!Note]  
> En algunos escenarios con un uso intensivo del procesador, como la tele telefónica inversa, WM ASF Writer puede requerir más búferes de salida de los que admiten algunos filtros de nivel inferior. El descodificador DV, por ejemplo, no aceptará más de un búfer para su pin de salida y lo mismo sucede para el descomprimidor AVI en determinadas condiciones. Si tiene problemas al intentar conectarse a estos filtros, o posiblemente al ejecutar el gráfico, puede que sea necesario escribir un filtro intermedio que acepte cualquier número de búferes en su pin de salida.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



