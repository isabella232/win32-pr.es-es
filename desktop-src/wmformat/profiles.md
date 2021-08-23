---
title: Profiles
description: Profiles
ms.assetid: 6e70393f-3dab-4036-8d34-a672ef1795c6
keywords:
- Windows SDK de formato multimedia, perfiles
- Formato de sistemas avanzados (ASF),perfiles
- ASF (formato de sistemas avanzados),perfiles
- Windows Sdk de formato multimedia, archivos .prx
- Advanced Systems Format (ASF), archivos .prx
- ASF (formato de sistemas avanzados), archivos .prx
- Windows SDK de formato multimedia, Editor de perfiles
- Formato de sistemas avanzados (ASF),Editor de perfiles
- ASF (formato de sistemas avanzados),Editor de perfiles
- Archivos .prx
- Archivos prx
- Editor de perfiles
- Windows Codificador multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a89c06f031c9cf8214888efb35f2986135f88207fc94a631e1e111c94ce16d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707424"
---
# <a name="profiles"></a>Profiles

Un perfil es una colección de datos que describe la configuración de un archivo ASF. Como mínimo, un perfil debe contener valores de configuración para una sola secuencia.

La información de secuencia de un perfil contiene la velocidad de bits, la ventana de búfer y las propiedades multimedia de la secuencia. La información de secuencia de audio y vídeo describe exactamente cómo se configura el medio en el archivo, incluido el códec (si existe) que se usará para comprimir los datos.

Un perfil también contiene información sobre las distintas características del archivo ASF que se usarán en los archivos creados con él. Entre ellos se [incluyen Exclusión mutua,](mutual-exclusion.md) [Priorización de flujos,](stream-prioritization.md)Uso [compartido de](bandwidth-sharing.md)ancho de banda y Extensiones de unidad de [datos](data-unit-extensions.md).

Las versiones anteriores del SDK de formato multimedia de Windows proporcionaban perfiles de sistema preconfigurados, que se podían usar para crear tipos comunes de archivos o modificarse ligeramente para satisfacer las necesidades de la aplicación. Los perfiles del sistema no se admiten para los códecs Windows de la serie Media 9. Esto se debe a que el número de tipos de archivos "comunes" ha aumentado exponencialmente con la adición de nuevas características. Se espera que prácticamente todos los creadores de contenido tienen necesidades que van más allá de las soluciones sencillas proporcionadas por los perfiles del sistema. Todavía puede usar los perfiles del sistema antiguos como punto de partida. Para obtener más información, [vea Using System Profiles](using-system-profiles.md).

Debe proporcionar al escritor un perfil para cada archivo que escriba. Puede especificar un perfil para usarlo con el escritor llamando a [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).

Los datos de perfil existen en varios formularios diferentes que puede usar el SDK Windows Media Format. También se puede acceder a la información del perfil de varias maneras. Esto puede provocar confusión sobre lo que es un perfil y cómo se usa.

En el diagrama siguiente se muestra cómo se usan los datos de perfil en el SDK.

![diagrama que muestra el flujo de información de perfil.](images/formatsdk01.png)

Los datos de perfil tienen tres formas diferentes: datos contenidos en un objeto de perfil en una aplicación, un archivo XML en disco y datos en el encabezado de un archivo ASF. Cada una de estas formas de datos se muestra como un rectángulo sombreado en el diagrama.

## <a name="data-in-a-profile-object"></a>Datos de un objeto de perfil

Al editar un perfil, se usa un objeto de perfil, que encapsula todos los datos del perfil. Puede crear un objeto de perfil vacío mediante el objeto del administrador de perfiles. También puede usar el objeto del administrador de perfiles para cargar los datos de perfil existentes en un objeto de perfil.

La mayoría de los datos del perfil se deben agregar y manipular mediante el uso de objetos que representan partes individuales del perfil. Estos incluyen objetos de configuración de flujo, objetos de exclusión mutua, objetos de uso compartido de ancho de banda y un objeto de priorización de secuencias. Cada uno de estos tipos de objeto se puede crear mediante métodos en el objeto de perfil. La realización de cambios en estos objetos no afecta al objeto de perfil hasta que se usa un método en el objeto de perfil para incluir los datos actualizados del otro objeto.

