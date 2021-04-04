---
description: Solicita que el compilador cargue el archivo MOF en el espacio de nombres especificado como namespacepath. Si se usan el modificador del espacio de nombres MOF-n del compilador y el \# espacio de nombres pragma&\# 32; el comando namespacepath, el comando tiene prioridad sobre el modificador.
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
ms.openlocfilehash: b5f5e164632fef5a41e7233caf4fd154d1dafe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811414"
---
# <a name="pragma-namespace"></a>pragma (espacio de nombres)

El comando **pragma namespace** Preprocessing solicita que el compilador cargue el archivo MOF en el espacio de nombres especificado como *namespacepath*. Si se usan el modificador del espacio de nombres MOF **-n** del compilador y el comando **\# pragma namespace** *namespacepath* , el comando tiene prioridad sobre el modificador.

A continuación se describe la sintaxis:


```mof
#pragma namespace ("[Namespace]")
```



El *\[ espacio de nombres \]* es el espacio de nombres especificado.

Si no especifica este comando ni el modificador de línea de comandos equivalente, el compilador MOF usará el \\ espacio de nombres predeterminado raíz de forma predeterminada.

## <a name="remarks"></a>Observaciones

Puede requerir que las aplicaciones y los scripts de cliente usen una conexión cifrada para la autenticación agregando el calificador **RequiresEncryption** al archivo. mof que crea el espacio de nombres. También puede modificar un espacio de nombres existente agregando este atributo y compilar de nuevo el archivo MOF. Para obtener más información sobre cómo usar **RequiresEncryption**, vea [requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo colocar clases o instancias en el espacio de nombres "raíz de \\ prueba".


```mof
#pragma namespace ("\\\\.\\Root\\Test")
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Calificadores WMI estándar**](standard-wmi-qualifiers.md)
</dt> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 




