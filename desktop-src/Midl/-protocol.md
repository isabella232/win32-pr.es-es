---
title: modificador/protocolo
description: El modificador/protocolo especifica qué protocolo de conexión es compatible con el código auxiliar generado.
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- /Protocolo modificador MIDL
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9770fa94d010e21dcbd2a5574a0cffe29273a23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358268"
---
# <a name="protocol-switch"></a>modificador/protocolo

El modificador **/Protocolo** especifica qué protocolo de conexión es compatible con el código auxiliar generado.

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span id="dce"></span><span id="DCE"></span>DCE * * * *


</dt> <dd>

El código auxiliar generado solo es compatible con el protocolo DCE.

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span id="ndr64"></span><span id="NDR64"></span>ndr64****


</dt> <dd>

El código auxiliar generado solo es compatible con el protocolo NDR64 de Microsoft.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>todo * * * *


</dt> <dd>

El código auxiliar generado es compatible con todos los protocolos disponibles para un entorno determinado.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

RPC calcula las referencias y las calcula las referencias de los datos de acuerdo con un protocolo de conexión estricto, también denominado sintaxis de transferencia, que define la representación del cable de datos, como el orden en que se calculan las referencias a los miembros de datos, la alineación de los datos en la conexión, la información adicional incluida con los datos, entre otros. Microsoft RPC es compatible con el protocolo NDR (representación de datos de red) de OSF DCE. En la versión de 64 bits de Windows XP, Microsoft presenta una NDR64 de protocolo experimental que está optimizada para transferir datos de 64 bits. NDR64 no es compatible con el protocolo DCE.

El protocolo **DCE** es compatible con la sintaxis de transferencia de NDR de OSF DCE. Este protocolo está optimizado para transferir datos de 32 bits.

Actualmente, el protocolo **ndr64** solo se admite cuando se usa junto con el modificador [**/Win64**](-win64.md) Si un cliente de ndr64 solo intenta conectarse a un servidor de solo DCE, o viceversa, se rechaza la llamada con \_ \_ Trans S no compatible con RPC \_ \_ .

La opción **All** crea un código auxiliar que puede usar cualquier protocolo disponible. En el caso de los códigos auxiliares de 32 bits, el único protocolo disponible actualmente es DCE. En el caso de los códigos auxiliares de 64 bits creados mediante el modificador [**/Win64**](-win64.md) , tanto DCE como NDR64 están disponibles.

## <a name="examples"></a>Ejemplos

**MIDL/protocolo All/Win64 FILENAME. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/<system>**](-system-.md)
</dt> </dl>

 

 




