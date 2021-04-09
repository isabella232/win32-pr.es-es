---
title: ncacn_at_dsp atributo)
description: La \_ \_ palabra clave ncacn at DSP identifica AppleTalk DSP como la familia de protocolos para el extremo. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- ncacn_at_dsp el atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9149cd7270c2e82e760c24b4af1fed54c2c08622
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995217"
---
# <a name="ncacn_at_dsp-attribute"></a>ncacn \_ en el \_ atributo DSP

La palabra clave **ncacn \_ at \_ DSP** identifica AppleTalk DSP como la familia de protocolos para el extremo. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre del puerto* 
</dt> <dd>

Especifica una cadena de caracteres de hasta 22 bytes de longitud.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La sintaxis de la cadena de puerto de DSP de AppleTalk, como todas las cadenas de puerto, se define mediante la implementación de transporte y es independiente de la especificación de IDL. El compilador MIDL realiza una comprobación de sintaxis limitada, pero no garantiza que la especificación del punto de conexión sea correcta. Es posible que se notifiquen algunas clases de errores en tiempo de ejecución en lugar de en tiempo de compilación.

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

[**finales**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**enlace de cadenas**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 