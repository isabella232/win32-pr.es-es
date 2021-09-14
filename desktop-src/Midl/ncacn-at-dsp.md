---
title: ncacn_at_dsp atributo
description: La palabra clave ncacn \_ at dsp identifica el DSP de \_ AppleTalk como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- ncacn_at_dsp atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9149cd7270c2e82e760c24b4af1fed54c2c08622
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159479"
---
# <a name="ncacn_at_dsp-attribute"></a>ncacn \_ en el atributo \_ dsp

La **palabra clave ncacn \_ at \_ dsp** identifica el DSP de AppleTalk como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*port-name* 
</dt> <dd>

Especifica una cadena de caracteres de hasta 22 bytes de longitud.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La sintaxis de la cadena de puerto de DSP de AppleTalk, como todas las cadenas de puerto, se define mediante la implementación de transporte y es independiente de la especificación de IDL. El compilador MIDL realiza una comprobación de sintaxis limitada, pero no garantiza que la especificación del punto de conexión sea correcta. Algunas clases de errores se pueden notifican en tiempo de ejecución en lugar de en tiempo de compilación.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_at_dsp:[my_services_endpoint]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**endpoint**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**enlace de cadena**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 