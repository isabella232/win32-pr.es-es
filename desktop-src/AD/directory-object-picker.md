---
title: Selector de objetos de directorio
description: El cuadro de diálogo selector de objetos de directorio permite al usuario seleccionar uno o varios objetos del catálogo global, un dominio o equipo o un grupo de trabajo.
ms.assetid: 5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a
ms.tgt_platform: multiple
keywords:
- Ad selector de objetos de directorio
- AD selector de objetos
- objects AD , selector de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2dec1e0ea4b021b7e8994c02af03269b2fd22cc64c8ed2974b4ab4fae5ac7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118019056"
---
# <a name="directory-object-picker"></a>Selector de objetos de directorio

El cuadro de diálogo selector de objetos de directorio permite al usuario seleccionar uno o varios objetos del catálogo global, un dominio o equipo o un grupo de trabajo. Los tipos de objeto entre los que un usuario puede seleccionar incluyen objetos de usuario, contacto, grupo y equipo. Para obtener más información sobre Active Directory Domain Services, [vea Active Directory Domain Services](active-directory-domain-services.md).

Para mostrar un cuadro de diálogo selector de objetos:

1.  Llame a [**las funciones CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) para crear una instancia de la [**interfaz IDsObjectPicker.**](/windows/desktop/api/Objsel/nn-objsel-idsobjectpicker)
2.  Llame al [**método IDsObjectPicker::Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) para inicializar el cuadro de diálogo.
3.  Llame al [**método IDsObjectPicker::InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog) para mostrar el cuadro de diálogo.
4.  Llame al [**método IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) de la instancia [**de IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) devuelta por el cuadro de diálogo selector de objetos para recuperar los datos de LA LISTA DE SELECCIÓN de [**DSOP de CFSTR \_ \_ DSOP. \_ \_**](cfstr-dsop-ds-selection-list.md) El **formato del \_ Portapapeles CFSTR \_ DSOP DS \_ SELECTION \_ LIST** proporciona **un HGLOBAL** que contiene una [**estructura DS \_ SELECTION \_**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) LIST. La **estructura DS \_ SELECTION \_ LIST** contiene datos sobre los elementos seleccionados en el cuadro de diálogo selector de objetos.

Si el identificador de seguridad (SID) es necesario para un objeto, debe solicitarse directamente desde el selector de objetos agregando el atributo **objectSID** a la lista de atributos que se recuperarán para el objeto seleccionado. No se recomienda pasar el nombre de objeto devuelto a la función [**LsaLookupNames**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames) o [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) porque la búsqueda de nombres será redundante y puede producir un error en algunos casos.

Si se guarda una referencia a los objetos seleccionados, el nombre distintivo no debe guardarse porque el objeto puede moverse, cambiar de nombre o cambiar debido a diferencias de configuración regional. En el caso de las entidades de seguridad, se debe solicitar **objectSID** para el objeto y guardarse de forma segura. Si el nombre de la entidad de seguridad es necesario más adelante, se puede recuperar con la [**función LookupAccountSid.**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) Para todos los demás objetos, se debe solicitar y guardar **objectGUID.**

## <a name="initialization"></a>Inicialización

Cuando se inicializa el cuadro de diálogo selector de objetos, se especifica un conjunto de tipos de ámbito y filtros. Los tipos de ámbito especificados determinan las ubicaciones, dominios o equipos, por ejemplo, desde los que un usuario puede seleccionar objetos. Los filtros determinan los tipos de objetos que un usuario puede seleccionar de un tipo de ámbito determinado. Para más información, consulte la sección Ámbitos y filtros a continuación.

De forma predeterminada, un usuario puede seleccionar un único objeto en el cuadro de diálogo selector de objetos de directorio. Para habilitar varias selecciones, establezca la marca **\_ DSOP FLAG \_ MULTISELECT** en el miembro **flOptions** de la estructura [**INFO de DSOP \_ INIT \_**](/windows/desktop/api/Objsel/ns-objsel-dsop_init_info) cuando se inicializó el cuadro de diálogo.

## <a name="scopes-and-filters"></a>Ámbitos y filtros

La **lista desplegable Buscar** en contiene los ámbitos desde los que un usuario puede seleccionar objetos. Un ámbito es un dominio, equipo, grupo de trabajo o catálogo global que almacena datos sobre y proporciona acceso a un conjunto de objetos disponibles. Las entradas de la lista de ámbitos dependen de los tipos de ámbito y del equipo de destino especificados cuando se llamó por última vez al método [**IDsObjectPicker::Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) para inicializar el cuadro de diálogo selector de objetos.

Un tipo de ámbito es una categoría genérica de ámbitos, como todos los dominios de la empresa a la que pertenece el equipo de destino, el catálogo global de la empresa del equipo de destino o el propio equipo de destino. Para cada tipo de ámbito especificado, el cuadro de diálogo usa el contexto del equipo de destino para determinar las entradas de la lista de ámbitos.

El [**método IDsObjectPicker::Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) toma un puntero a una estructura INFO init de [**DSOP \_ \_**](/windows/desktop/api/Objsel/ns-objsel-dsop_init_info) que contiene una matriz de estructuras DE INFORMACIÓN INIT de [**DSOP \_ SCOPE. \_ \_**](/windows/desktop/api/Objsel/ns-objsel-dsop_scope_init_info) Cada entrada de la **matriz DSOP \_ SCOPE \_ INIT \_ INFO** especifica uno o varios tipos de ámbito, así como filtros aplicables y otros atributos. Los filtros determinan los tipos de objetos, como usuarios, grupos, contactos y equipos, que el usuario puede seleccionar de un tipo de ámbito determinado. Cuando el usuario selecciona un ámbito de la lista, el cuadro de diálogo aplica los filtros de ese tipo de ámbito para mostrar una lista de objetos desde los que el usuario puede seleccionar.

Cada [**estructura info de DSOP SCOPE \_ \_ INIT \_**](/windows/desktop/api/Objsel/ns-objsel-dsop_scope_init_info) contiene una estructura [**DSOP \_ FILTER \_ FLAGS**](/windows/desktop/api/Objsel/ns-objsel-dsop_filter_flags) que especifica los filtros para ese tipo de ámbito. La **estructura DSOP \_ FILTER \_ FLAGS** distingue entre ámbitos de nivel superior y de nivel inferior:

-   Un ámbito de nivel superior es un catálogo global o un dominio que admite el proveedor [LDAP](/windows/desktop/ADSI/adsi-ldap-provider)ADSI .
-   Un ámbito de nivel inferior incluye grupos de trabajo y todos los equipos individuales. El cuadro de diálogo usa el proveedor ADSI WinNT para acceder a un ámbito de nivel inferior.

Hay dos conjuntos de marcas de filtro definidas para su uso en la estructura [**DSOP \_ FILTER \_ FLAGS:**](/windows/desktop/api/Objsel/ns-objsel-dsop_filter_flags) una para ámbitos de nivel superior y otra para ámbitos de nivel inferior. El **miembro Uplevel** de la estructura **DSOP FILTER \_ \_ FLAGS** es una estructura [**DSOP \_ UPLEVEL FILTER \_ \_ FLAGS**](/windows/desktop/api/Objsel/ns-objsel-dsop_uplevel_filter_flags) que especifica los filtros para los ámbitos de nivel superior. El **miembro flDownlevel** de la estructura **DSOP \_ FILTER \_ FLAGS** es un conjunto de marcas que especifican los filtros para los ámbitos de nivel inferior.

 

 