---
title: Deshabilitar clases y atributos existentes
description: Las adiciones de esquema son permanentes.
ms.assetid: 13ffd2f5-cf1d-4cde-a3d5-74cb5a44b6fc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74863d0d3c72f383259cfe262f4b7aa6fa27774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773249"
---
# <a name="disabling-existing-classes-and-attributes"></a>Deshabilitar clases y atributos existentes

Las adiciones de esquema son permanentes. No se pueden eliminar los objetos **attributeSchema** y **ClassSchema** . En un sistema distribuido, es difícil garantizar que no haya instancias de una clase o un atributo determinados. La eliminación de la definición de una clase o atributo daña las instancias existentes de esa clase o atributo.

Puede deshabilitar una clase o un atributo existente marcándolos como "inactivo". Esto no afecta a las instancias existentes de la clase o atributo, así que impide la creación de nuevas instancias.

Al deshabilitar las clases y atributos de esquema se aplican las restricciones siguientes:

-   No se puede deshabilitar una clase o atributo de categoría 1.
-   No se puede deshabilitar un atributo que sea miembro de una clase que no esté también deshabilitada. Esto se debe a que es posible que se requiera un atributo para la clase (no deshabilitada) y al deshabilitar el atributo se evita que se creen nuevas instancias de la clase.

Para deshabilitar un atributo, establezca el atributo **isDefunct** de su objeto **attributeSchema** en **true**. Cuando un atributo está deshabilitado, no se pueden crear nuevas instancias del atributo. Para volver a habilitar el atributo, establezca el atributo **isDefunct** en **false**.

Para deshabilitar una clase, establezca el atributo **isDefunct** de su objeto **ClassSchema** en **true**. Cuando se deshabilita una clase, no se pueden crear nuevas instancias de la clase. Para volver a habilitar la clase, establezca el atributo **isDefunct** en **false**.

La configuración de objetos de esquema como inactivos puede ser útil en entornos de producción. Cuando ya no se necesite una versión de prueba de una extensión de esquema, márquela como inactiva. Puede restaurarlo quitando el atributo **isDefunct** o estableciendo el valor del atributo en **false**. Esto también protege contra una eliminación imprevista de un objeto de esquema estableciéndolo en inactivo porque la operación se puede invertir fácilmente.

Tenga en cuenta que el servidor de Active Directory no limpia las instancias existentes de un atributo o clase cuando se hace que un objeto de esquema esté inactivo. Si quita la propiedad **isDefunct** , todas las instancias volverán a ser objetos normales válidos.

La lista siguiente incluye otras consecuencias de marcar un objeto **attributeSchema** o **ClassSchema** como inactivo:

-   Se produce un error al agregar o modificar una instancia.
-   Los códigos de error se comportan como si nunca existiera una clase inactiva.
-   Buscar y eliminar se comportan como si no se hubieran creado objetos de esquema inactivos.
-   Solo se permite la eliminación de un atributo completo del objeto.

La lista siguiente incluye opciones adicionales en un entorno de producción para reducir el impacto de las extensiones de esquema inactivas:

-   Quite todos los valores de atributo **mayHave** de una clase inactiva.
-   Reduzca el tamaño de todos los valores de atributo **mustHave** de una clase inactiva.
-   Quitar un atributo inactivo del catálogo global.
-   Quitar un atributo inactivo de cualquier índice.

Otras opciones para quitar los cambios de esquema no deseados en un entorno de producción son para que los desarrolladores usen un controlador de dominio privado para las pruebas. En este caso, puede:

-   "Restablezca" el servidor de Active Directory mediante Dcpromo.exe para disminuir de nivel el controlador de dominio. Una vez finalizada la degradación, vuelva a usar Dcpromo.exe para promover el servidor a un controlador de dominio. A continuación, el desarrollador puede usar scripts LDIF para volver a cargar las clases, los atributos y las instancias de objeto necesarios.
-   Use Ntbackup.exe para realizar una copia de seguridad del estado del sistema en una partición de disco disponible. Reinicie el modo seguro o de restauración del servicio de directorio para restaurar.

En el caso de los sistemas operativos Windows Server 2003, cuando se establece una clase o un atributo en inactivo, se pueden volver a usar inmediatamente los valores **LDAPDisplayName**, **schemaIdGuid**, **OID** y **mapiID** del elemento de esquema inactivo al crear una nueva clase o atributo para reemplazarlo. La versión inactiva de la clase o atributo se mantiene en el contenedor de esquema, pero está oculta en el complemento MMC. Para reactivar el elemento de esquema anterior, establezca **isDefunct** en **false**.

En el ejemplo de código LDIF siguiente se muestra cómo modificar el atributo **isDefunct** y cambiar el RDN para que no se confunda con la nueva clase que se crea para reemplazarlo.

``` syntax
 dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modify
   replace: isDefunct
   isDefunct: TRUE
   -

   dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modrdn
   newrdn: cn=MyClassOld
   deleteoldrdn: 1

   dn:
   changetype: modify
   add: schemaUpdateNow
   schemaUpdateNow: 1
   -
```

Use el siguiente comando para ejecutar el ejemplo de código LDIF en un bosque de un equipo que se ejecuta en sistemas operativos Windows Server 2003.

**LDIFDE/i/f RDN. ldf/c "DC = X" "DC = miDominio, DC = com"**

(Donde "DC = X" es una constante)

 

 




