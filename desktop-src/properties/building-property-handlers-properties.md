---
description: Las propiedades se representan mediante identificadores conocidos como identificadores de propiedad (PID).
ms.assetid: a773c7b3-a1a2-4cce-ae5f-b54217ea06f4
title: Descripción de los controladores de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 564d6f8bd325e649ff1356869932521d8c1cd885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276209"
---
# <a name="understanding-property-handlers"></a>Descripción de los controladores de propiedades

Las propiedades se representan mediante identificadores conocidos como identificadores de propiedad (PID). Cada propiedad debe tener un identificador único global (GUID). Este identificador está compuesto de un GUID, que representa una colección de propiedades denominada un conjunto de propiedades más una cadena o un entero de 32 bits para identificar la propiedad dentro del conjunto. Si se utiliza la forma de entero de ID, se considera que los valores 0x00000000, 0xFFFFFFFF y 0xFFFFFFFE no son válidos. Los proveedores pueden garantizar que sus propiedades se definen de forma única al colocarlas en un conjunto de propiedades definido por sus propios GUID.

> [!IMPORTANT]
> Es fundamental que defina las propiedades con cuidado y de forma estratégica para la primera versión del esquema. Cualquier cambio en las propiedades personalizadas (como el ancho de columna o el tipo de propiedad) no se reflejará en la base de datos después de que se haya registrado un esquema. La única manera de que estos cambios se reconozcan después de que el esquema se haya registrado una vez en un sistema sería volver a generar el índice y, a continuación, registrar el nuevo esquema, o bien registrar el esquema y, a continuación, crear una nueva propiedad (que consta de un nombre canónico y un PKEY) para cada versión de subequent; por ejemplo `PKEY_GroupName_PropertyNameV2` , `PKEY_GroupName_PropertyNameV3` , y así sucesivamente). No se recomienda crear nuevas propiedades de esta manera, ya que varias columnas extrañas pueden afectar al rendimiento del sistema.

 

Este tema se organiza de la siguiente manera:

