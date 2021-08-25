---
description: Inicializar el objeto ContentInfo de un nuevo archivo ASF
ms.assetid: a4f6c90e-1b38-4c70-8bc5-e2e16af3d87a
title: Inicializar el objeto ContentInfo de un nuevo archivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf0180eb4e9369447355a9a4cd607f630bfb3664108ad77d6d008c281f92fdf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114255"
---
# <a name="initializing-the-contentinfo-object-of-a-new-asf-file"></a>Inicializar el objeto ContentInfo de un nuevo archivo ASF

Después de crear un objeto ContentInfo vacío llamando a la función [**MFCreateASFContentInfo,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) la aplicación debe llamar a [**MFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para proporcionar el perfil de codificación. Para obtener información sobre cómo crear un perfil, vea [Crear un perfil de ASF.](creating-an-asf-profile.md)

Para poder leer información del perfil, el **método SetProfile** debe validar el objeto de perfil especificado comprobando los identificadores de flujo o los tipos de medios. Si el perfil pasa la validación, se generan varios objetos de encabezado, como el objeto de propiedades de archivo, el objeto de propiedades de velocidad de bits de flujo, el objeto de propiedades de flujo y el objeto de exclusión mutua.

**SetProfile** calcula y establece los valores recomendados para determinadas propiedades, como el valor de inscripción previa. Si aún no se ha establecido, el valor de inscripción previa recomendado en milisegundos depende de la ventana de búfer máxima del cubo de pérdidas especificado para las secuencias del perfil. Del mismo modo, también se establecen los tamaños mínimo y máximo de paquetes de datos. Los valores recomendados pueden invalidar los tamaños de paquete que se establecen en el perfil a través de atributos.

Dado que el archivo está en proceso de creación, el archivo se clasifica como un tipo de difusión, que se indica mediante el campo Flags del objeto De propiedades de archivo. Ciertos valores desconocidos, como el número de paquetes de datos, la duración del juego y la duración del envío, se establecen en cero. Estos valores se representan mediante atributos **XXX de MF PD \_ \_ ASF \_** y la aplicación debe actualizarlo una vez completada la creación del archivo.

El objeto de perfil especificado reemplaza cualquier perfil existente asociado al objeto ContentInfo, quita los objetos de encabezado a los que se hace referencia y restablece las propiedades globales del archivo, como la inscripción previa y el tamaño del paquete de datos.

El **método SetProfile** también crea el objeto de datos que representa el objeto de datos de ASF. Si reutiliza un objeto ContentInfo que incluye información sobre los paquetes de datos, **SetProfile** produce un error y devuelve el error MF E ALREADY INITIALIZED que indica que ya está asociado a un objeto de \_ datos \_ \_ asf existente. De forma predeterminada, para un nuevo objeto ContentInfo, el número de paquetes de datos se establece en cero y el tamaño del objeto de datos se establece en 50 bytes. Si usa el multiplexor para generar paquetes de datos, el multiplexador actualiza el objeto ContentInfo para reflejar nuevos valores, como el número de paquetes de datos. Para obtener más información sobre la generación de paquetes de datos, vea [Generar nuevos paquetes de datos de ASF.](generating-new-asf-data-packets.md)

Después de agregar todos los objetos de encabezado al objeto de encabezado ASF final, se puede recuperar el tamaño total del encabezado llamando a [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize). Este tamaño incluye el tamaño inicial del objeto de datos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer propiedades en el objeto ContentInfo](setting-properties-in-the-contentinfo-object.md)
</dt> <dt>

[Escribir un objeto de encabezado ASF para un nuevo archivo](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



