---
description: Las propiedades se representan mediante identificadores conocidos como identificadores de propiedad (PID).
ms.assetid: a773c7b3-a1a2-4cce-ae5f-b54217ea06f4
title: Descripción de los controladores de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42139a869551f0f4dc786f02c66c673a49495ba01f5258aeeff12051bd3f60b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119946975"
---
# <a name="understanding-property-handlers"></a>Descripción de los controladores de propiedades

Las propiedades se representan mediante identificadores conocidos como identificadores de propiedad (PID). Cada propiedad DEBE tener un identificador único global (GUID). Este identificador consta de un GUID, que representa una colección de propiedades denominada conjunto de propiedades más una cadena o un entero de 32 bits para identificar la propiedad dentro del conjunto. Si se usa la forma de entero de id., los valores 0x00000000, 0xFFFFFFFF y 0xFFFFFFFE se consideran no válidos. Los proveedores pueden garantizar que sus propiedades se definen de forma única colocándolas en un conjunto de propiedades definido por sus propios GUID.

> [!IMPORTANT]
> Es fundamental definir las propiedades de forma cuidadosa y estratégica para la primera versión del esquema. Los cambios en las propiedades personalizadas (como el ancho de columna o el tipo de propiedad) no se reflejarán en la base de datos después de registrar un esquema. La única manera de que se reconozcan estos cambios después de registrar el esquema una vez en un sistema sería volver a generar el índice y, a continuación, registrar el nuevo esquema, o registrar el esquema y, a continuación, crear una nueva propiedad (que consta de un nombre canónico y un PKEY) para cada versión subequente. por `PKEY_GroupName_PropertyNameV2` ejemplo, `PKEY_GroupName_PropertyNameV3` , , etc.). No se recomienda crear nuevas propiedades de esta manera, ya que varias columnas externas pueden afectar al rendimiento del sistema.

 

Este tema se organiza de la siguiente manera:

