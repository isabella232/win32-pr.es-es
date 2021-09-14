---
title: Modificador /protocol
description: El modificador /protocol especifica qué protocolo de conexión es compatible con el código auxiliar generado.
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- /protocol switch MIDL
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555482677afff83d9f52e06c7b8e445504d222c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159716"
---
# <a name="protocol-switch"></a>Modificador /protocol

El **modificador /protocol** especifica qué protocolo de conexión es compatible con el código auxiliar generado.

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span id="dce"></span><span id="DCE"></span>dce**


</dt> <dd>

El código auxiliar generado solo admite el protocolo DCE.

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span id="ndr64"></span><span id="NDR64"></span>dín64**


</dt> <dd>

El código auxiliar generado solo admite el protocolo TLS64 de Microsoft.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>all**


</dt> <dd>

El código auxiliar generado admite todos los protocolos disponibles para un entorno determinado.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Las referencias RPC y los datos no semarshals según un protocolo de conexión estricto, también denominado sintaxis de transferencia, que define la representación de la conexión de datos, como el orden en que se serializan los miembros de datos, la alineación de los datos en la conexión, la información adicional incluida con los datos, entre otros. Rpc de Microsoft es compatible con el protocolo TLS (representación de datos de red) de OSF DCE. En la versión de 64 bits de Windows XP, Microsoft presenta un protocolo experimental KERBEROS64 optimizado para transferir datos de 64 bits. SMTP64 no es compatible con versiones anteriores del protocolo DCE.

El **protocolo dce** es compatible con la sintaxis de transferencia de QL de OSF DCE. Este protocolo está optimizado para transferir datos de 32 bits.

El **protocolo press64** solo se admite actualmente cuando se usa junto con el [**modificador /win64.**](-win64.md) Si un solo cliente biz64 intenta conectarse a un servidor solo dce, o viceversa, la llamada se rechaza con RPC \_ S \_ \_ UNSUPPORTED TRANS \_ SYN.

La **opción all** crea un código auxiliar que puede usar cualquier protocolo disponible. En el caso de los códigos auxiliares de 32 bits, el único protocolo disponible actualmente es DCE. En el caso de los códigos auxiliares de 64 bits, creados mediante el modificador [**/win64,**](-win64.md) están disponibles DCE y MUTACIÓN64.

## <a name="examples"></a>Ejemplos

**midl /protocol all /win64 filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**/&lt;Sistema&gt;**](-system-.md)
</dt> </dl>

 

 




