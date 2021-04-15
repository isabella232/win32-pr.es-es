---
title: Profiles
description: Profiles
ms.assetid: 6e70393f-3dab-4036-8d34-a672ef1795c6
keywords:
- Windows Media Format SDK, perfiles
- Advanced Systems Format (ASF), perfiles
- ASF (formato de sistemas avanzados), perfiles
- SDK de Windows Media Format, archivos. prx
- Advanced Systems Format (ASF), archivos. prx
- ASF (formato de sistemas avanzados), archivos. prx
- SDK de Windows Media Format, editor de perfiles
- Advanced Systems Format (ASF), editor de perfiles
- ASF (formato de sistemas avanzados), editor de perfiles
- archivos. prx
- archivos PRX
- Editor de perfiles
- Codificador de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de244445a7c1301c7a14ef273b81ac9fd9cbfb62
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695552"
---
# <a name="profiles"></a>Profiles

Un perfil es una colección de datos que describe la configuración de un archivo ASF. Como mínimo, un perfil debe contener valores de configuración para un solo flujo.

La información de la secuencia de un perfil contiene la velocidad de bits, la ventana del búfer y las propiedades multimedia de la secuencia. La información del flujo de audio y vídeo describe exactamente cómo se configura el medio en el archivo, incluido el códec (si existe) que se utilizará para comprimir los datos.

Un perfil también contiene información acerca de las diversas características de archivos ASF que se utilizarán en los archivos creados con ella. Entre ellas se incluyen [exclusión mutua](mutual-exclusion.md), [priorización de flujo](stream-prioritization.md), [uso compartido de ancho de banda](bandwidth-sharing.md)y extensiones de unidad de [datos](data-unit-extensions.md).

Las versiones anteriores del SDK de Windows Media Format proporcionaban perfiles del sistema preconfigurados, que podrían usarse para crear tipos comunes de archivos o modificarse ligeramente para adaptarse a las necesidades de la aplicación. Los perfiles del sistema no son compatibles con los códecs de la serie Windows Media 9. Esto se debe a que el número de tipos "comunes" de archivos ha crecido exponencialmente con la adición de nuevas características. Se espera que prácticamente todos los creadores de contenido tengan que ir más allá de las soluciones simples proporcionadas por los perfiles del sistema. Todavía puede usar los perfiles del sistema antiguos como punto de partida. Para obtener más información, consulte [Using System profiles](using-system-profiles.md).

Debe proporcionar el sistema de escritura con un perfil para cada archivo que escriba. Puede especificar un perfil para usarlo con el escritor llamando a [**IWMWriter:: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).

Los datos de perfil existen en varias formas diferentes que puede usar el SDK de Windows Media Format. También se puede tener acceso a la información de Perfil de varias maneras. Esto puede llevar a confusión sobre qué es un perfil y cómo se usa.

En el diagrama siguiente se muestra cómo se usan los datos de perfil en el SDK.

![diagrama que muestra el flujo de información de perfil.](images/formatsdk01.png)

Los datos de perfil adoptan tres formas diferentes: los datos contenidos en un objeto de Perfil de una aplicación, un archivo XML en el disco y los datos en el encabezado de un archivo ASF. Cada una de estas formas de datos se muestra como un rectángulo sombreado en el diagrama.

## <a name="data-in-a-profile-object"></a>Datos en un objeto de perfil

Cuando se edita un perfil, se usa un objeto de perfil, que encapsula todos los datos del perfil. Puede crear un objeto de perfil vacío mediante el objeto de administrador de perfiles. También puede usar el objeto de administrador de perfiles para cargar los datos de perfil existentes en un objeto de perfil.

La mayoría de los datos de perfil se deben agregar y manipular mediante el uso de objetos que representan partes individuales del perfil. Estos incluyen objetos de configuración de secuencias, objetos de exclusión mutua, objetos de uso compartido de ancho de banda y un objeto de priorización de flujo. Cada uno de estos tipos de objeto se puede crear mediante métodos en el objeto de perfil. La realización de cambios en estos objetos no afecta al objeto de perfil hasta que se usa un método en el objeto de perfil para incluir los datos actualizados del otro objeto.