-   [Metadatos](#metadata)
    -   [Abrir metadatos](#open-metadata)
-   [Acerca de los controladores de propiedades](#about-property-handlers)
-   [Tecnología heredada](#legacy-technology)
-   [Temas relacionados](#related-topics)

## <a name="metadata"></a>Metadatos

En Windows Vista y versiones posteriores, un nuevo sistema de propiedades basado en metadatos es fundamental para organizar elementos como archivos, correo electrónico y contactos. En este nuevo sistema de propiedades, se pueden buscar elementos en función de sus metadatos y los usuarios pueden leer o escribir esos metadatos. Los metadatos de este sistema se representan mediante un conjunto extensible de *propiedades* implementadas como pares de nombre/valor.

En Windows Vista y versiones posteriores, un amplio conjunto de propiedades cubre las características específicas de los elementos, como fotos, música, documentos, mensajes, contactos y archivos. Los fabricantes de software independientes (ISV) pueden introducir sus propias propiedades en la plataforma si ninguna propiedad existente satisface sus necesidades.

### <a name="open-metadata"></a>Abrir metadatos

El sistema de propiedades de Windows Vista y versiones posteriores es un sistema de metadatos abierto. Un formato de archivo almacena cualquier propiedad que se le haya asignado y expone ese valor cuando se consulta, independientemente de su relevancia o significado. Esto permite a los desarrolladores de terceros adjuntar propiedades adicionales al archivo sin necesidad de un cambio en el controlador de propiedad asociado a él. Los metadatos abiertos son un concepto eficaz. Para obtener más información sobre cómo admitir los metadatos abiertos para un formato de archivo basado en XML, vea "compatibilidad con metadatos abiertos" en [inicializar controladores de propiedades](./building-property-handlers-property-handlers.md).

> [!Note]  
> Los controladores de propiedades siempre se asocian a tipos de archivo específicos; por lo tanto, si el formato de archivo contiene propiedades que requieren un controlador de propiedades personalizado, debe registrar siempre una extensión de nombre de archivo única para cada formato de archivo.

 

## <a name="about-property-handlers"></a>Acerca de los controladores de propiedades

En Windows Vista y versiones posteriores, Windows tiene un sistema de propiedades extensible para almacenar y recuperar metadatos en los archivos y elementos de datos a los que se tiene acceso. El explorador de Windows y el sistema de Windows Search, junto con otras aplicaciones, utilizan controladores de propiedades para leer y modificar estos metadatos. Si es un desarrollador que posee un tipo de archivo específico, debe registrar un controlador de propiedades para proporcionar al sistema de propiedades acceso a los metadatos de los archivos. En algunos casos, es posible que pueda usar un controlador de propiedades existente que pueda leer y comprender el formato de archivo y sus propiedades. en otros casos, puede que necesite desarrollar un nuevo controlador de propiedades para el tipo de archivo.

El primer paso para escribir un controlador de propiedades es considerar qué propiedades admite el tipo de archivo. Los valores de propiedad se almacenan en el flujo de archivo, principalmente para habilitar la transferencia. Cuando los valores de propiedad se almacenan en el propio archivo, tal como están en este sistema, un usuario puede copiar un archivo en otro equipo, una unidad flash USB u otro sistema de archivos, o bien enviar el archivo como datos adjuntos de correo electrónico, las propiedades viajan con el archivo y no se pierden ni se pierden. Por lo tanto, si el formato de archivo admite el almacenamiento de información adicional, es mejor almacenar las propiedades en el propio archivo.

El siguiente paso consiste en determinar qué propiedades debe proporcionar el archivo. En principio, puede pensar que un conjunto limitado de propiedades es adecuado. Un archivo de audio podría admitir solo propiedades relacionadas con el audio y finalizar allí. Sin embargo, ese archivo de audio puede ser un registro de una sesión de un tribunal de justicia, archivado por una empresa judicial. En ese caso, el bufete de la ley querrá asociar otras propiedades que no sean de audio a este archivo, como el número de caso. Es posible que el proveedor del formato de archivo de audio no pueda determinar todos los escenarios en los que nunca se usará su formato. Por lo tanto, deben considerar la posibilidad de habilitar el almacenamiento global de cualquier propiedad arbitraria compatible con el sistema de propiedades.

## <a name="legacy-technology"></a>Tecnología heredada

La tecnología de secuencias secundarias del sistema de archivos de Microsoft Windows NT (NTFS) se desarrolló para admitir la persistencia de información adicional con el archivo a través de un conjunto de flujos alternativo en la capa del sistema de archivos. Es posible que se pregunte por qué esas secuencias secundarias no se usan como método principal para almacenar propiedades, especialmente con la compatibilidad con metadatos abiertos. El motivo principal es la portabilidad de esta información adicional. Desafortunadamente, estas secuencias alternativas se quitan en muchos escenarios, como la compatibilidad con el almacenamiento en caché del lado cliente (CSC), el envío de archivos como datos adjuntos y la copia de archivos en un almacén que no es NTFS.

Las secuencias secundarias no proporcionan una solución sólida en la que se garantiza que las propiedades viajan con el archivo y, por lo tanto, el sistema de propiedades de Windows Vista no proporciona un mecanismo integrado que aprovecha las secuencias NTFS secundarias para el almacenamiento de propiedades. También se recomienda encarecidamente que los ISV creen controladores de propiedades que usen secuencias secundarias para el almacenamiento de propiedades. Por supuesto, hay escenarios en los que las secuencias secundarias de NTFS son adecuadas, especialmente cuando las aplicaciones pueden garantizar que el archivo con el que están tratando siempre se almacenan en un volumen NTFS y no se recorren como resultado de la interacción del usuario final.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar nombres de tipo](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Usar listas de propiedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inicializar controladores de propiedades](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrar y distribuir controladores de propiedades](./prophand-reg-dist.md)
</dt> <dt>

[Prácticas recomendadas y preguntas más frecuentes sobre controladores de propiedades](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
