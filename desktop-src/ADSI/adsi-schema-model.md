---
title: Modelo de esquema ADSI
description: Un esquema es similar a un diccionario en que contiene la definición de cada tipo de objeto conocido para un servicio de directorio.
ms.assetid: 70561a11-1560-4b1c-a999-e2a7b2002ab0
ms.tgt_platform: multiple
keywords:
- ADSI del modelo de esquema ADSI
- ADSI ADSI, acerca de, esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23eec9264ae2692952106802cc06cbad937a42a9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995623"
---
# <a name="adsi-schema-model"></a>Modelo de esquema ADSI

Un esquema es similar a un diccionario en que contiene la definición de cada tipo de objeto conocido para un servicio de directorio. Las aplicaciones cliente ADSI pueden examinar un esquema para detectar las características de cualquier implementación de ADSI determinada. Además, ADSI proporciona interfaces de administración de esquemas que se pueden utilizar para comunicarse con el esquema subyacente de un servicio de directorio.

Algunos esquemas son extensibles y los proveedores ADSI o proveedores de terceros pueden optar por publicar nuevas interfaces o propiedades adicionales para las interfaces existentes. Los clientes ADSI usan estos datos para determinar qué características se admiten para cada servicio de directorio.

Hay tres tipos de objetos de esquema: clases, propiedades y sintaxis, cada una de las cuales admite respectivamente las interfaces de administración de esquema [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)y [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax).

> [!Note]  
> La clase es un término sobrecargado. Hay clases de C++, clases de Java, clases COM y clases ADSI. En este documento, la palabra clase, a menos que se califique de otra manera, hace referencia a una categoría o tipo de objeto de esquema.

 

ADSI abstrae el esquema de cada servicio de directorio y lo coloca en todos los nodos raíz de nivel superior del objeto de **espacio de nombres** . Para identificar las clases que admite un servicio de directorio en un nodo raíz determinado, se enumera el objeto de esquema y se obtiene una lista de objetos de clase, objetos de propiedad y objetos de sintaxis. Para obtener más información, vea [usar el esquema ADSI](using-the-adsi-schema.md).

## <a name="adsi-ldap-provider-schema-cache"></a>Caché de esquema del proveedor LDAP de ADSI

El proveedor LDAP para ADSI intenta almacenar en caché los datos de esquema en el equipo local. Un subesquema se identifica mediante un nombre distintivo almacenado en el atributo [**subSchemaSubEntry**](/windows/desktop/ADSchema/a-subschemasubentry) situado en la raíz del servicio de directorio Enterprise (RootDSE). Además de proporcionar los datos del subesquema, los servidores LDAP v3 deben exponer un atributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) que se usa para determinar la última vez que se modificó el esquema.

Cuando ADSI se enlaza primero al servidor LDAP, recupera los datos del subesquema mediante el atributo [**subSchemaSubEntry**](/windows/desktop/ADSchema/a-subschemasubentry) . Si ADSI consigue encontrar el objeto de subesquema, almacena un puntero a los datos del registro en el equipo que se está conectando al servidor LDAP. Para obtener información sobre exactamente dónde se almacenan estos valores en el registro, consulte [ADSI y control de cuentas de usuario](adsi-and-uac.md).

ADSI intenta procesar los datos de esquema y lee el atributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) . Si el atributo **modifyTimeStamp** existe y ADSI procesa correctamente el esquema, ADSI escribe el subesquema en el disco y crea los dos valores del registro siguientes bajo la clave. Si los datos del subesquema existen, pero no se pueden procesar, no se crea ninguno de estos valores del registro:

-   Un valor de **hora** , que contiene el atributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) . Este valor se utiliza para asegurarse de que los datos del esquema están actualizados y evita la recarga constante de los datos del esquema.
-   Un valor de **archivo** , que contiene la ruta de acceso donde ADSI almacena los datos de esquema en el sistema de archivos. De forma predeterminada, ADSI almacena en caché el subesquema del <systemroot> \\ directorio SchCache con un nombre de archivo que corresponde al nombre del servidor LDAP.

Si se pueden procesar los datos del subesquema, pero no se expone ningún atributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) , los datos del esquema se almacenan en la memoria caché, pero no se escriben en el disco. Si se ha contactado con un servidor LDAP v3 a través de ADSI en el equipo local y no hay un subesquema almacenado en caché, lo más probable es que se deba a uno de los siguientes motivos:

-   El servidor no expondría las propiedades correctas.
-   ADSI no pudo procesar el esquema.
-   ADSI no pudo escribir el archivo en el sistema de archivos.

 

 