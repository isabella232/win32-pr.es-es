---
title: Crear grupos en un dominio
description: Se crea un objeto de grupo Active Directory Domain Services en el contenedor de dominio donde se incluirá el nuevo grupo.
ms.assetid: 40792878-4219-4242-8cf7-b092b28f2ff4
ms.tgt_platform: multiple
keywords:
- groups AD , crear grupos en un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e2f0811e54707d0cfcc2e2efecfac33199e47d1bebd70ac7ee7e2900d8779bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020342"
---
# <a name="creating-groups-in-a-domain"></a>Crear grupos en un dominio

Se crea un objeto de grupo Active Directory Domain Services en el contenedor de dominio donde se incluirá el nuevo grupo. Los grupos se pueden crear en la raíz del dominio, dentro de una unidad organizativa o dentro de un contenedor. Para crear un objeto de grupo, use [**los métodos IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) o [**IDirectoryObject::CreateDSObject.**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject)

Los atributos siguientes son necesarios para convertir el objeto de grupo en un grupo legal que el servidor Active Directory y el Windows de seguridad del grupo reconocerán:

<dl> <dt>

<span id="cn"></span><span id="CN"></span>**Cn**
</dt> <dd>

Especifica el nombre del objeto de grupo en el directorio . Este será el nombre distintivo relativo del objeto dentro del contenedor donde se crea el grupo.

</dd> <dt>

<span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**
</dt> <dd>

Contiene un entero que especifica el tipo de grupo y el ámbito. La [**\_ enumeración ADS GROUP \_ TYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) define los valores posibles para el **atributo groupType.**

En la lista siguiente se definen los tipos de grupo y los valores comunes para este atributo.

<dl> <dt>

<span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Distribución local de dominio
</dt> <dd>

**GRUPO DE \_ ANUNCIOS \_ TIPO GRUPO LOCAL \_ DE \_ \_ DOMINIO**

</dd> <dt>

<span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Seguridad local del dominio
</dt> <dd>

**ADS \_ TIPO DE \_ GRUPO \_ DOMINIO GRUPO \_ LOCAL \_** \| **ADS GROUP TYPE \_ SECURITY \_ \_ \_ ENABLED**

</dd> <dt>

<span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Distribución global
</dt> <dd>

**GRUPO DE \_ \_ ANUNCIOS TIPO \_ GRUPO \_ GLOBAL**

</dd> <dt>

<span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Seguridad global
</dt> <dd>

**ADS \_ TIPO DE \_ GRUPO \_ GLOBAL GROUP \_ ADS** \| **GROUP TYPE \_ SECURITY \_ \_ \_ ENABLED**

</dd> <dt>

<span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Distribución universal
</dt> <dd>

**GRUPO DE \_ \_ ANUNCIOS TIPO \_ GRUPO \_ UNIVERSAL**

</dd> <dt>

<span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Seguridad universal
</dt> <dd>

**ADS \_ TIPO DE \_ GRUPO \_ UNIVERSAL \_ GROUP** \| **ADS GROUP TYPE \_ SECURITY \_ \_ \_ ENABLED**

</dd> <dt>


</dt> <dd>

</dd> </dl>

Si el grupo está pensado para establecer el control de acceso en objetos de directorio, el grupo debe ser un grupo de seguridad global o de seguridad universal.

Tenga en cuenta que los grupos de seguridad universal solo se pueden crear Windows 2000 dominios que se ejecutan en modo nativo. Para obtener más información sobre cómo detectar el modo mixto y nativo, vea Detectar el [modo de operación de un dominio](detecting-the-operation-mode-of-a-domain.md).

</dd> <dt>

<span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**Samaccountname**
</dt> <dd>

Contiene una cadena que es el nombre usado para admitir clientes y servidores de una versión anterior. **SAMAccountName** debe tener menos de 20 caracteres para admitir clientes de una versión anterior de Windows.

**sAMAccountName** debe ser único entre todos los objetos de entidad de seguridad dentro del dominio. Se debe realizar una consulta en el dominio para comprobar que **sAMAccountName** es único dentro del dominio.

</dd> </dl>

Los miembros del grupo se pueden agregar en el momento de la creación mediante el [**método IDirectoryObject::CreateDSObject.**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) Opcionalmente, los miembros se pueden agregar al grupo después de su creación mediante [**el método IADsGroup::Add.**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) Para obtener más información sobre cómo agregar miembros a un grupo, vea [Agregar miembros a grupos en un dominio](adding-members-to-groups-in-a-domain.md).

 

 