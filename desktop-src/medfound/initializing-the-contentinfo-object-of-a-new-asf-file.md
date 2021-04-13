---
description: Inicializar el objeto ContentInfo de un nuevo archivo ASF
ms.assetid: a4f6c90e-1b38-4c70-8bc5-e2e16af3d87a
title: Inicializar el objeto ContentInfo de un nuevo archivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74826942700f4be8028075fcd9466414834eb8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360265"
---
# <a name="initializing-the-contentinfo-object-of-a-new-asf-file"></a>Inicializar el objeto ContentInfo de un nuevo archivo ASF

Después de crear un objeto ContentInfo vacío mediante una llamada a la función [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , la aplicación debe llamar a [**IMFASFContentInfo:: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para proporcionar el perfil de codificación. Para obtener información acerca de cómo crear un perfil, consulte [crear un perfil ASF](creating-an-asf-profile.md).

Antes de que se pueda leer la información del perfil, el método **SetProfile** debe validar el objeto de perfil especificado comprobando los identificadores de secuencia o los tipos de medios. Si el perfil pasa la validación, se generan varios objetos de encabezado, como el objeto de propiedades de archivo, el objeto de propiedades de velocidad de bits de flujo, el objeto de propiedades de la secuencia y el objeto de exclusión mutua.

**SetProfile** calcula y establece los valores recomendados para ciertas propiedades como, por ejemplo, el valor de preprocesamiento. Si aún no se ha establecido, el valor de preajuste recomendado en milisegundos depende de la ventana de búfer máxima del depósito de fugas especificado para las secuencias del perfil. Del mismo modo, también se establecen los tamaños de paquete de datos mínimo y máximo. Los valores recomendados podrían invalidar los tamaños de paquetes que se establecen en el perfil mediante atributos.

Dado que el archivo está en proceso de creación, el archivo se clasifica como un tipo de difusión, que se indica mediante el campo Flags del objeto de propiedades de archivo. Algunos valores desconocidos, como el número de paquetes de datos, la duración de la reproducción y la duración del envío, se establecen en cero. Estos valores están representados por los atributos **MF \_ PD \_ ASF \_ XXX** y deben ser actualizados por la aplicación una vez completada la creación del archivo.

El objeto de perfil especificado reemplaza cualquier perfil existente asociado al objeto ContentInfo, quita los objetos de encabezado a los que se hace referencia y restablece las propiedades de archivo globales, como el tamaño del paquete de datos y el preajuste.

El método **SetProfile** también crea el objeto de datos que representa el objeto de datos ASF. Si reutiliza un objeto ContentInfo que incluye información sobre los paquetes de datos, se produce un error de **SetProfile** y se devuelve el \_ error MF E \_ ya \_ inicializado, lo que indica que ya está asociado a un objeto de datos ASF existente. De forma predeterminada, para un nuevo objeto ContentInfo, el recuento de paquetes de datos se establece en cero y el tamaño del objeto de datos se establece en 50 bytes. Si usa el multiplexor para generar paquetes de datos, el multiplexor actualiza el objeto ContentInfo para reflejar los nuevos valores, como el recuento de paquetes de datos. Para obtener más información acerca de la generación de paquetes de datos, consulte [generación de nuevos paquetes de datos ASF](generating-new-asf-data-packets.md).

Después de agregar todos los objetos de encabezado al objeto de encabezado ASF final, se puede recuperar el tamaño total del encabezado mediante una llamada a [**IMFASFContentInfo:: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize). Este tamaño incluye el tamaño del objeto de datos inicial.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer propiedades en el objeto ContentInfo](setting-properties-in-the-contentinfo-object.md)
</dt> <dt>

[Escribir un objeto de encabezado ASF para un nuevo archivo](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



