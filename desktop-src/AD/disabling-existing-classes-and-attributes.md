---
title: Deshabilitar clases y atributos existentes
description: Las adiciones de esquema son permanentes.
ms.assetid: 13ffd2f5-cf1d-4cde-a3d5-74cb5a44b6fc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a783bc0898cf3ecc883865abde037d1e70c60ec83913f2fb9148e230ae392f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118018814"
---
# <a name="disabling-existing-classes-and-attributes"></a>Deshabilitar clases y atributos existentes

Las adiciones de esquema son permanentes. No se pueden eliminar **objetos attributeSchema** **y classSchema.** En un sistema distribuido, es difícil garantizar que no haya instancias de una clase o atributo determinados. Al quitar la definición de una clase o atributo, se dañan las instancias existentes de esa clase o atributo.

Puede deshabilitar una clase o atributo existente si lo marca como "defunct". Esto no afecta a las instancias existentes de la clase o atributo tan marcados, pero impide la creación de nuevas instancias.

Las restricciones siguientes se aplican al deshabilitar clases y atributos de esquema:

-   No se puede deshabilitar una clase o atributo de categoría 1.
-   No se puede deshabilitar un atributo que sea miembro de una clase que no esté también deshabilitada. Esto se debe a que es posible que se requiera un atributo para la clase (no deshabilitada) y deshabilitar el atributo impide que se cree nuevas instancias de la clase.

Para deshabilitar un atributo, establezca el **atributo isDefunct** de su **objeto attributeSchema** en **TRUE.** Cuando se deshabilita un atributo, no se pueden crear nuevas instancias del atributo. Para volver a habilitar el atributo, establezca **el atributo isDefunct** en **FALSE.**

Para deshabilitar una clase, establezca el **atributo isDefunct** de su **objeto classSchema** en **TRUE.** Cuando una clase está deshabilitada, no se pueden crear nuevas instancias de la clase . Para volver a habilitar la clase, establezca el **atributo isDefunct** en **FALSE.**

El establecimiento de objetos de esquema como en desa desarrollo puede ser útil en entornos de producción. Cuando ya no se necesite una versión de prueba de una extensión de esquema, mónquela como defunta. Puede restaurarlo quitando el atributo **isDefunct** o estableciendo el valor del atributo en **FALSE.** Esto también protege contra una eliminación no intencionada de un objeto de esquema al establecerlo en defunción porque la operación se puede invertir fácilmente.

Tenga en cuenta que Active Directory servidor no limpia las instancias existentes de un atributo o clase al hacer que un objeto de esquema esté en deserción. Si quita la **propiedad isDefunct,** las instancias se vuelven objetos normales válidos de nuevo.

En la lista siguiente se incluyen otras consecuencias de marcar **un objeto attributeSchema** o **classSchema** en deserción:

-   Se produce un error en la adición o modificación de una instancia.
-   Los códigos de error se comportan como si nunca existiera una clase en deserción.
-   La búsqueda y eliminación se comportan como si no hubiera objetos de esquema que se hubieran dejado de hacer.
-   Permitir solo la eliminación de todo el atributo del objeto.

En la lista siguiente se incluyen opciones adicionales en un entorno de producción para reducir el impacto de las extensiones de esquema inactivas:

-   Quite todos **los valores de atributo mayAttribute** de una clase en deserción.
-   Reduzca el tamaño de todos los **valores de atributo mustAttribute** de una clase en deserción.
-   Quite un atributo en des estado del catálogo global.
-   Quite un atributo en des estado de cualquier índice.

Otras opciones para quitar cambios de esquema no deseados en un entorno de producción son para que los desarrolladores usen un controlador de dominio privado para las pruebas. En este caso, puede:

-   "Restablecer" el servidor Active Directory mediante Dcpromo.exe para degradar el controlador de dominio. Una vez completada la degradación, use Dcpromo.exe para volver a promover el servidor a un controlador de dominio. A continuación, el desarrollador puede usar scripts LDIF para volver a cargar las clases, atributos e instancias de objeto necesarias.
-   Use Ntbackup.exe para realizar una copia de seguridad del estado del sistema en una partición de disco disponible. Reinicie para Caja fuerte/Modo de restauración del servicio de directorio para restaurar.

En el caso de los sistemas operativos de Windows Server 2003, al establecer una clase o atributo en desuso, puede reutilizar inmediatamente los valores **ldapDisplayName**, **schemaIdGuid,** **OID** y **mapiID** del elemento de esquema en desuso al crear una nueva clase o atributo para reemplazarlo. La versión en deserción de la clase o atributo se mantiene en el contenedor Schema, pero está oculta en el complemento MMC. Para reactivar el elemento de esquema anterior, establezca **isDefunct** en **FALSE.**

En el siguiente ejemplo de código LDIF se muestra cómo modificar el atributo **isDefunct** y cambiar el RDN para que no se confunda con la nueva clase que se crea para reemplazarlo.

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

Use el siguiente comando para ejecutar el ejemplo de código LDIF en un bosque para un equipo que se ejecuta en Windows server 2003.

**ldifde /i /f rdn.ldf /c "DC=X" "dc=mydomain,dc=com"**

(Donde "DC=X" es una constante)

 

 