-   [Metadata](#metadata)
    -   [Abrir metadatos](#open-metadata)
-   [Acerca de los controladores de propiedades](#about-property-handlers)
-   [Tecnología heredada](#legacy-technology)
-   [Temas relacionados](#related-topics)

## <a name="metadata"></a>Metadatos

En Windows Vista y versiones posteriores, un nuevo sistema de propiedades basado en metadatos es fundamental para organizar elementos como archivos, correo electrónico y contactos. En este nuevo sistema de propiedades, se pueden buscar elementos en función de sus metadatos y los usuarios pueden leer o escribir los metadatos. Los metadatos de este sistema se representan mediante un conjunto extensible de *propiedades* implementadas como pares nombre-valor.

En Windows Vista y versiones posteriores, un amplio conjunto de propiedades cubre los detalles de elementos como fotos, música, documentos, mensajes, contactos y archivos. Los proveedores de software independientes (ISV) pueden presentar sus propias propiedades a la plataforma si ninguna propiedad existente satisface sus necesidades.

### <a name="open-metadata"></a>Abrir metadatos

El sistema de propiedades de Windows Vista y versiones posteriores es un sistema de metadatos abierto. Un formato de archivo almacena cualquier propiedad asignada y expone ese valor cuando se consulta, independientemente de su relevancia o significado. Esto permite a los desarrolladores de terceros adjuntar propiedades adicionales al archivo sin necesidad de un cambio en el controlador de propiedades asociado a él. Los metadatos abiertos son un concepto eficaz. Para obtener más información sobre cómo admitir metadatos abiertos para un formato de archivo basado en XML, vea "Admitir metadatos abiertos" en [Inicializar](./building-property-handlers-property-handlers.md)controladores de propiedades .

> [!Note]  
> Los controladores de propiedades siempre están asociados a tipos de archivo específicos; Por lo tanto, si el formato de archivo contiene propiedades que requieren un controlador de propiedades personalizado, siempre debe registrar una extensión de nombre de archivo única para cada formato de archivo.

 

## <a name="about-property-handlers"></a>Acerca de los controladores de propiedades

En Windows Vista y versiones posteriores, Windows un sistema de propiedades extensible para almacenar y recuperar metadatos en los archivos y elementos de datos a los que tiene acceso. Windows El Explorador y el Windows Search, junto con otras aplicaciones, usan controladores de propiedades para leer y modificar estos metadatos. Si es un desarrollador propietario de un tipo de archivo específico, debe registrar un controlador de propiedades para proporcionar al sistema de propiedades acceso a los metadatos de los archivos. En algunos casos, es posible que pueda usar un controlador de propiedades existente que pueda leer y comprender el formato de archivo y sus propiedades. En otros casos, es posible que tenga que desarrollar un nuevo controlador de propiedades para el tipo de archivo.

El primer paso para escribir un controlador de propiedades es tener en cuenta las propiedades que admite el tipo de archivo. Los valores de propiedad se almacenan en la secuencia de archivos, principalmente para habilitar la transportabilidad. Cuando los valores de propiedad se almacenan en el propio archivo, como en este sistema, un usuario puede copiar un archivo en otro equipo, una unidad flash USB u otro sistema de archivos, o enviar el archivo como datos adjuntos de correo electrónico, las propiedades viajan con el archivo y nunca se pierden ni se sincronizan. Por lo tanto, si el formato de archivo admite el almacenamiento de información adicional, es mejor almacenar las propiedades en el propio archivo.

El siguiente paso consiste en determinar qué propiedades debe proporcionar el archivo. Inicialmente, podría pensar que un conjunto limitado de propiedades es adecuado. Un archivo de audio solo podría admitir propiedades relacionadas con audio y terminar allí. Sin embargo, ese archivo de audio podría ser una grabación de una sesión de un abogado, archivada por un estudio de abogados. En ese caso, el abogado ciertamente querrá asociar otras propiedades que no son de audio a este archivo, como el número de caso. El proveedor del formato de archivo de audio no puede determinar posiblemente todos los escenarios en los que se usará su formato. Por lo tanto, deben considerar la posibilidad de habilitar el almacenamiento de las propiedades arbitrarias admitidas por el sistema de propiedades.

## <a name="legacy-technology"></a>Tecnología heredada

La tecnología de flujo secundario del sistema de archivos DE MICROSOFT Windows NT (NTFS) se desarrolló para admitir la persistencia de información adicional con el archivo a través de un flujo alternativo establecido en la capa del sistema de archivos. Es posible que se pregunte por qué esas secuencias secundarias no se usan como método principal para almacenar propiedades, especialmente con compatibilidad con metadatos abiertos. La razón principal es la transportabilidad de esta información adicional. Desafortunadamente, estas secuencias alternativas se quitan en muchos escenarios, incluida la compatibilidad con el almacenamiento en caché del lado cliente (CSC), el envío de archivos como datos adjuntos y la copia de archivos a un almacén que no es NTFS.

Las secuencias secundarias no proporcionan una solución sólida en la que se garantiza que las propiedades viajen con el archivo y, por tanto, el sistema de propiedades Windows Vista no proporciona un mecanismo integrado que aproveche las secuencias NTFS secundarias para el almacenamiento de propiedades. También se desaconseja encarecidamente a los ISV la creación de controladores de propiedades que usan secuencias secundarias para el almacenamiento de propiedades. Por supuesto, hay escenarios en los que los flujos secundarios NTFS son adecuados, especialmente cuando las aplicaciones pueden garantizar que el archivo con el que están trabajando siempre se almacena en un volumen NTFS y no viajará como resultado de la interacción del usuario final.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar nombres de tipo](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Usar listas de propiedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inicialización de controladores de propiedades](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registro y distribución de controladores de propiedades](./prophand-reg-dist.md)
</dt> <dt>

[Procedimientos recomendados y preguntas más frecuentes sobre el controlador de propiedades](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
