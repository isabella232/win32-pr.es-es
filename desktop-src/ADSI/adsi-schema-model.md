---
title: Modelo de esquema ADSI
description: Un esquema es similar a un diccionario en que contiene la definición de cada tipo de objeto conocido por un servicio de directorio.
ms.assetid: 70561a11-1560-4b1c-a999-e2a7b2002ab0
ms.tgt_platform: multiple
keywords:
- ADSI Schema Model ADSI
- ADSI ADSI , about, schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfd8c06d10e05c11b2cc7c578814bb4ded2d897d3b7913b9b3d341a8a6c49086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023753"
---
# <a name="adsi-schema-model"></a>Modelo de esquema ADSI

Un esquema es similar a un diccionario en que contiene la definición de cada tipo de objeto conocido por un servicio de directorio. Las aplicaciones cliente adsi pueden examinar un esquema para detectar las características de cualquier implementación de ADSI determinada. Además, ADSI proporciona interfaces de administración de esquemas que se pueden usar para comunicarse con el esquema subyacente de un servicio de directorio.

Algunos esquemas son extensibles y los proveedores adsi o proveedores de terceros pueden optar por publicar nuevas interfaces o propiedades adicionales para las interfaces existentes allí. Los clientes ADSI usan estos datos para determinar qué características se admiten para cada servicio de directorio.

Hay tres tipos de objetos de esquema: clases, propiedades y sintaxis, cada uno de los que admiten respectivamente las interfaces de administración de esquemas [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)e [**IADsSyntax.**](/windows/desktop/api/Iads/nn-iads-iadssyntax)

> [!Note]  
> La clase es un término sobrecargado. Hay clases de C++, clases de Java, clases COM y clases ADSI. En este documento, la palabra class, a menos que se califice de otro modo, hace referencia a una categoría o tipo de objeto de esquema.

 

ADSI abstrae el esquema de cada servicio de directorio y lo coloca en cada nodo raíz de nivel superior del objeto **Namespace.** Para identificar qué clases admite un servicio de directorio en un nodo raíz determinado, enumere el objeto de esquema y obtenga una lista de objetos de clase, objetos de propiedad y objetos de sintaxis. Para obtener más información, [vea Using the ADSI Schema](using-the-adsi-schema.md).

## <a name="adsi-ldap-provider-schema-cache"></a>Caché de esquemas del proveedor LDAP ADSI

El proveedor LDAP para ADSI intenta almacenar en caché los datos de esquema en el equipo local. Un subesquema se identifica mediante un nombre distintivo almacenado en el atributo [**subSchemaSubEntry**](/windows/desktop/ADSchema/a-subschemasubentry) ubicado en la raíz de la empresa del servicio de directorio (rootDSE). Además de proporcionar los datos de subesquema, los servidores LDAP v3 deben exponer un atributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) que se usa para determinar la última vez que se modificó el esquema.

Cuando ADSI se enlaza por primera vez al servidor LDAP, recupera los datos de subesquema mediante el [**atributo subSchemaSubEntry.**](/windows/desktop/ADSchema/a-subschemasubentry) Si ADSI encuentra correctamente el objeto de subesquema, almacena un puntero a los datos del Registro en el equipo que se conecta al servidor LDAP. Para obtener información sobre exactamente dónde se almacenan estos valores en el Registro, vea [ADSI y Control de cuentas de usuario.](adsi-and-uac.md)

ADSI intenta procesar los datos del esquema y lee el [**atributo modifyTimeStamp.**](/windows/desktop/ADSchema/a-modifytimestamp) Si el atributo **modifyTimeStamp** existe y ADSI procesa correctamente el esquema, ADSI escribe el subesquema en el disco y crea los dos valores del Registro siguientes en la clave. Si los datos de subesquema existen, pero no se pueden procesar, no se crea ninguno de estos valores del Registro:

-   Valor **Time,** que contiene el [**atributo modifyTimeStamp.**](/windows/desktop/ADSchema/a-modifytimestamp) Este valor se usa para asegurarse de que los datos del esquema están actuales y evita la recarga constante de los datos del esquema.
-   Valor **De** archivo, que contiene la ruta de acceso a donde ADSI almacena los datos de esquema en el sistema de archivos. De forma predeterminada, ADSI almacena en caché el subesquema en el directorio SchCache con un nombre de archivo correspondiente al nombre <systemroot> \\ del servidor LDAP.

Si se pueden procesar los datos del subesquema, pero no se expone ningún atributo [**modifyTimeStamp,**](/windows/desktop/ADSchema/a-modifytimestamp) los datos del esquema se almacenan en caché en la memoria, pero no se escriben en el disco. Si se ha contactado con un servidor LDAP v3 a través de ADSI en el equipo local y no hay un subesquema almacenado en caché, lo más probable es que se deba a uno de los siguientes motivos:

-   El servidor no exponía las propiedades correctas.
-   ADSI no pudo procesar el esquema.
-   ADSI no pudo escribir el archivo en el sistema de archivos.

 

 