## <a name="data-in-an-xml-file"></a>Datos en un archivo XML

Los datos de perfil se almacenan en el disco en forma de archivo XML con la extensión de nombre de archivo. prx. En el SDK de Windows Media Format se incluye un conjunto de perfiles denominados perfiles del sistema que cubren los tipos de archivos ASF más comunes. Los perfiles del sistema se almacenan en un archivo denominado WMSysPr9. prx. (Tenga en cuenta que este archivo no contiene ningún perfil de sistema para Windows Media 9 series porque ya no se usa el concepto de perfiles del sistema). Cuando guarde sus propios perfiles personalizados, deberá guardarlos en sus propios archivos.

Puede usar el objeto de administrador de perfiles para guardar los datos de un objeto de perfil en una cadena de texto XML. Después, puede usar cualquier función de e/s de archivo que desee para guardar la cadena en un archivo en disco.

## <a name="data-in-the-header-of-an-asf-file"></a>Datos en el encabezado de un archivo ASF

El escritor toma la información del perfil y la usa para crear las secuencias que van a la sección de datos del archivo ASF. La mayor parte de los datos de perfil se almacena en la sección de encabezado del archivo cuando se escribe un archivo. En la reproducción, el objeto lector (o el objeto lector sincrónico) puede tener acceso a la información del encabezado del archivo. En este caso, el objeto de lectura crea un objeto de perfil y lo rellena con los datos del encabezado.

Al tener acceso a los datos del perfil mediante el lector (o el lector sincrónico), puede realizar cambios en la información del perfil, pero no hay ninguna manera de aplicar esos cambios al archivo en el lector. Puede aplicar la información de Perfil de un archivo en un lector a un perfil de un escritor para crear un nuevo archivo con la misma configuración que el archivo del lector. En este caso, cualquier cambio que realice en la información del perfil antes de configurar el perfil en el escritor se reflejará en la información de perfil registrada por el escritor.

## <a name="using-profile-editor"></a>Usar el editor de perfiles

En lugar de crear perfiles mediante el SDK de Windows Media Format, puede usar el editor de perfiles, una utilidad que se incluye con el codificador de Windows Media. En la aplicación de codificación, use el método **IWMProfileManager:: LoadProfileByData** para cargar el perfil guardado. En algunos escenarios, por ejemplo, si usa un número limitado de perfiles que nunca se modifican dinámicamente, puede ser más conveniente usar el editor de perfiles para crear los perfiles.

Sin embargo, si usa el editor de perfiles, se recomienda que no use la opción "tamaño de vídeo: igual que la entrada de vídeo". Cuando esta casilla está activada, el editor de perfiles creará un perfil con el ancho y el alto de salida de vídeo establecidos en cero. Cuando Windows Media Encoder encuentra estos perfiles, establece los valores correctos para que coincidan con su entrada de vídeo. Sin embargo, el escritor del SDK de Windows Media Format no lo hace automáticamente, por lo que debe asegurarse de que la aplicación establece el tamaño del fotograma de vídeo en los casos en los que el perfil no tiene ninguno.

**Nota:** Algunos elementos de configuración de secuencia no se almacenan en el perfil. Los datos del perfil describen el formato del archivo ASF terminado. Las propiedades de los medios de entrada y otros datos de configuración usados por el objeto de escritor para configurar los códecs no se guardan en el perfil. Esto incluye todas las propiedades establecidas mediante el método [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objeto de uso compartido de ancho de banda**](bandwidth-sharing-object.md)
</dt> <dt>

[**Conceptos**](concepts.md)
</dt> <dt>

[**Interfaz IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interfaz IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Objeto de exclusión mutua**](mutual-exclusion-object.md)
</dt> <dt>

[**Objeto del administrador de perfiles**](profile-manager-object.md)
</dt> <dt>

[**Objeto de configuración del flujo**](stream-configuration-object.md)
</dt> <dt>

[**Objeto de priorización de flujo**](stream-prioritization-object.md)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> </dl>

 

 




