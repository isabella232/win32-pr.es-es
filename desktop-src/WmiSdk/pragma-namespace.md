---
description: Solicita que el compilador cargue el archivo MOF en el espacio de nombres especificado como namespacepath. Si se usan el modificador de espacio de nombres -n del compilador MOF y el comando \# pragma namespace&32;namespacepath, el comando tiene prioridad \# sobre el modificador.
ms.assetid: d280f67a-a798-47c0-b8de-071c290dd216
ms.tgt_platform: multiple
title: pragma (espacio de nombres)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3eea58c8e32ab8b1b851205b365b837194d0472a1c39017e2eb69dc3fe70a98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316831"
---
# <a name="pragma-namespace"></a>pragma (espacio de nombres)

El **comando pragma namespace** preprocessor solicita que el compilador cargue el archivo MOF en el espacio de nombres especificado como *namespacepath*. Si se usan el modificador de espacio de nombres -n del compilador **MOF** y el comando **\# pragma namespacepath,** el comando tiene prioridad sobre el modificador. 

A continuación se describe la sintaxis:


```mof
#pragma namespace ("[Namespace]")
```



*\[ Namespace \]* es el espacio de nombres especificado.

Si no especifica este comando o el modificador de línea de comandos equivalente, el compilador de MOF usa el espacio de \\ nombres predeterminado raíz de forma predeterminada.

## <a name="remarks"></a>Comentarios

Puede requerir que los scripts de cliente y las aplicaciones usen una conexión cifrada para la autenticación agregando el calificador **RequiresEncryption** al archivo .mof que crea el espacio de nombres . También puede modificar un espacio de nombres existente agregando este atributo y compilando de nuevo el archivo MOF. Para obtener más información sobre cómo usar **RequiresEncryption**, vea [Requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo colocar clases o instancias en el espacio de nombres "Root \\ Test".


```mof
#pragma namespace ("\\\\.\\Root\\Test")
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Establecer descriptores de seguridad namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Calificadores WMI estándar**](standard-wmi-qualifiers.md)
</dt> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 