## <a name="data-in-an-xml-file"></a>Datos de un archivo XML

Los datos de perfil se almacenan en el disco en forma de archivo XML con la extensión de nombre de archivo .prx. Incluido con el SDK Windows Media Format es una colección de perfiles denominados perfiles del sistema que cubren los tipos más comunes de archivos ASF. Los perfiles del sistema se almacenan en un archivo denominado WMSysPr9.prx. (Tenga en cuenta que este archivo realmente no contiene perfiles del sistema para Windows Media 9 Series porque ya no se usa el concepto de perfiles del sistema). Al guardar sus propios perfiles personalizados, debe guardarlos en sus propios archivos.

Puede usar el objeto del administrador de perfiles para guardar los datos de un objeto de perfil en una cadena de texto XML. A continuación, puede usar las funciones de E/S de archivo que quiera para guardar la cadena en un archivo en el disco.

## <a name="data-in-the-header-of-an-asf-file"></a>Datos en el encabezado de un archivo ASF

El escritor toma la información del perfil y la usa para crear los flujos que van a la sección de datos del archivo ASF. La mayor parte de los datos del perfil se almacenan en la sección de encabezado del archivo cuando se escribe un archivo. En la reproducción, el objeto lector (o el objeto de lector sincrónico) puede acceder a la información del encabezado del archivo. En este caso, el objeto de lectura crea un objeto de perfil y lo rellena con los datos del encabezado .

Al acceder a los datos del perfil mediante el lector (o lector sincrónico), puede realizar cambios en la información del perfil, pero no hay ninguna manera de aplicar esos cambios al archivo en el lector. Puede aplicar la información de perfil de un archivo de un lector a un perfil de un sistema de escritura para crear un archivo con la misma configuración que el archivo del lector. En este caso, los cambios que realice en la información del perfil antes de establecer el perfil en el escritor se reflejarán en la información de perfil registrada por el escritor.

## <a name="using-profile-editor"></a>Uso del Editor de perfiles

En lugar de crear perfiles mediante Windows SDK de formato multimedia, puede usar el Editor de perfiles, una utilidad que se incluye con Windows Media Encoder. En la aplicación de codificación, use el **método IWMProfileManager::LoadProfileByData** para cargar el perfil guardado. En algunos escenarios, por ejemplo, si usa un número limitado de perfiles que nunca se modifican dinámicamente, puede ser más conveniente usar el Editor de perfiles para crear los perfiles.

Sin embargo, si usa el Editor de perfiles, se recomienda no usar la opción "Tamaño de vídeo: igual que la entrada de vídeo". Cuando esta casilla está activada, el Editor de perfiles creará un perfil con el alto y el ancho de salida del vídeo establecidos en cero. Cuando Windows codificador multimedia encuentra estos perfiles, establece los valores correctos para que coincidan con su entrada de vídeo. Sin embargo, el escritor del SDK de formato multimedia de Windows no lo hace automáticamente, por lo que debe asegurarse de que la aplicación establece el tamaño del fotograma de vídeo en los casos en los que el perfil no tiene ninguno.

**Nota** Algunos elementos de configuración de flujo no se almacenan en el perfil. Los datos del perfil describen el formato del archivo ASF finalizado. Las propiedades de medios de entrada y otros datos de configuración utilizados por el objeto de escritor para configurar los códecs no se guardan en el perfil. Esto incluye todas las propiedades establecidas mediante [**el método IWMPropertyVault::SetProperty.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objeto de uso compartido de ancho de banda**](bandwidth-sharing-object.md)
</dt> <dt>

[**Conceptos**](concepts.md)
</dt> <dt>

[**IWMProfile (interfaz)**](iwmprofile.md)
</dt> <dt>

[**IWMProfileManager (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Objeto de exclusión mutua**](mutual-exclusion-object.md)
</dt> <dt>

[**Objeto del administrador de perfiles**](profile-manager-object.md)
</dt> <dt>

[**Objeto de configuración del flujo**](stream-configuration-object.md)
</dt> <dt>

[**Objeto Stream Prioritization**](stream-prioritization-object.md)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> </dl>

 

 




