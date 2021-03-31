---
title: Crear grupos en un dominio
description: Se crea un objeto de grupo en Active Directory Domain Services en el contenedor de dominio donde se incluirá el nuevo grupo.
ms.assetid: 40792878-4219-4242-8cf7-b092b28f2ff4
ms.tgt_platform: multiple
keywords:
- agrupa AD, crear grupos en un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100700b08fb82b750ee68dfed6bcb26060929e87
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077542"
---
# <a name="creating-groups-in-a-domain"></a>Crear grupos en un dominio

Se crea un objeto de grupo en Active Directory Domain Services en el contenedor de dominio donde se incluirá el nuevo grupo. Los grupos se pueden crear en la raíz del dominio, dentro de una unidad organizativa o dentro de un contenedor. Para crear un objeto de grupo, use el método [**IADsContainer:: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) o [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .

Los atributos siguientes son necesarios para convertir el objeto de grupo en un grupo legal que reconozcan el servidor de Active Directory y el sistema de seguridad de Windows:

<dl> <dt>

<span id="cn"></span><span id="CN"></span>**CN**
</dt> <dd>

Especifica el nombre del objeto de grupo en el directorio. Este será el nombre distintivo relativo del objeto dentro del contenedor donde se crea el grupo.

</dd> <dt>

<span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**
</dt> <dd>

Contiene un entero que especifica el tipo y el ámbito de grupo. La enumeración de enumeración de [**\_ \_ tipo \_ de grupo ADS**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) define los valores posibles para el atributo **GroupType** .

En la lista siguiente se definen los tipos y valores de grupo comunes para este atributo.

<dl> <dt>

<span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Distribución local de dominio
</dt> <dd>

**tipo de grupo de ADS \_ \_ \_ \_ grupo local de dominio \_**

</dd> <dt>

<span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Seguridad local de dominio
</dt> <dd>

**Anuncios \_ de tipo de grupo de grupo \_ \_ local de dominio \_ \_** \| **ADS seguridad de grupo \_ \_ \_ \_ habilitada**

</dd> <dt>

<span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Distribución global
</dt> <dd>

**\_ \_ grupo global de tipo de grupo de \_ ADS \_**

</dd> <dt>

<span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Seguridad global
</dt> <dd>

**Anuncios \_ de tipo de grupo de grupo de ADS de \_ \_ \_ grupo global** \| **\_ \_ \_ \_ habilitado para seguridad**

</dd> <dt>

<span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Distribución universal
</dt> <dd>

**tipo de grupo de ADS \_ \_ \_ \_ grupo universal**

</dd> <dt>

<span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Seguridad universal
</dt> <dd>

**Anuncios \_ de tipo de grupo de grupo de ADS de \_ \_ \_ grupo universal** \| **\_ \_ \_ \_ habilitado para seguridad**

</dd> <dt>


</dt> <dd>

</dd> </dl>

Si el grupo está pensado para establecer el control de acceso en los objetos de directorio, el grupo debe ser un grupo de seguridad global o de seguridad universal.

Tenga en cuenta que los grupos de seguridad universal solo se pueden crear en los dominios de Windows 2000 que se ejecutan en modo nativo. Para obtener más información acerca de cómo detectar el modo mixto y nativo, consulte [detectar el modo de operación de un dominio](detecting-the-operation-mode-of-a-domain.md).

</dd> <dt>

<span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**Atributo**
</dt> <dd>

Contiene una cadena que es el nombre que se usa para admitir clientes y servidores de una versión anterior. **SamAccountName** debe tener menos de 20 caracteres para admitir clientes de una versión anterior de Windows.

**SamAccountName** debe ser único entre todos los objetos de entidad de seguridad del dominio. Se debe realizar una consulta en el dominio para comprobar que **samAccountName** es único en el dominio.

</dd> </dl>

Los miembros del grupo se pueden agregar en el momento de la creación mediante el método [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) . Opcionalmente, los miembros se pueden agregar al grupo después de la creación mediante el método [**IADsGroup:: Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) . Para obtener más información sobre cómo agregar miembros a un grupo, consulte [Agregar miembros a grupos en un dominio](adding-members-to-groups-in-a-domain.md).

 

 