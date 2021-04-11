---
description: Proporciona información a los métodos de la interfaz IQueryAssociations.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: Enumeración ASSOCF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ddb0b4fb89925c643eb01c276772b9a7151578
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279851"
---
# <a name="assocf-enumeration"></a>Enumeración ASSOCF

Proporciona información a los métodos de la interfaz [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .

## <a name="syntax"></a>Sintaxis

<span codelanguage="ManagedCPlusPlus"></span>

<table><colgroup><col style="width: 100%" /></colgroup><thead><tr class="header"><th>C++</th></tr></thead><tbody><tr class="odd"><td><pre><code>typedef enum  { 
  ASSOCF_NONE                  = 0x00000000,
  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,
  ASSOCF_INIT_BYEXENAME        = 0x00000002,
  ASSOCF_OPEN_BYEXENAME        = 0x00000002,
  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,
  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,
  ASSOCF_NOUSERSETTINGS        = 0x00000010,
  ASSOCF_NOTRUNCATE            = 0x00000020,
  ASSOCF_VERIFY                = 0x00000040,
  ASSOCF_REMAPRUNDLL           = 0x00000080,
  ASSOCF_NOFIXUPS              = 0x00000100,
  ASSOCF_IGNOREBASECLASS       = 0x00000200,
  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,
  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,
  ASSOCF_IS_PROTOCOL           = 0x00001000,
  ASSOCF_INIT_FOR_FILE         = 0x00002000
} ASSOCF;</code></pre></td></tr></tbody></table>



## <a name="constants"></a>Constantes

 <span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF \_ ninguno** 

No se ha establecido ninguna de las siguientes opciones.

 <span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF \_ init \_ NOREMAPCLSID** 

Indica a los métodos de interfaz [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) que no asignen valores CLSID a los valores ProgID.

 <span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF \_ init \_ BYEXENAME** 

Identifica el valor del parámetro *pwszAssoc* de [**IQueryAssociations:: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) como nombre de archivo ejecutable. Si no se establece esta marca, la clave raíz se establecerá en el identificador de programa (ProgID) asociado a la clave **. exe** en lugar del identificador de programa (ProgID) del archivo ejecutable.

 <span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF \_ abrir \_ BYEXENAME** 

Idéntico a **ASSOCF \_ init \_ BYEXENAME**.

 <span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF \_ init \_ DEFAULTTOSTAR** 

Especifica que cuando un método [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) no encuentra el valor solicitado bajo la clave raíz, debe intentar recuperar el valor comparable de la **\*** subclave.

 <span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF \_ init \_ DEFAULTTOFOLDER** 

Especifica que cuando un método [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) no encuentra el valor solicitado bajo la clave raíz, debe intentar recuperar el valor comparable de la subclave de **carpeta** .

 <span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF \_ NOUSERSETTINGS** 

Especifica que solo se debe buscar en la **\_ \_ raíz de las clases HKEY** y que el **\_ \_ usuario actual de HKEY** debe omitirse.

 <span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF \_ NOtruncate** 

Especifica que la cadena devuelta no se debe truncar. En su lugar, devuelva un valor de error y el tamaño necesario para la cadena completa.

 <span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**\_comprobar ASSOCF** 

Indica a los métodos de [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) que comprueben que los datos son precisos. Esta configuración permite a los métodos de **IQueryAssociations** leer datos del disco duro del usuario para su comprobación. Por ejemplo, pueden comprobar el nombre descriptivo en el registro con el que se almacena en el archivo. exe. Al establecer esta marca, normalmente se reduce la eficacia del método.

 <span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF \_ REMAPRUNDLL** 

Indica a los métodos de [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) que omitan Rundll.exe y devuelvan información sobre su destino. Normalmente, los métodos **IQueryAssociations** devuelven información sobre el primer archivo. exe o. dll en una cadena de comandos. Si un comando usa Rundll.exe, al establecer esta marca, se indica al método que omita Rundll.exe y devuelva información sobre su destino.

 <span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF \_ NOfixups** 

Indica a los métodos de [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) que no corrijan los errores en el registro, como el nombre descriptivo de una función que no coincide con el encontrado en el archivo. exe.

 <span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF \_ IGNOREBASECLASS** 

Especifica que el valor de BaseClass debe omitirse.

 <span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF \_ init \_ IGNOREUNKNOWN** 

**Introducido en Windows 7**. Especifica que se debe omitir el ProgID "Unknown"; en su lugar, produce un error.

 <span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**ASSOCF \_ init \_ fixed \_ ProgID** 

**Introducido en Windows 8**. Especifica que el ProgID proporcionado debe asignarse utilizando los valores predeterminados del sistema, en lugar de los valores predeterminados del usuario actual.

 <span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF \_ es \_ Protocol** 

**Introducido en Windows 8**. Especifica que el valor es un protocolo y debe asignarse con los valores predeterminados del usuario actual.

 <span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF \_ init \_ para el \_ archivo** 

**Introducido en Windows 8.1**. Especifica que el ProgID corresponde a una asociación basada en la extensión de archivo. Úselo junto con **ASSOCF \_ init \_ fixed \_ ProgID**.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]               |
| Servidor mínimo compatible | \[Solo aplicaciones de escritorio\] de Windows 2000 Server                                 |
| Encabezado                   |  Shlwapi. h  |



## <a name="see-also"></a>Vea también

 [**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) 

 

 

© 2017 Microsoft. Todos los derechos reservados.
