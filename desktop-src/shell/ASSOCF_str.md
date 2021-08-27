---
description: Proporciona información a los métodos de interfaz IQueryAssociations.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: Enumeración ASSOCF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6920ef874833471d88c4d42a074661337469b11
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477941"
---
# <a name="assocf-enumeration"></a>Enumeración ASSOCF

Proporciona información a los [**métodos de interfaz IQueryAssociations.**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations)

## <a name="syntax"></a>Syntax

<span codelanguage="ManagedCPlusPlus"></span>


| C++ | 
|-----|
| <pre><code>typedef enum  {   ASSOCF_NONE                  = 0x00000000,  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,  ASSOCF_INIT_BYEXENAME        = 0x00000002,  ASSOCF_OPEN_BYEXENAME        = 0x00000002,  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,  ASSOCF_NOUSERSETTINGS        = 0x00000010,  ASSOCF_NOTRUNCATE            = 0x00000020,  ASSOCF_VERIFY                = 0x00000040,  ASSOCF_REMAPRUNDLL           = 0x00000080,  ASSOCF_NOFIXUPS              = 0x00000100,  ASSOCF_IGNOREBASECLASS       = 0x00000200,  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,  ASSOCF_IS_PROTOCOL           = 0x00001000,  ASSOCF_INIT_FOR_FILE         = 0x00002000} ASSOCF;</code></pre> | 




## <a name="constants"></a>Constantes

 <span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF \_ NONE** 

No se establece ninguna de las opciones siguientes.

 <span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF \_ INIT \_ NOREMAPCLSID** 

Indica a [**los métodos de interfaz IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) que no asignen valores CLSID a valores ProgID.

 <span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF \_ INIT \_ BYEXENAME** 

Identifica el valor del parámetro *pwszAssoc* de [**IQueryAssociations::Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) como nombre de archivo ejecutable. Si no se establece esta marca, la clave raíz se establecerá en el ProgID asociado a la clave **.exe** en lugar del ProgID del archivo ejecutable.

 <span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF \_ OPEN \_ BYEXENAME** 

Idéntico a **ASSOCF \_ INIT \_ BYEXENAME.**

 <span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF \_ INIT \_ DEFAULTTOSTAR** 

Especifica que cuando un [**método IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) no encuentra el valor solicitado en la clave raíz, debe intentar recuperar el valor comparable de la **\*** subclave.

 <span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF \_ INIT \_ DEFAULTTOFOLDER** 

Especifica que cuando un [**método IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) no encuentra el valor solicitado en la clave raíz, debe intentar recuperar el valor comparable de la subclave **Folder.**

 <span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF \_ NOUSERSETTINGS** 

Especifica que solo se debe buscar **HKEY \_ CLASSES \_ ROOT** y que se debe omitir **HKEY \_ CURRENT \_ USER.**

 <span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF \_ NOTRUNCATE** 

Especifica que la cadena de devolución no se debe truncar. En su lugar, devuelva un valor de error y el tamaño necesario para la cadena completa.

 <span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**COMPROBACIÓN DE ASSOCF \_** 

Indica a [**los métodos IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) que comprueben que los datos son precisos. Esta configuración permite a **los métodos IQueryAssociations** leer datos del disco duro del usuario para la comprobación. Por ejemplo, pueden comprobar el nombre descriptivo del Registro con el que se almacena en el .exe archivo. Establecer esta marca normalmente reduce la eficacia del método .

 <span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF \_ REMAPRUNDLL** 

Indica a [**los métodos IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) que ignoren Rundll.exe y devuelvan información sobre su destino. Normalmente, **los métodos IQueryAssociations** devuelven información sobre la primera .exe o .dll en una cadena de comando. Si un comando usa Rundll.exe, al establecer esta marca se indica al método que ignore Rundll.exe y devuelva información sobre su destino.

 <span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF \_ NOFIXUPS** 

Indica a [**los métodos IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) que no corrija errores en el Registro, como el nombre descriptivo de una función que no coincide con el que se encuentra en el archivo .exe datos.

 <span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF \_ IGNOREBASECLASS** 

Especifica que se debe omitir el valor BaseClass.

 <span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF \_ INIT \_ IGNOREUNKNOWN** 

**Se introdujo en Windows 7**. Especifica que se debe omitir el ProgID "Desconocido"; en su lugar, se producirá un error.

 <span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**PROGID FIJO DE ASSOCF \_ INIT \_ \_** 

**Se introdujo en Windows 8**. Especifica que el ProgID proporcionado debe asignarse utilizando los valores predeterminados del sistema, en lugar de los valores predeterminados del usuario actual.

 <span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF \_ IS \_ PROTOCOL** 

**Se introdujo en Windows 8**. Especifica que el valor es un protocolo y se debe asignar mediante los valores predeterminados del usuario actual.

 <span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF \_ INIT \_ FOR \_ FILE** 

**Se introdujo en Windows 8.1**. Especifica que el ProgID se corresponde con una asociación basada en la extensión de archivo. Use junto con **ASSOCF \_ INIT \_ FIXED \_ PROGID**.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 2000 Professional, Windows solo aplicaciones de \[ escritorio XP\]               |
| Servidor mínimo compatible | \[Solo aplicaciones de escritorio\] de Windows 2000 Server                                 |
| Encabezado                   |  Shlwapi.h  |



## <a name="see-also"></a>Consulte también

 [**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) 

 

 

© 2017 Microsoft. Todos los derechos reservados.
