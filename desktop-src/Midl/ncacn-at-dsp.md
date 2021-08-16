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
ms.openlocfilehash: cb021f9212f1034f0b3c235ad77d9ad270325af914887252494316f9ae1c41b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642776"
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

## <a name="remarks"></a>Comentarios

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

[**Extremo**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**enlace de cadena**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 