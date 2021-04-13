---
title: Códigos de error del proveedor WMI de Servicios de Escritorio remoto (Wbemcli. h)
description: Errores devueltos por el proveedor de WMI de Servicios de Escritorio remoto. Para obtener una lista de otros errores de WMI, vea constantes error de WMI.
ms.assetid: 1e68c41d-f321-4bc5-ba30-b69f5ba741eb
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WBEM_E_FAILED
- WBEM_E_NOT_FOUND
- WBEM_E_PROVIDER_FAILURE
- WBEM_E_TYPE_MISMATCH
- WBEM_E_OUT_OF_MEMORY
- WBEM_E_INVALID_PARAMETER
- WBEM_E_NOT_AVAILABLE
- WBEM_E_NOT_SUPPORTED
- WBEM_E_INVALID_NAMESPACE
- WBEM_E_INVALID_OBJECT
- WBEM_E_INITIALIZATION_FAILURE
- WBEM_E_INVALID_OPERATION
- WBEM_E_INVALID_QUERY
- WBEM_E_INVALID_QUERY_TYPE
- WBEM_E_ALREADY_EXISTS
- WBEM_E_INVALID_SYNTAX
- WBEM_E_READ_ONLY
- WBEM_E_PROVIDER_NOT_CAPABLE
- WBEM_E_ILLEGAL_NULL
- WBEM_E_VALUE_OUT_OF_RANGE
- WBEM_E_INVALID_METHOD
- WBEM_E_INVALID_METHOD_PARAMETERS
- WBEM_E_INVALID_OBJECT_PATH
api_location:
- Wbemcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252015a5d80a1487033ad285ce3080f4d666f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535374"
---
# <a name="remote-desktop-services-wmi-provider-error-codes"></a>Códigos de error del proveedor de Servicios de Escritorio remoto WMI

En la lista siguiente se enumeran los errores de WMI devueltos por el proveedor de WMI de Servicios de Escritorio remoto. Para obtener una lista de otros errores de WMI, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**error de WBEM \_ E \_**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001)
</dt> <dt>



Error en la llamada al método.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002)
</dt> <dt>



No se encontró el objeto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**error del proveedor de WBEM \_ E \_ \_**
</dt> <dd> <dl> <dt>

2147749892 (0x80041004)
</dt> <dt>



El proveedor ha producido un error en algún momento distinto de durante la inicialización.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**\_ \_ no coinciden los tipos E de WBEM \_**
</dt> <dd> <dl> <dt>

2147749893 (0x80041005)
</dt> <dt>



Se ha producido un error de coincidencia de tipos.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**\_ \_ memoria insuficiente \_ de \_ WBEM**
</dt> <dd> <dl> <dt>

2147749894 (0x80041006)
</dt> <dt>



No había memoria suficiente para la operación.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_ \_ parámetro no válido de WBEM E \_**
</dt> <dd> <dl> <dt>

2147749896 (0x80041008)
</dt> <dt>



Uno de los parámetros de la llamada no es correcto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ no \_ disponible**
</dt> <dd> <dl> <dt>

2147749897 (0x80041009)
</dt> <dt>



El recurso, que suele ser un servidor remoto, no está actualmente disponible.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ no \_ compatible**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100C)
</dt> <dt>



No se admite esta característica u operación.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**\_espacio de \_ nombres no válido de WBEM E \_**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100E)
</dt> <dt>



No se pudo encontrar el espacio de nombres especificado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**\_ \_ objeto no válido de WBEM E \_**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100F)
</dt> <dt>



La instancia especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_error de \_ inicialización de WBEM E \_**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014)
</dt> <dt>



Un módulo, como un proveedor, no se pudo inicializar por razones internas.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_ \_ operación no válida de WBEM E \_**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016)
</dt> <dt>



La operación solicitada no es válida. Normalmente, este error está relacionado con intentos no válidos de eliminar clases o propiedades. Este error se devuelve en un intento de modificar una propiedad de invalidación de servidor a través del control de directiva de grupo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_ \_ consulta no válida de WBEM E \_**
</dt> <dd> <dl> <dt>

2147749911 (0x80041017)
</dt> <dt>



La consulta no era válida sintácticamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_tipo de consulta WBEM E \_ no válido \_ \_**
</dt> <dd> <dl> <dt>

2147749912 (0x80041018)
</dt> <dt>



No se admite el lenguaje de consulta solicitado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ ya \_ existe**
</dt> <dd> <dl> <dt>

2147749913 (0x80041019)
</dt> <dt>



En una operación PUT, se especificó la marca **wbemChangeFlagCreateOnly** , pero la instancia ya existe.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_ \_ sintaxis no válida de WBEM E \_**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021)
</dt> <dt>



La consulta no es válida sintácticamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ \_ solo lectura**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023)
</dt> <dt>



La propiedad que intenta modificar es de sólo lectura.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**proveedor de WBEM \_ E \_ \_ no \_ compatible**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024)
</dt> <dt>



El proveedor no puede realizar la operación solicitada. La operación podría incluir una consulta demasiado compleja, recuperar una instancia, crear una clase, actualizar una clase, eliminar una clase o enumerar una clase.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ no válido \_ null**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028)
</dt> <dt>



Se especificó un valor de **Nothing** / **null** para una propiedad que no puede ser **Nothing** / **null**, como una marcada por un calificador de [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**indexado**](/windows/desktop/WmiSdk/optional-qualifiers)o [**not \_ null**](/windows/desktop/WmiSdk/optional-qualifiers) .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_valor de WBEM E comprendido \_ \_ fuera \_ del \_ intervalo**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102B)
</dt> <dt>



La solicitud se realizó con un valor fuera del intervalo o es incompatible con el tipo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ método no válido \_**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102E)
</dt> <dt>



El método solicitado no está disponible.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_parámetros de \_ método no válido de WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102F)
</dt> <dt>



Los parámetros proporcionados para el método no son válidos.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**\_ruta de \_ objeto no válida de WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749946 (0x8004103A)
</dt> <dt>



La ruta de acceso del objeto especificado no era válida.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Wbemcli. h</dt> </dl> |



 

