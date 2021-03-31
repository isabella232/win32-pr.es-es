---
title: Selector de objetos de directorio
description: El cuadro de diálogo Selector de objetos de directorio permite al usuario seleccionar uno o más objetos del catálogo global, un dominio o un equipo o un grupo de trabajo.
ms.assetid: 5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a
ms.tgt_platform: multiple
keywords:
- AD de selector de objetos de directorio
- Selector de objetos AD
- objetos AD, selector de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f6ba7fd053aa8ab3245bf72c693f0a887aa983
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077529"
---
# <a name="directory-object-picker"></a>Selector de objetos de directorio

El cuadro de diálogo Selector de objetos de directorio permite al usuario seleccionar uno o más objetos del catálogo global, un dominio o un equipo o un grupo de trabajo. Los tipos de objeto entre los que un usuario puede seleccionar son los objetos de usuario, contacto, grupo y equipo. Para obtener más información acerca de Active Directory Domain Services, vea [Active Directory Domain Services](active-directory-domain-services.md).

Para mostrar un cuadro de diálogo Selector de objetos:

1.  Llame a la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) para crear una instancia de la interfaz [**IDsObjectPicker**](/windows/desktop/api/Objsel/nn-objsel-idsobjectpicker) .
2.  Llame al método [**IDsObjectPicker:: Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) para inicializar el cuadro de diálogo.
3.  Llame al método [**IDsObjectPicker:: InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog) para mostrar el cuadro de diálogo.
4.  Llame al método [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) de la instancia de [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) que devuelve el cuadro de diálogo Selector de objetos para recuperar los datos de la [**lista de selección de CFSTR \_ DSOP \_ DS \_ \_**](cfstr-dsop-ds-selection-list.md) . El formato del portapapeles de la **\_ \_ \_ \_ lista de selección DS de CFSTR DSOP** proporciona un **HGLOBAL** que contiene una estructura de [**lista de \_ selección \_ de DS**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) . La estructura de la **\_ \_ lista de selección de DS** contiene datos sobre los elementos seleccionados en el cuadro de diálogo Selector de objetos.

Si se requiere el identificador de seguridad (SID) para un objeto, debe solicitarse directamente desde el selector de objetos agregando el atributo **objectSid** a la lista de atributos que se van a recuperar para el objeto seleccionado. No se recomienda pasar el nombre de objeto devuelto a la función [**LsaLookupNames**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames) o [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) porque la búsqueda de nombre será redundante y puede producir un error en algunos casos.

Si se va a guardar una referencia a los objetos seleccionados, el nombre distintivo no se debe guardar porque el objeto puede moverse, cambiarse de nombre o puede cambiar debido a las diferencias de configuración regional. En el caso de las entidades de seguridad, se debe solicitar el **objectSid** para el objeto y guardarlo de forma segura. Si más adelante se necesita el nombre de la entidad de seguridad, se puede recuperar con la función [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) . En el caso de todos los demás objetos, debe solicitarse y guardarse el **objectGUID** .

## <a name="initialization"></a>Inicialización

Cuando se inicializa el cuadro de diálogo Selector de objetos, se especifica un conjunto de tipos de ámbito y filtros. Los tipos de ámbito especificados determinan las ubicaciones, los dominios o los equipos, por ejemplo, desde el que un usuario puede seleccionar objetos. Los filtros determinan los tipos de objetos que un usuario puede seleccionar a partir de un tipo de ámbito determinado. Para obtener más información, vea la sección ámbitos y filtros más adelante.

De forma predeterminada, un usuario puede seleccionar un solo objeto en el cuadro de diálogo Selector de objetos de directorio. Para habilitar las selecciones múltiples, establezca la marca DSOP de la **\_ marca de \_ selección** múltiple en el miembro **flOptions** de la estructura [**DSOP \_ init \_ info**](/windows/desktop/api/Objsel/ns-objsel-dsop_init_info) al inicializarse el cuadro de diálogo.

## <a name="scopes-and-filters"></a>Ámbitos y filtros

La lista desplegable **Buscar en** contiene los ámbitos de los que un usuario puede seleccionar objetos. Un ámbito es un dominio, un equipo, un grupo de trabajo o un catálogo global que almacena datos sobre y proporciona acceso a un conjunto de objetos disponibles. Las entradas de la lista de ámbitos dependen de los tipos de ámbito y el equipo de destino especificado cuando se llamó por última vez al método [**IDsObjectPicker:: Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) para inicializar el cuadro de diálogo Selector de objetos.

Un tipo de ámbito es una categoría genérica de ámbitos, como todos los dominios de la empresa a los que pertenece el equipo de destino, o el catálogo global de la empresa del equipo de destino o el propio equipo de destino. Para cada tipo de ámbito especificado, el cuadro de diálogo utiliza el contexto del equipo de destino para determinar las entradas de la lista de ámbitos.

El método [**IDsObjectPicker:: Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) toma un puntero a una estructura de [**información de DSOP \_ init \_**](/windows/desktop/api/Objsel/ns-objsel-dsop_init_info) que contiene una matriz de estructuras de [**\_ \_ \_ información de ámbito de DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_scope_init_info) . Cada entrada de la matriz de **información de DSOP \_ Scope \_ init \_** especifica uno o varios tipos de ámbito, así como los filtros aplicables y otros atributos. Los filtros determinan los tipos de objetos, como usuarios, grupos, contactos y equipos, que el usuario puede seleccionar en un tipo de ámbito determinado. Cuando el usuario selecciona un ámbito de la lista, el cuadro de diálogo aplica los filtros de ese tipo de ámbito para mostrar una lista de objetos entre los que el usuario puede seleccionar.

Cada estructura [**DSOP \_ Scope \_ init \_ info**](/windows/desktop/api/Objsel/ns-objsel-dsop_scope_init_info) contiene una estructura de [**\_ \_ marcas de filtro DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_filter_flags) que especifica los filtros para ese tipo de ámbito. La estructura de **\_ \_ marcas de filtro de DSOP** distingue entre los ámbitos de nivel superior y nivel inferior:

-   Un ámbito de nivel superior es un catálogo global o un dominio que admite el [proveedor LDAP](/windows/desktop/ADSI/adsi-ldap-provider)de ADSI.
-   Un ámbito de nivel inferior incluye grupos de trabajo y todos los equipos individuales. El cuadro de diálogo utiliza el proveedor WinNT de ADSI para tener acceso a un ámbito de nivel inferior.

Hay dos conjuntos de marcas de filtro definidas para su uso en la estructura de [**\_ \_ marcas de filtro DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_filter_flags) : una para ámbitos de nivel superior y otra para ámbitos de nivel inferior. El miembro de **nivel superior** de la estructura de **\_ \_ marcas de filtro DSOP** es una estructura de filtros de nivel superior DSOP que especifica los filtros para ámbitos de nivel superior. [**\_ \_ \_**](/windows/desktop/api/Objsel/ns-objsel-dsop_uplevel_filter_flags) El miembro **flDownlevel** de la estructura de **\_ \_ marcas de filtro DSOP** es un conjunto de marcas que especifican los filtros para los ámbitos de nivel inferior.

 

 