---
description: Identificador del objeto Policy local.
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: LSA_HANDLE (Ntsecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07bd71a14666dde7bb92e439159a55dd71706612
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374870"
---
# <a name="lsa_handle"></a>CONTROLADOR \_ LSA

El **tipo de datos \_ LSA HANDLE** es un identificador del objeto [**Policy**](policy-object.md) local.


```C++
typedef PVOID LSA_HANDLE, *PLSA_HANDLE;
```



## <a name="remarks"></a>Observaciones

Para poder usar la API de directiva local, la aplicación debe abrir un identificador para un [**objeto Policy.**](policy-object.md) Para ello, llame a [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy). Esta función devuelve un identificador que la aplicación puede especificar en posteriores llamadas a la función de directiva LSA.

Cada identificador tiene un conjunto de permisos asociado que determina las operaciones que la aplicación puede realizar en el [**objeto Policy**](policy-object.md) mediante el identificador. La aplicación puede abrir más de un identificador para el **objeto Policy** a la vez. Cuando ya no se necesita un identificador, la aplicación debe cerrarlo mediante una llamada a [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Ntsecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 

